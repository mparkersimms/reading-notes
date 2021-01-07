# Notes on a Coders Computer

#### Table of Contents
* [README](README.md)
* [Growth Mindset](Growth-Mindset.md)
* [Markdown](markdown.md)
* [Coders Computer](coders-computer.md)
* [Git-Tutorial](Git_Tutorial.md)
* [Structure web pages](Structure_webpages.md)
* [CSS](CSS.md)


Reference 

["Choosing a Text Editor"](https://codefellows.github.io/code-102-guide/curriculum/class-02/Choosing-A-Text-Editor--The-Older-Coder.pdf) by The Older Coder

["Linux tutorial"](https://ryanstutorials.net/linuxtutorial/commandline.php) by Ryan Chadwick
 
## What is a text editor
* a piece of software to allow you to write and manage text
* designed especially for text used to build a website
* some of the most important features
  * Code completion
  * syntax highlighting
  * variety of themes
  * selection of extensions available
  
### Code Completion
* allows you to start typing and the *code completion* will display possible suggestions based on what was originally typed
  * saves time by allowing choice 
  * eliminates possible typos
  * closing brackets when opened etc. 
* short hand language called *Emmet*
  * can be downloaded or may already be installed in the program you use
 
### Syntax Highlighting
* Colorizes text
* attributes different color than elements, and elements are a different color than copy

### Themes
* *helps reduce eye strain*
* Change the color of the background
* change the color of the text

### Extensions
* like plugins for your text editor

### Programs already on your computer
* definitely possible to use to create website, but limited in possibilities 
* *MAC*
  * "Text Edit" 
* no formatting assitance

### Third party options
* NotePad++
  * free 
  * Windows only
* TextWrangler / BB Edit
  * Mac only
  *  BB edit is not free
* Visual Studio Code
  * Mac, Windows, and Linux
* Atom 
  * Mac, Windows, and Linux
* Brackets
  * Mac, Windows, and Linux
* Sublime Text
  * not free 
  
### The difference between Text editors and IDEs
* IDE (Integrated Development Environment) 
  * a text editor, a file manager, a compiler, and debugger all in one
    
## Linux Tutorial - The command Line
* Text based interface to the system
* use commands and line arguements aka *options*, outputs, error messages, prompts 

### Opening a Terminal
* MAC
  * Applications -> Utilities -> Terminal 
  * command + space
    * search "Terminal"

### The Shell, Bash
* Part of the operating system that defines how the terminal will behave and look after running commands
* most common shell is "Bash" 
  * Stands for *"Bourne again shell"*
* command "echo $SHELL" will display the type of shell you are using 
  * **echo is a command used to display messages**

## Linux Tutorial - Navigation

### Where are we?
* pwd
  * stand for *Print Working Directory*
  * tells you what your current or present working directory is " where you are" 

### What's there?
* ls
  * short for "list" 
  * tells you what's there
  * ls [option][location]
    * inside [] is optional 
      * may run the command with or without them 
 * -l 
   * *command line option*
   * (optional as stated above)
   * means "long list"
   * gives more information to the list such as 
     * whether the file is a normal file (-) or directory (d) 
     * permissions for the file or directory
     * the owner of the directory
     * group the file or directory belongs to 
     * file size
     * modification time
     * actual name
 * /etc
   * *command line argument* 
   * (optional)
   * tells the command to *not* list the current directory but instead to list the directories contents
 
 * **can combine (-l) and (/etc)** 
   * will tell the command to make a long list of the /etc
   
* touch
   * make a file
   
 * mkdir 
   * makes a folder
   
 * cp 
   * copy 
   * requires two arguments 
   * the first is what you are copying 
   * the second is what you want to name the copy as 
   
 * mv 
   * move a file 
   * two purposes 
     * *moves* and also *renames* a file
   * takes two arguments 
     * the first being what you want to move, 
     * and the second is where you want to put it, and what you want to name it
   
 * rm 
   * remove file 
   
### Paths
 * a path is a means to get to a particular file or directory on the system
 
#### Absolute and Relative Paths
 * The very top of the structure is called the **root** directory
   * denoted by a single slash (/) 
   * has subdirectories that also have subdirectories.. etc. 
 
 * absolute paths specify a location in relation to the **root directory** and *always* start with a forward slash (/) 
 * relative paths specify a location in relation to where we currently are in the system
   * do not begin with a slash
   
 * ~ (tilde) 
   * shortcut for home directory
   * if home directory is (/home/matt) then you could refer to the directory (Documents) with /home/matt/Documents or ~/Documents
 * . (dot) 
   * reference to your current directory
 * .. (dotdot) 
   * reference to parent directory
   * used to cascade up the hierarchy
   
 * cd [location] 
   * stands for *change directory* 
   * with no arguments it always takes you back to your home directory
   
 * tab completion 
   * shortcut used to fill in possible paths with whats been typed already 
   * hitting **tab** at anytime on your keyboard will invoke an autocomplete action
     * if nothing happens, there are several possibilites
     * hitting **tab** again will show you all the possibilities 
       * continue typing and hit **tab** again and it will complete the autocomplete function
       
## Linux Tutorial - More about Files 
 * **Everything is a file**
 * Extensions
   * .exe - an executable file 
   * .txt - a plain text file
   * .png, .gif, .jpg - an image
 * Linux is case sensitive, other operating systems are case insensitive
 * spaces between words count as separate files, 
   * use quotations to include multiple words as one file eg. (" Matts Photos") 
   * you can also use \ as an **escape character** such as (Matts\ Photos) 
   * *using the Tab Completion function will work to escape any spaces as well*
 * use a .(period or full stop) at the beginning of a file to make it *hidden* 
   * removing the (.) will un-hide the file
   * using (-a) as a command line option will show hidden files eg. ( ls -a) will show all hidden files in the list that omiting the (-a) would otherwise not. 
   
  * *testing how it works*


  

