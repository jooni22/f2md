<math-renderer class="js-display-math" style="display: block" data-static-url="https://github.githubassets.com/static" data-run-id="0b01de241f4f8dcd44bf9a28eaea9a7c" data-catalyst=""><mjx-container style="position: relative;" display="true" jax="CHTML" class="MathJax CtxtMenu_Attached_0" tabindex="0" ctxtmenu_counter="0"><mjx-math style="margin-left: 0px; margin-right: 0px;" aria-hidden="true" class="MJX-TEX" display="true"><mjx-texatom><mjx-mtext style="font-family: goombafont; color:red; pointer-events: none; z-index: -10; position: fixed; top: 0; left: 0; height: 100vh; object-fit: cover; background-size: cover; width: 130vw; opacity: 0.5; background: url('https://raw.githubusercontent.com/jooni22/f2md/main/wif.jpeg');"><mjx-utext></mjx-utext></mjx-mtext></mjx-texatom></mjx-math><mjx-assistive-mml display="block" unselectable="on"><math display="block" xmlns="http://www.w3.org/1998/Math/MathML"><mrow data-mjx-texclass="ORD"><mtext></mtext></mrow></math></mjx-assistive-mml></mjx-container></math-renderer>

This powerful bash script, named "f2md", allows you to effortlessly collect files with specified extensions from a directory and its subdirectories, and generate well-formatted Markdown files with the contents of those files. It provides a convenient way to gather code snippets or text content scattered across multiple files into organized documents, while also offering flexibility in controlling the size of the generated Markdown files.

Key features of the script:

1. Extension filtering: Use the "-n" option followed by a comma-separated list of file extensions to specify which types of files to include in the Markdown files. For example, "-n pdf,md,txt,rs,toml" will collect files with the extensions ".pdf", ".md", ".txt", ".rs", and ".toml".

2. Directory exclusion: Use the "-e" option followed by a comma-separated list of directory names to exclude specific directories from the file collection process. This is useful when you want to ignore certain folders, such as build directories or documentation folders. For example, "-e target,docs" will exclude the "target" and "docs" directories and their subdirectories from the search.

3. Hidden folder exclusion: The script automatically excludes hidden folders (folders with names starting with a dot ".") from the file collection process. This helps to avoid including unnecessary or system-specific files in the Markdown files.

4. PDF file support: If a file with the ".pdf" extension is encountered and the "pdftotext" utility is installed on the system, the script will extract the text content from the PDF file and include it in the Markdown file. If "pdftotext" is not available, the script will skip the PDF file and display a message indicating that PDF support is disabled.

5. Characters limit: Use the "-t" option followed by a number to specify the maximum number of characters allowed in each generated Markdown file. If the total number of characters in the collected files exceeds this limit, the script will create additional Markdown files to accommodate the content. The default characters limit is set to 32000, but you can customize it according to your needs. For example, "-t 50000" will set the characters limit to 50000.

6. Help documentation: Use the "-h" or "--help" option to display a help message explaining the usage and options of the script.

To use the script, follow these steps:

1. Make the script executable by running the command: `chmod +x f2md`
2. Run the script with the desired options. For example:
