# Disco tool

GOALS:
- expose the tool through command line interface
- create files and project to accelerate development and focus more on tasks to do.
- tool must be easy to use: not too much option
- *optional: -help option -verbose options*


## Bash file
** new bash_file myfile /path/to/myfile -d "This is my bash script description" **

Create a template (header) of a **bash**
Header composed of: 
- Date, Time
- Author
- Contact information: email
- name of the file
- description

## Project
** new project name /path/to/myproject **

Create a directory standardize structure for all my project:
.
|_ src
|_ bin
|_ dependencies
|_ ...

Features:
- Dependencies management. Goal is that all dependencies for a specific project can be saved and setup easily on another setup
  - packet management (apt-get)
  - configuration, all changes to a configuration file (~/.) must be saved and the tool need to provide easy way of applying them to new setup

