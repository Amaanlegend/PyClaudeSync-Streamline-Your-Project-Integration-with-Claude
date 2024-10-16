# PyClaudeSync: Streamline Your Project Integration with Claude

PyClaudeSync is a Python package designed to make uploading your entire project directory to a Claude project effortless. By doing so, Claude can access all your project files, enabling it to provide more insightful analysis and interact with your codebase more effectively.

# Key Features:

- **Project Setup**: Automatically prepare your project for integration with Claude by generating a .ignore file. This file lets you specify which files and directories should be excluded from uploads.

- **Claude Project Creation**: Seamlessly create a new Claude project and upload your complete directory, including all relevant files and folders.

- **Project Updates**: Keep your Claude project up to date by re-uploading your current directory, ensuring it reflects the latest version of your project.

- **Custom Ignore Rules**: Modify the pyclaudesync.ignore file to control which directories, file types, or filenames should be skipped during the upload process.

## Requirements:

- A Claude account.
- Python 3.6 or newer.
- A session key from your Claude account.

Installation:

You can easily install PyClaudeSync using pip:

```bash
pip install pyclaudesync
```

## How to Use PyClaudeSync:

### Initialize Your Project
Begin by initializing the project, which will create necessary configuration files, including the ignore file (pyclaudesync.ignore), and save your session key.

```bash
python -m pyclaudesync.cli init -K "your_session_key"
```

### Create a New Claude Project
After initialization, create a new project in Claude. This will upload your project directory, excluding files specified in the ignore file.

```bash
python -m pyclaudesync.cli create -N "Your Project Name"
```

### Update the Claude Project
As your project evolves, use the update command to re-upload your project to Claude, replacing outdated files with the latest versions.

```bash
python -m pyclaudesync.cli update
```

### Customizing the Ignore File:
The pyclaudesync.ignore file lets you specify which folders, file types, and filenames to exclude during the upload process. 

Here’s an example:
```plaintext 
ignore_folders=[".venv", ".idea", ".vscode"]
ignore_file_extensions=["pdf", "jpg", "png", "pyc"]
ignore_name_includes=["pyclaudesync"]
```

- ignore_folders: List of directories to exclude from uploads.
- ignore_file_extensions: Specify file types to be ignored.
- ignore_name_includes: Skip files containing specific substrings in their names.

### Updating Your Session Key:
To update your session key, simply open the `pyclaudesync.key` file and replace its content with the new key.

## Disclaimer:
This package provides an unofficial API for Claude and is not affiliated with or endorsed by Claude AI or Anthropic. Please use it responsibly and refer to the official Claude AI documentation for further details.


