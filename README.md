# mark_cdp
## CLI navigation system

This navigation system allows you to mark directory paths under bash using user set keywords.
The system is written in Perl.  It needs to be installed in your user profile.
The system uses vim or an alternate editor that you configure into the code.
When you add a mark, it also creates local bash variables of the form: $M_<mark_name> which can be used 
to more easily move or copy data across different directories.

To mark the current working directory use:
   mark <mark_name>
To look at the directory of marked names do
   mark -v
(v stands for vim or vi - a popular editor)
You can add comments to the directory and it preserves them.
Ocasionally if you use odd characters you may have to directly edit the database file and fix it.

To go to a path you can do:
   cdp <mark_name>
You can also do: 
   cdp -l
in order to see a list of the last n-places (e.g. 50) you have visited in order (except repeats are removed).
Entries in the list are numbered.  You can also revisit a place you visited recently by doing:
   cdp <number>
You can edit the database of visited places with the command:
   cdp -v
You can modify it, reorder it, etc.
The cdp database is just a reminder of places you have visited.
cdp and mark are not programs, they are shell functions.
Other than this, the perl program is fairly small, easy to understand and modify.
Interesting desirable future additions to the program could be:
    drawers (e.g.) you can open marks under drawer names and close them.
    inter-computer mark/cdp to navigate paths across a network.
Want to help? that would be cool.

## INSTALLATION
To install ungzip the tar file under /usr/local/
go into the created directory.
Run install with sudo.
and follow the instructions, the program will install in /usr/local/bin/mark_dir
I reccommend you persuse the file and get acquainted with the code first.




