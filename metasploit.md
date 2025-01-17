## Metasploit
This is a walkthrough the introduction to metasploit room. It is not a fully comprehensive room hence more reading is required. 

## Task one: Introduction 
Metasploit, an open-source pentesting framework, is a powerful tool utilized by security engineers around the world. Maintained by Rapid 7, Metasploit is a collection of not only thoroughly tested exploits but also auxiliary and post-exploitation tools. Throughout this room, we will explore the basics of using this massive framework and a few of the modules it includes. 

Kali and most other security distributions of Linux include Metasploit by default. If you are using a different distribution of Linux, verify that you have it installed or install it from the Rapid 7 Github repository. 

    Answer: No answer needed
    
## Task two: Initializing...

First things first, we need to initialize the database! Let's do that now with the command: msfdb init
If you're using the AttackBox, you don't need to do this.
    
    Answer: No answer needed
    Command: msfdb init


Before starting Metasploit, we can view some of the advanced options we can trigger for starting the console. Check these out now by using the command: msfconsole -h

    Answer: No answer needed
    Command: msfconsole -h
    
We can start the Metasploit console on the command line without showing the banner or any startup information as well. What switch do we add to msfconsole to start it without showing this information? This will include the '-'

    Answer: -q 
    This means that metasploit will start quielty without the banner(art) or info
   
Once the database is initialized, go ahead and start Metasploit via the command: msfconsole

    Answer: NO answer needed
    Command: msfconsole
   
After Metasploit has started, let's go ahead and check that we've connected to the database. Do this now with the command: db_status

    Answer: No answer needed 
    In the output make sure you are connected to a database
    
Cool! We've connected to the database, which type of database does Metasploit 5 use? 

    Answer: postgresql 
    Command: db_status
## Task three: Rock 'em to the core[commands] 
The following questions can be answered using info in the metasploit help tab.
    
    Command: ? 
    
 
Let's go ahead and start exploring the help menu. On the Metasploit prompt (where we'll be at after we start Metasploit using msfconsole), type the command: help

    Command: help(in metasploit console) 
    Answer: No answer needed
 
The help menu has a very short one-character alias, what is it?

    Answer: ? 
    ?             Help menu
   

Finding various modules we have at our disposal within Metasploit is one of the most common commands we will leverage in the framework. What is the base command we use for searching?

    Answer: search
    search        Searches module names and descriptions
    
Once we've found the module we want to leverage, what command we use to select it as the active module?

    Answer: use 
    use           Interact with a module by name or search term/index


How about if we want to view information about either a specific module or just the active one we have selected?
    
    Answer: info 
    info          Displays information about one or more modules
    
Metasploit has a built-in netcat-like function where we can make a quick connection with a host simply to verify that we can 'talk' to it. What command is this?

    Answer: connect 
    connect       Communicate with a host

Entirely one of the commands purely utilized for fun, what command displays the motd/ascii art we see when we start msfconsole (without -q flag)?

    Answer: banner
    banner        Display an awesome metasploit banner

We'll revisit these next two commands shortly, however, they're two of the most used commands within Metasploit. First, what command do we use to change the value of a variable?

    Answer: set
    set           Sets a context-specific variable to a value

Metasploit supports the use of global variables, something which is incredibly useful when you're specifically focusing on a single box. What command changes the value of a variable globally?  

    Answer: setg
    setg          Sets a global variable to a value
    
Now that we've learned how to change the value of variables, how do we view them? There are technically several answers to this question, however, I'm looking for a specific three-letter command which is used to view the value of single variables.

    Answer: get
    get           Gets the value of a context-specific variable
    

How about changing the value of a variable to null/no value?
    
    Answer: unset
    unset         Unsets one or more context-specific variables
    
When performing a penetration test it's quite common to record your screen either for further review or for providing evidence of any actions taken. This is often coupled with the collection of console output to a file as it can be incredibly useful to grep for different pieces of information output to the screen. What command can we use to set our console output to save to a file?

    Answer: spool 
    spool         Write console output into a file as well the screen
    

Leaving a Metasploit console running isn't always convenient and it can be helpful to have all of our previously set values load when starting up Metasploit. What command can we use to store the settings/active datastores from Metasploit to a settings file? This will save within your msf4 (or msf5) directory and can be undone easily by simply removing the created settings file. 

    Answer: save 
    save          Saves the active datastores

## Task four: Modules for every occassion

This section will maily focus on the various modules offered by metasploit.

Easily the most common module utilized, which module holds all of the exploit code we will use?

    Answer: Exploit

Used hand in hand with exploits, which module contains the various bits of shellcode we send to have executed following exploitation? 

    Answer: Payload
    
Which module is most commonly used in scanning and verification machines are exploitable? This is not the same as the actual exploitation of course. 
    
    Answer: Auxilliary
    
One of the most common activities after exploitation is looting and pivoting. Which module provides these capabilities?

    Answer: Post 
    
Commonly utilized in payload obfuscation, which module allows us to modify the 'appearance' of our exploit such that we may avoid signature detection?

    Answer:Encoder
    
Last but not least, which module is used with buffer overflow and ROP attacks?

    Answer: Nop 
    
Not every module is loaded in by default, what command can we use to load different modules? 

    Answer: Load
















