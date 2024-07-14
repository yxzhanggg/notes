---
layout: default
---
# I/O
buffered I/O: store the data in blocks of buffers, then read/write.

unbuffered I/O: read/write data char by char (atom operation). [invokes a system call in kernel]

File descriptor:
- standard input: 0
- standard output: 1
- standard error : 2
```sh
# The program I/O is directed to 3 file descriptors by default
# Redirection: replace the file descriptor by certain file
prog < infile > outfile
# Pipe: the command still have defualt I/O, and pipe connects the I/O between files
prog1 | prog2 | prog3
```
Low level read/write:
```c
int n_read = read(int fd, char *buf, int n); // Returns byte transfered
int n_written = write(int fd, char *buf, int n);
#include <fcntl.h>
fd = int open(char *name, int flags, int perms); // Value for flags: O_RDONLY, O_WRONLY, O_RDWR...
fd = int creat(char *name, int perms);
close(int fd); // Breaks the connection between a file descriptor and an open file, 
               // and frees the file descriptor for use.
unlink(char *name); // Removes the file name from the file system
long lseek(int fd, long offset, int origin); // Sets the place that the file descriptor points to to a place in file
                                             // Sets the current position in the file whose descriptor is fd to offset, 
                                             // which is taken relative to the location specified by origin: 0, 1, 2
```
# Directory
The 'inode' for a file is where all information about the file except its name is kept.

```c
#include <dirent.h>
#define NAME_MAX 14

// Dirent structure contains the inode number and the name
typedef struct { // portable directory entry
  long ino;      // inode number
  char name[NAME_MAX+1]; // name + '\0' terminator
} Dirent;

typedef struct { // minimal DIR: no buffering, etc
  int fd;        // file descriptor for the directory
  Dirent d;      // the directory entry
} DIR;

DIR *opendir(char *dirname); // DIR is a structure analogous to FILE
Dirent *readdir(DIR *dfd);
void closedir(DIR *dfd);
```
