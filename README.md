# Additional Syntax Highlighting files for Kate

## Installation

~~~bash
mkdir -p ~/.local/share/org.kde.syntax-highlighting/syntax/
cp ./jsonnet.xml ~/.local/share/org.kde.syntax-highlighting/syntax/
~~~

Restart Kate

## Installation for development

~~~bash
mkdir -p ~/.local/share/org.kde.syntax-highlighting/syntax/
ln -s $(pwd)/jsonnet.xml ~/.local/share/org.kde.syntax-highlighting/syntax/
~~~

Once Kate has been restarted the new sytax file is known.

Changes can now be loaded by executing `reload-highlighting` in the Kate Commandline (open with `F7`).

## Documentation

* Developer reference: See [KatePart Handbook](https://docs.kde.org/stable5/en/kate/katepart/index.html) > Extending KatePart > [Working with Syntax Highlighting](https://docs.kde.org/stable5/en/kate/katepart/highlight.html)
* The original [Kate syntax files](https://kate-editor.org/syntax/data/)
    * [json.xml](https://kate-editor.org/syntax/data/syntax/json.xml) as base for the jsonnet snytax file
    * [scss.xml](https://kate-editor.org/syntax/data/syntax/scss.xml) as example for detecting comments and functions
* A syntax file for the Atom editor: https://github.com/google/language-jsonnet

# XML Validation

Optionally: Download the latest language.xsd from https://invent.kde.org/frameworks/syntax-highlighting/-/tree/master/data/schema to the root of this repo.

Vsalidate with `./validatehl.sh jsonnet.xml`
