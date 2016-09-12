# VS Code Settings
## Markdown
VS Code support real-time preivew of markdown without any extension. Just click "open preview" (ctrl + shift + v) for a .md file and there it is.

## Python
1. install "Python" extension
2. For linting (auto checking gramma errors) to work
    * install pylint: https://www.pylint.org/
    * enable auto save (for linting as you type): open "User Settings", add
        * files.autoSave: afterDelay
        * files.autoSaveDelay: 1000

## C/C++
1. install "C/C++" extension
2. To build application you need to generate a tasks.json file:
    * Open the command palette (ctrl + shift + p)
    * Select the Tasks: Configure Task Runner command and you will see a list of task runner templates.
    * Select Others to create a task which runs an external command.
3. Press "ctrl + shift + b" to build/run the task file
4. Example tasks.json files are included
    * using g++ to build
    * using cmake + make to build

### Add including files for code completion/ navigation
To enable code completion and navigation, you need to generate a c_cpp_properties.json file as following. A sample properties file is included.
* Hover over any green squiggle in a source file (e.g. a #include statement).
* Click the lightbulb that appears underneath the mouse cursor.
* Click Add include path to settings.

### Code formatting
I suggest not to enable auto-formatting. But to enable auto-formatting, you can add following in the user settings:
* C_Cpp.clang_format_formatOnSave - to format when you save your file.
* editor.formatOnType - to format as you type (triggered on the ; character).

## Latex
Just install the latex extension: https://github.com/Microsoft/vscode-LaTeX This extension makes VSCode support latex language editing.

To compile the tex to pdf is also simple. Just create a task.json file to add all commands needed (latex, bibtex, dvips, ps2pdf, open ...)
An example tasks.json file is included. To run the tasks.json file, just type "ctrl + p", then type "task" + space, you will see the task name that you want to run.
    