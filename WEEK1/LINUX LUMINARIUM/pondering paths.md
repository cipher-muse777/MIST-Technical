# The Root 

**FLAG:** pwn.college{8PrcvWq0Z8NaE8t4wOCHYpAyn1Y.QX4cTO0wCMyAzNzEzW}
when i typed in /pwn i got BOOM!!! Here is your flag.

### What i learned 
a path that starts with the root directory, is referred to as an "absolute path"

# Program and Absolute Paths

**FLAG:** pwn.college{oo019ubfUM0S-m_za-CLuVVhliH.QX1QTN0wCMyAzNzEzW}
when i typed in //challenge/run since the challenge required us to execute run which is in challenge which is in turn in / i got Correct!!!
//challenge/run is an absolute path! Here is your flag:

### What i learned
you can find the absolute path by correcting putting the order of directories with /

# Position Thy Self

**FLAG:** pwn.college{QwqnuNlY1dZhWsivMLR7jKv76_K.QX2QTN0wCMyAzNzEzW}
when i first typed in /challenge/run it showed its incorrect and that we are not currently in the /sys directory so i used cd/sys/challenge/run which in turn showed that there was no such directory so i understood i had to execute cd /sys and then input /challenge/run so i got Correct!!! /challenge/run is an absolute path, invoked from the right directory! Here is your flag:

### What i learned 
to navigate across different directories we can use cd command and that ~ shows the current path that your shell is located at

# Position Elsewhere

**FLAG:** pwn.college{AU0t6fHx45A_UnypuqOD-i9h922.QX3QTN0wCMyAzNzEzW}
when i first typed in /challenge/run it showed its incorrect and that we are not currently in the /home directory so i executed cd /home and then input /challenge/run so i got Correct!!! /challenge/run is an absolute path, invoked from the right directory! Here is your flag:

### What i learned 
to navigate across different directories we can use cd command

# Position Yet Elsewhere

**FLAG:** pwn.college{gnA3zecRGnm0OeCn3TUEI7hyuB8.QX4QTN0wCMyAzNzEzW}
when i first typed in /challenge/run it showed its incorrect and that we are not currently in the /etc/apt/sources.list.d directory so i executed cd /etc/apt/sources.list.d and then input /challenge/run so i got Correct!!! /challenge/run is an absolute path, invoked from the right directory! Here is your flag:

### What i learned 
to navigate across different directories we can use cd command and that we can navigate through different directories in a single cd command.

# Implicit Relative Paths, From /

**FLAG:** pwn.college{MSEkfdusNz3HFXBeQ3F05MCaqZM.QX5QTN0wCMyAzNzEzW}
when i first typed /challenge/run it showed it wasnt in the correct directory so i used cd / to enter that directory then i typed in challenge/run to obtain Correct!!! challenge/run is a relative path, invoked from the right directory! Here is your flag:

### What i learned 
how relative path doesnt have / in the beginning

# Explicit Relative Paths, From /
**FLAG:** pwn.college{0W5hHKJexlZpslc5j5nkbMxFaYC.QXwUTN0wCMyAzNzEzW}
when i first typed /challenge/run it was shown im not in the right directory so i inputed cd / then retried which then showed it has to be relative path so i changed to challenge/run then it was shown it has to explicitly start with '.' so i tried ./challenge/run so it showed Correct!!!./challenge/run is a relative path, invoked from the right directory! Here is your flag:

### What i learned 
how '.' refers to same directory and ./x refers to the directory 'x' in the current directory

# Implicit Relative Path
**FLAG:**pwn.college{sAfZT9CzMVsdeGsaIqqEv1L-lps.QXxUTN0wCMyAzNzEzW}
i first opened /challenge using the cd command and then tried executing run so it showed me command not found so i tried ./run so it showed me Correct!!!./run is a relative path, invoked from the right directory! Here is your flag:

### What i learned 
that Linux explicitly avoids automatically looking in the current directory when you provide a "naked" path because it could accidentally execute programs in the current directory that happened to have the same names as core system utilities

# Home Sweet Home

**FLAG:** pwn.college{0rE-MeSMFWwfh-HeT9XiQNeWu6G.QXzMDO0wCMyAzNzEzW}
i first typed in /challenge/run/~ so it showed not a file or directory then i tried /challenge/run/~/a which showed same output and then i realised its a command so it should be /challenge/run ~/a so i got; Writing the file to /home/hacker/a!
... and reading it back to you:

### what did i learned 
when we expand ~ it becomes /home/hacker and how cd  is simply cd /home/hacker


