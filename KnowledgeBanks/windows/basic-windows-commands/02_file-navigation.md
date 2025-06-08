# File & Directory Commands:

# `dir`

The `dir` command displays a list of files and subdirectories within a specified directory. It can be used with or without parameters to customize the output, such as showing hidden files, sorting by date, or displaying information in wide format.

![dir function CMD](assets/dir_cmd.png)

*CMD - `dir` screenshot showing contents of C:\Demo*

![dir function PowerShell](assets/dir_PowerShell.png)

*PowerShell - `dir` screenshot*

### Using parameters:

You can use various parameters with the dir command to modify its behavior in CMD, such as:

- `/a` to display hidden and system files, Powershell method is `dir C:\Demo -Force`
  
  ![dir /a function CMD](assets/dir-a_cmd.png)

  *CMD - `dir /a` command, showing an extra previously hidden file - hiddent_text_document.txt*

- `/s` to recursively list files and directories in subdirectories.
  
  ![dir /s function CMD](assets/dir-s_cmd.png)

  *CMD - `dir /s` command, showing contents of the directory and subdirectories.*


- `/w` to display the results in a wide format.
  
  ![dir /w function CMD](assets/dir-w_cmd.png)

  *CMD - `dir /w` command, showing all contents of C:\Demo in a wide format, sometimes required for better readability.*

- `/t` to choose which time to sidplay from, last write time `/t:w` - default, creation time `/t:c`, or last access time `/t:a`.
  
  ![dir /t function CMD](assets/dir-t_cmd.png)
  
  *CMD - `dir /t` command, showing different time displays - we can add `/O:-D` to order the list by newest first, or `/O:D` to order oldest first* 


- `/x` to display the short names of long file names. 
- `/r` to show alternate data streams (ADS).


## cd

## mkdir (md)

## ren

## copy

## move

## del 
