Explain this command:
sed 's/ /_/g'  sed.txt |   sed 's/\[.*\]//g' | sed 's/[^a-zA-Z_.]//g'|sed 's/__/_/g'|  sed 's/_\././g'

This command is a text-processing pipeline that cleans up filenames or strings (likely YouTube video titles) by converting spaces to underscores, stripping brackets, removing random symbols/numbers, and fixing messy punctuation.
Here is the step-by-step breakdown of how your text changes as it flows through each pipe (|):
1. sed 's/ /_/g' sed.txtWhat it does: Reads the file sed.txt and replaces every single space character with an underscore (_).Why: It standardizes spacing so the text is safe for command-line file names (which hate raw spaces).
2. sed 's/\[.*\]//g'What it does: Finds any opening square bracket [, matches everything inside it, and deletes the brackets along with their contents.Why: This is commonly used to strip out YouTube video IDs (like [4JWeU78A95c]) or tags from filenames.
3. sed 's/[^a-zA-Z_.]//g'What it does: Deletes any character that is not a letter (A-Z, a-z), an underscore (_), or a period (.).Why: It wipes out numbers, dashes, spaces, colons, and special symbols, leaving only clean text and the file extension.
4. sed 's/__/_/g'What it does: Finds any double underscores (__) and squashes them down into a single underscore (_).Why: Because Step 2 and Step 3 delete characters, they often leave behind orphan underscores next to each other (e.g., name_[id].webm becomes name__.webm). This cleans up that formatting.
5. sed 's/_\././g'What it does: Looks for an underscore right before a period (_.) and deletes the underscore, leaving just the period (.).Why: It ensures your file extensions look clean (changing file_.webm to file.webm).

You can combine all of this into one command
sed 's/ /_/g; s/\[.*\]//g; s/[^a-zA-Z_.]//g; s/__/_/g; s/_\././g' sed.txt

for file in *.webm *.mp4; do
    # Prevent errors if no files match the pattern
    [ -f "$file" ] || continue

    # Process the filename through your sed chain
    new_name=$(echo "$file" | sed 's/ /_/g; s/\[.*\]//g; s/[^a-zA-Z_.]//g; s/__/_/g; s/_\././g')

    if [ "$file" != "$new_name" ]; then
        echo "Targeting: '$file' ---> '$new_name'"
    fi
done

Safety Features Included:

- **`[ -f "$file" ] || continue`**: Ensures the script ignores folders so you don't accidentally rename directories.
- **`mv -n`**: The `-n` (no-clobber) flag prevents the script from accidentally overwriting an existing file if two messy filenames happen to resolve to the exact same clean name.



Live Script

for file in *.webm *.mp4; do
    [ -f "$file" ] || continue
    new_name=$(echo "$file" | sed 's/ /_/g; s/\[.*\]//g; s/[^a-zA-Z_.]//g; s/__/_/g; s/_\././g')
    
    if [ "$file" != "$new_name" ]; then
        mv -n "$file" "$new_name"
    fi
done
