
| Command                     | What it does                                                                  | Best Used For                                |
| --------------------------- | ----------------------------------------------------------------------------- | -------------------------------------------- |
| `sudo lshw -short`          | Displays a compact, dense summary of all hardware in a table layout.          | Getting a quick snapshot of the system.      |
| `sudo lshw -C memory`       | Filters the hardware profile to show only RAM details (size, banks, speed).   | Checking memory upgrade compatibility.       |
| `sudo lshw -C network`      | Targets and isolates network adapters, showing Wi-Fi and Ethernet hardware.   | Finding your specific network card model.    |
| `sudo lshw -C display`      | Isolates graphics cards and video processing controllers.                     | Identifying your GPU.                        |
| `sudo lshw -json`           | Exports the full system hardware map into structured JSON format.             | Automating scripts or data logging.          |
| `sudo lshw -html > hw.html` | Converts the hardware profile into a clean, visual HTML webpage file.         | Reviewing configurations in a browser.       |
| `sudo lshw -sanitize`       | Removes sensitive markers like system serial numbers or private IP addresses. | Sharing system information safely on forums. |
