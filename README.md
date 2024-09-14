# Python-Get-game-Data
A Python script to automate the process of collecting game directories, compiling Go game code, and generating metadata. This script is particularly useful for organizing game projects written in Go, but can be adapted for other programming languages.

## Features
Directory Scanning: Searches a specified source directory for subdirectories containing the word "game" (case-insensitive).
Directory Renaming: Strips "_game" from directory names for cleaner organization.
Directory Copying: Copies and overwrites game directories to a target location.
Code Compilation: Compiles Go code (.go files) found within the game directories.
Metadata Generation: Creates a metadata.json file in the target directory with details about the games.

## Requirements
Python 3.x
Go programming language installed (for compiling .go files)

## How It Works
1. Find All Game Paths
The script starts by scanning the immediate subdirectories of the source directory to find any directories containing the word "game".

2. Generate New Directory Names
It then generates new directory names by stripping "_game" from the original directory names.

3. Create Target Directory
If the target directory doesn't exist, the script creates it.

4. Copy and Overwrite Directories
Each game directory is copied to the target directory with the new name. If a directory with the same name exists in the target location, it is overwritten.

5. Compile Game Code
The script searches for Go code files (.go files) in each copied directory and compiles them using the go build command.

6. Generate Metadata
Finally, a metadata.json file is created in the target directory, containing the names of the games and the total number of games processed.

## Customization
Changing the Game Directory Pattern: Modify GAME_DIR_PATTERN to search for a different pattern in directory names.
Changing the Code Extension: Update GAME_CODE_EXTENSION if your game code uses a different file extension.
Changing the Compile Command: Adjust GAME_COMPILE_COMMAND to compile code written in a language other than Go.

## Potential Improvements
Error Handling: Add comprehensive error handling for robustness.
Command Execution: Ensure that the run_command function captures and handles errors appropriately.
Recursive Directory Search: Extend the directory scanning to search subdirectories recursively if needed.
Return Statements: Verify that all functions return values as expected.

## License
This project is licensed under the MIT License.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

