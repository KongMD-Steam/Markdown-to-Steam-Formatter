# Markdown to Steam Formatter
Markdown to Steam Formatter is a group of utilities you can use to convert Markdown formatting to the equivalent Steam formatting.

## Using the Notepad++ Macro (Windows only)
1. Download and install Notepad++. The macro should work with any of the versions available.
2. Click the green 'Clone or Download' button in Github and download a .zip of this repository.
3. Copy **NPP_Macro\shortcuts.xml** from the .zip file to your `%APPDATA%\Notepad++` directory and overwrite the file there. 
4. Open Notepad++, and paste in the Markdown text you want to convert. Use 'formatting_sample.md' from the .zip file, if you want.
5. Click the Macro menu and select 'MarkdownToSteam' from the list

**NOTE:** If you want to preserve your existing macros, open NPP_Macro\shortcuts.xml in a text editor, copy the entire `<Macro name="MarkdownToSteam">` XML element, and paste it inside the `<Macros>` element in your shortcuts.xml file.

## Notes on Behavior
* Markdown Ordered Lists remain unchanged. The formatting would be very close to Steam, so I didn't bother.
* Adds a newline + space character at the bottom of the file to make Lists at EOF match the RegEx pattern (hack)
* Hover text and Alt. Text in links and images isn't supported by Steam, so that text will be discarded
* Steam doesn't have an inline codeblock, so inline code formatting 'uses apostrophes instead'
* Code blocks that have the backtick character in the first three chars of the body might not be replaced. 98% of users will never encounter this bug naturally.
* Reference-style links & images are not supported, yet. Inline link & image formatting works fine.
* Tables are not yet supported, due to the complexity of the RegEx involved. Will hopefully get support added soon.

## VSCode plugin (Cross-Platform)
This is on the roadmap!

## Contributing
See a RegEx pattern that needs improvement? Send in a Pull Request with some example text to match, and I'll probably merge it.

## Credits ## 
* KongMD - NPP macro and RegEx patterns
* GreatGrogrodor - Extended support for steam formatting.