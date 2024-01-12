# Obisidan Stream Part 2

follow up from [obsidian and obsidian share](obsidian%20and%20obsidian%20share.md)

## Themes
(install from the appearance section of settings):
- [Minimal](https://github.com/kepano/obsidian-minimal)
- [Things](https://github.com/colineckert/obsidian-things)
- Default theme
	- honestly pretty good, way better than it was a few years ago

## Plugins
Taylor's Community Plugins:
- obsidian-languagetool-plugin
- copy-url-in-preview
- obsidian-readability
- dataview
- tag-wrangler
- calendar
- obsidian-table-generator
- table-editor-obsidian
- obsidian-auto-link-title
- janitor
- url-into-selection
- link-tree
- markdown-table-editor
- obsidian-style-settings
- copilot
- obsidian-shellcommands

## Taylor's weirdo public notes system:

make a public folder and initialize a git repo in there

https://github.com/taylorjadin/obsidian-notes

Obisdian Vault `public` folder --> [Github repo](https://github.com/TaylorJadin/obsidian-notes)

Use the shell commands community plugin for quick syncing
![](public_files/Capture%202024-01-12%2008.54.08@2x.png)

### integration with docsify-this!

![](public_files/Capture%202024-01-12%2008.49.10@2x.png)

I set up a redirect so I can share nice clean looking URLs with the note title. For instance, this note should be at https://notes.jadin.me/obsidian-stream-2 because the title of the note is obsidian-stream-2 

the pattern is like this:
https://notes.jadin.me/NOTENAME --> https://docsify.jadin.me/?basePath=https://raw.githubusercontent.com/TaylorJadin/obsidian-notes/main&homepage=NOTENAME.md#/