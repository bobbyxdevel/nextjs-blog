---
title: Emacs Quickguide
date: 2025-04-09T05:22:00.000Z
author:
  name: bobbyxdevel
  picture: /assets/logo.jpg
ogImage:
  url: /assets/9d07ed17d5cad9e6177ce0c65388d024.jpg
---
\# Introduction to Emacs

Welcome to your Emacs journey! As your tutor, I'll guide you through learning Emacs from the ground up. Let's start with the fundamentals.

\## What is Emacs?

Emacs is a powerful, extensible text editor with a rich history dating back to the 1970s. More than just a text editor, it's often described as an integrated computing environment that can be used for editing text, programming, managing files, running shell commands, and much more.

Key characteristics that make Emacs special:

\- \*\*Extensibility\*\*: Nearly every aspect can be customized using Emacs Lisp  
\- \*\*Self-documenting\*\*: Comprehensive built-in help system  
\- \*\*Free and open-source\*\*: Part of the GNU Project  
\- \*\*Cross-platform\*\*: Works on Linux, macOS, Windows, and other systems

\## Installing Emacs on Arch Linux

Let's get Emacs installed on your Arch Linux system. Open your terminal (Alacritty, Kitty, or Konsole) and run:

\`\`\`bash  
sudo pacman -S emacs  
\`\`\`

This will install the current stable version of Emacs from the official Arch repositories.

\## Starting Emacs

After installation, you can start Emacs by typing in your terminal:

\`\`\`bash  
emacs  
\`\`\`

You can also run Emacs in terminal mode (without a graphical interface) using:

\`\`\`bash  
emacs -nw  
\`\`\`

\## The Emacs Interface

When you first open Emacs, you'll see something like this:

\- A \*\*menu bar\*\* at the top  
\- A large editing area (the \*\*buffer\*\*)  
\- A \*\*mode line\*\* at the bottom showing information about the current buffer  
\- A \*\*minibuffer\*\* at the very bottom for commands and messages

Key terminology to understand:

\- \*\*Buffer\*\*: A workspace for viewing and editing text  
\- \*\*Window\*\*: A viewport displaying a buffer (Emacs can split into multiple windows)  
\- \*\*Frame\*\*: What other programs call a "window" (the entire Emacs application window)  
\- \*\*Point\*\*: The cursor position  
\- \*\*Mark\*\*: A saved position used for selecting text  
\- \*\*Region\*\*: The area between point and mark  
\- \*\*Mode\*\*: A set of behaviors and customizations (major modes for specific file types, minor modes for additional features)

\## Emacs Key Notation

Emacs uses a special notation for key combinations:

\- \`C-x\` means "hold Ctrl and press x"  
\- \`M-x\` means "hold Alt (Meta) and press x"  
\- \`C-x C-f\` means "hold Ctrl and press x, then while still holding Ctrl, press f"  
\- \`C-g\` is the universal "cancel" command - remember this if you get stuck!

\## Basic Navigation

Let's learn how to move around in Emacs:

\- \`C-f\`: Move forward one character  
\- \`C-b\`: Move backward one character  
\- \`C-n\`: Move to next line  
\- \`C-p\`: Move to previous line  
\- \`C-a\`: Move to beginning of line  
\- \`C-e\`: Move to end of line  
\- \`M-<\`: Move to beginning of buffer  
\- \`M->\`: Move to end of buffer

Try these commands now to get comfortable moving around.

\## Exiting Emacs

To exit Emacs:

\- \`C-x C-c\`: Quit Emacs (it will prompt to save unsaved buffers)

If you're ever stuck or want to cancel a command in progress:

\- \`C-g\`: Cancel the current command

\## Getting Help

Emacs has an excellent built-in help system:

\- \`C-h t\`: Start the built-in tutorial  
\- \`C-h k\`: Describe what a key combination does  
\- \`C-h f\`: Describe a function  
\- \`C-h v\`: Describe a variable  
\- \`C-h i\`: Open the Info documentation browser

\## Practice Exercises

Let's apply what you've learned:

1\. Start Emacs in your terminal.  
2\. Practice navigation using the key combinations above.  
3\. Try opening the tutorial with \`C-h t\`.  
4\. Find out what \`C-x C-f\` does by using \`C-h k C-x C-f\`.  
5\. Exit Emacs using \`C-x C-c\`.

\## Questions to Check Understanding

1\. What key combination would you use to move to the end of a line?  
2\. How would you cancel a command that you started but don't want to complete?  
3\. What's the difference between a buffer and a window in Emacs terminology?  
4\. How would you access Emacs' built-in tutorial?

In our next lesson, we'll learn how to create and save files, basic editing commands, and working with multiple buffers. Is there anything specific about these basics you'd like me to clarify before we move on?

\---

\> let's move on

\---

\# Lesson 2: Files, Editing, and Buffers

Now that you've been introduced to Emacs basics, let's learn how to work with files, perform basic editing operations, and manage multiple buffers.

\## Creating and Opening Files

One of the most common operations in Emacs is opening files:

\- \`C-x C-f\`: Find file (open a file or create a new one)

When you press this key combination, the minibuffer will prompt you for a filename. You can:  
\- Type a path to an existing file to open it  
\- Type a new filename to create it  
\- Use tab completion to navigate directories

Try creating a new file now:  
1\. Press \`C-x C-f\`  
2\. Type \`~/practice.txt\` (this will create a file in your home directory)  
3\. Press Enter

\## Saving Files

After making changes to a file, you'll want to save it:

\- \`C-x C-s\`: Save the current buffer to its file  
\- \`C-x C-w\`: Save as (write file to a new name)

\## Basic Editing Commands

Now let's learn how to edit text effectively:

\*\*Inserting and Deleting\*\*  
\- Just type to insert text at the cursor position  
\- \`Backspace\`: Delete the character before the cursor  
\- \`C-d\`: Delete the character under the cursor  
\- \`C-k\`: Kill (cut) from cursor to end of line  
\- \`M-d\`: Kill word forward  
\- \`M-Backspace\`: Kill word backward

\*\*Undo and Redo\*\*  
\- \`C-/\` or \`C-\_\` or \`C-x u\`: Undo  
\- To redo in vanilla Emacs, you undo the undo by pressing \`C-g\` and then using undo again

\*\*Copy, Cut, and Paste\*\*  
\- \`C-SPC\`: Set mark (start selection)  
\- Navigate to select text  
\- \`M-w\`: Copy the selected region (Emacs calls this "save to kill ring")  
\- \`C-w\`: Cut the selected region (Emacs calls this "kill region")  
\- \`C-y\`: Paste (Emacs calls this "yank")  
\- \`M-y\`: Cycle through previous items in the kill ring (press after \`C-y\`)

\*\*Example\*\*: Let's copy and paste a line:  
1\. Move to the beginning of a line with \`C-a\`  
2\. Set mark with \`C-SPC\`  
3\. Move to end of line with \`C-e\`  
4\. Copy with \`M-w\`  
5\. Move to where you want to paste  
6\. Paste with \`C-y\`

\## Working with Buffers

Emacs can have multiple buffers open simultaneously:

\*\*Buffer Management\*\*  
\- \`C-x b\`: Switch to another buffer (prompts for buffer name)  
\- \`C-x C-b\`: List all buffers  
\- \`C-x k\`: Kill (close) a buffer

In the buffer list (\`C-x C-b\`):  
\- Navigate with \`C-n\` and \`C-p\`  
\- Press \`d\` to mark a buffer for deletion  
\- Press \`x\` to execute the marked operations

\## Working with Windows (Split Screen)

Emacs allows you to split the screen to view multiple buffers at once:

\*\*Window Commands\*\*  
\- \`C-x 2\`: Split window horizontally (one above the other)  
\- \`C-x 3\`: Split window vertically (side by side)  
\- \`C-x o\`: Move cursor to other window  
\- \`C-x 0\`: Close current window  
\- \`C-x 1\`: Close all windows except the current one

\*\*Example\*\*: View two files side by side:  
1\. Open a file with \`C-x C-f\`  
2\. Split window with \`C-x 3\`  
3\. Move to the new window with \`C-x o\`  
4\. Open another file with \`C-x C-f\`  
5\. Switch between windows with \`C-x o\`

\## Emacs Modes

Emacs uses modes to provide specialized behavior for different file types:

\*\*Major Modes\*\*  
\- Activated automatically based on file extension  
\- Provide syntax highlighting, indentation, and special commands  
\- Examples: text-mode, python-mode, c-mode, org-mode

\*\*Minor Modes\*\*  
\- Additional features that can be toggled on/off  
\- Multiple minor modes can be active simultaneously  
\- Examples: auto-fill-mode, flyspell-mode

\## Practice Exercises

1\. Create a new file named \`notes.txt\`  
2\. Type a few paragraphs of text  
3\. Practice copying and pasting sections of text  
4\. Save the file  
5\. Create a second file called \`more-notes.txt\`  
6\. Practice splitting windows and switching between your two files  
7\. Close one window, then close the remaining buffer

\## Questions to Check Understanding

1\. What key combination would you use to save your current file?  
2\. How do you select text in Emacs?  
3\. What is the difference between killing text and deleting text?  
4\. How would you split your Emacs screen to see two files side by side?  
5\. How do you switch between open buffers?

In our next lesson, we'll explore the search and replace functions, learn about the Emacs help system in more depth, and introduce basic customizations to make Emacs more comfortable for you. Ready to continue?