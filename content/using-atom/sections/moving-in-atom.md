---
title: Moving in Atom
---
### Moving in Atom

While it's pretty easy to move around Atom by clicking with the mouse or using the arrow keys, there are some keybindings that may help you keep your hands on the keyboard and navigate around a little faster.

{{#mac}}

Atom ships with many of the basic Emacs keybindings for navigating a document. To go up and down a single character, you can use <kbd class="platform-mac">Ctrl+P</kbd> and <kbd class="platform-mac">Ctrl+N</kbd>. To go left and right a single character, you can use <kbd class="platform-mac">Ctrl+B</kbd> and <kbd class="platform-mac">Ctrl+F</kbd>. These are the equivalent of using the arrow keys, though some people prefer not having to move their hands to where the arrow keys are located on their keyboard.

In addition to single character movement, there are a number of other movement keybindings:

{{/mac}}

{{#windows}}

Atom has support for all the standard Windows cursor movement key combinations. To go up, down, left or right a single character you can use the arrow keys.

In addition to single character movement, there are a number of other movement keybindings:

{{/windows}}

{{#linux}}

Atom has support for all the standard Linux cursor movement key combinations. To go up, down, left or right a single character you can use the arrow keys.

In addition to single character movement, there are a number of other movement keybindings:

{{/linux}}

* <span class="platform-mac"><kbd class="platform-mac">Alt+Left</kbd> or <kbd class="platform-mac">Alt+B</kbd></span><kbd class="platform-windows platform-linux">Ctrl+Left</kbd> - Move to the beginning of word
* <span class="platform-mac"><kbd class="platform-mac">Alt+Right</kbd> or <kbd class="platform-mac">Alt+F</kbd></span><kbd class="platform-windows platform-linux">Ctrl+Right</kbd> - Move to the end of word
* <span class="platform-mac"><kbd class="platform-mac">Cmd+Left</kbd> or <kbd class="platform-mac">Ctrl+A</kbd></span><kbd class="platform-windows platform-linux">Home</kbd> - Move to the first character of the current line
* <span class="platform-mac"><kbd class="platform-mac">Cmd+Right</kbd> or <kbd class="platform-mac">Ctrl+E</kbd></span><kbd class="platform-windows platform-linux">End</kbd> - Move to the end of the line
* <kbd class="platform-mac">Cmd+Up</kbd><kbd class="platform-windows platform-linux">Ctrl+Home</kbd> - Move to the top of the file
* <kbd class="platform-mac">Cmd+Down</kbd><kbd class="platform-windows platform-linux">Ctrl+End</kbd> - Move to the bottom of the file

You can also move directly to a specific line (and column) number with <kbd class="platform-all">Ctrl+G</kbd>. This will bring up a dialog that asks which line you would like to jump to. You can also use the `row:column` syntax to jump to a character in that line as well.

![Go directly to a line](../../images/goto.png "Go directly to a line")

#### Navigating by Symbols

You can also jump around a little more informatively with the Symbols View. To jump to a symbol such as a method definition, press <kbd class="platform-mac">Cmd+R</kbd><kbd class="platform-windows platform-linux">Ctrl+R</kbd>. This opens a list of all symbols in the current file, which you can fuzzy filter similarly to <kbd class="platform-mac">Cmd+T</kbd><kbd class="platform-windows platform-linux">Ctrl+T</kbd>. You can also search for symbols across your project but it requires a `tags` file.

![Search by symbol across your project](../../images/symbol.png)

You can generate a `tags` file by using the [ctags utility](https://ctags.io/). Once it is installed, you can use it to generate a `tags` file by running a command to generate it. See the [ctags documentation](https://docs.ctags.io/en/latest/) for details.

Once you have your `tags` file generated, you can use it to search for symbols across your project by pressing <kbd class="platform-mac">Cmd+Shift+R</kbd><kbd class="platform-windows platform-linux">Ctrl+Shift+R</kbd>. This also enables you to use <kbd class="platform-mac">Alt+Cmd+Down</kbd><kbd class="platform-windows platform-linux">Alt+Ctrl+Down</kbd> to go to and <kbd class="platform-mac">Alt+Cmd+Up</kbd><kbd class="platform-windows platform-linux">Alt+Ctrl+Up</kbd> to return from the declaration of the symbol under the cursor.

You can customize how tags are generated by creating your own `.ctags` file in your home directory, <span class="platform-mac platform-linux">`~/.ctags`</span><span class="platform-windows">`%USERPROFILE%\.ctags`</span>. An example can be found [here](https://github.com/atom/symbols-view/blob/master/lib/ctags-config).

The symbols navigation functionality is implemented in the [symbols-view](https://github.com/atom/symbols-view) package.

#### Bookmarks

Atom also has a great way to bookmark specific lines in your project so you can jump back to them quickly.

If you press <kbd class="platform-mac">Cmd+F2</kbd><kbd class="platform-windows">Alt+Ctrl+F2</kbd><kbd class="platform-linux">Ctrl+Shift+F2</kbd>, Atom will toggle a "bookmark" on the current line. You can set these throughout your project and use them to quickly find and jump to important lines of your project. A small bookmark symbol is added to the line gutter, like on line 22 of [the image below](#bookmarks-image).

If you hit <kbd class="platform-all">F2</kbd>, Atom will jump to the next bookmark in the file you currently have focused. If you use <kbd class="platform-all">Shift+F2</kbd> it will cycle backwards through them instead.

You can also see a list of all your project's current bookmarks and quickly filter them and jump to any of them by hitting <kbd class="platform-all">Ctrl+F2</kbd>.

<a name="bookmarks-image"/>
![View and filter bookmarks](../../images/bookmarks.png "View and filter bookmarks")

The bookmarks functionality is implemented in the [bookmarks](https://github.com/atom/bookmarks) package.