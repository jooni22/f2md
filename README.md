# f2md
This bash script, named "code_to_markdown.sh", allows you to collect files with specified extensions from a directory and its subdirectories, and generate a well-formatted Markdown file with the contents of those files. It provides a convenient way to gather code snippets or text content scattered across multiple files into a single, organized document.

Key features of the script:

1. Extension filtering: Use the "-n" option followed by a comma-separated list of file extensions to specify which types of files to include in the Markdown file. For example, "-n pdf,md,txt,rs,toml" will collect files with the extensions ".pdf", ".md", ".txt", ".rs", and ".toml".

2. Directory exclusion: Use the "-e" option followed by a comma-separated list of directory names to exclude specific directories from the file collection process. This is useful when you want to ignore certain folders, such as build directories or documentation folders. For example, "-e target,docs" will exclude the "target" and "docs" directories and their subdirectories from the search.

3. Hidden folder exclusion: The script automatically excludes hidden folders (folders with names starting with a dot ".") from the file collection process. This helps to avoid including unnecessary or system-specific files in the Markdown file.

4. PDF file support: If a file with the ".pdf" extension is encountered and the "pdftotext" utility is installed on the system, the script will extract the text content from the PDF file and include it in the Markdown file. If "pdftotext" is not available, the script will skip the PDF file and display a message indicating that PDF support is disabled.

5. Help documentation: Use the "-h" or "--help" option to display a help message explaining the usage and options of the script.

To use the script, follow these steps:

1. Make the script executable by running the command: `chmod +x code_to_markdown.sh`
2. Run the script with the desired options. For example:
