| Search Type                  | Command                  | Description                                                                                 |
| ---------------------------- | ------------------------ | ------------------------------------------------------------------------------------------- |
| Simple Search                | `fd invoice`             | Search for any file or directory containing a specific phrase.                              |
| By Extension                 | `fd -e md`               | Filter results by file extension using the `-e` flag.                                       |
| Specific Directory           | `fd report Documents/`   | Limit the search to a specific directory.                                                   |
| Include Hidden/Ignored Files | `fd -H secret_config`    | Search hidden files and directories. Use `-I` to ignore `.gitignore` rules as well.         |
| Search by Type               | `fd -t d project_folder` | Search only for directories (`d`) or use `-t f` for files.                                  |
| Execute Commands             | `fd -e pdf -x gzip {}`   | Run a command on every matched result. In this example, compress all PDF files with `gzip`. |
