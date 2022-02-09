# Disco tool

GOALS:
- expose the tool through command line interface
- create files and project to accelerate development and focus more on tasks to do.
- tool must be easy to use: not too much option
- *optional: -help option -verbose options*


## Bash file
**disco new bash_file myfile /path/to/myfile -d "This is my bash script description"**
what it does: 
- Create file
- Make it executable
- Create a template (header) of a **bash**
Header composed of: 
  - Date, Time
  - Author
  - Contact information: email
  - name of the file
  - description

## Project
 **disco new project name /path/to/myproject**
GOALS:
- Dependencies management. Goal is that all dependencies for a specific project can be saved and setup easily on another setup
  - packet management (apt-get)
  - configuration, all changes to a configuration file (~/.) must be saved and the tool need to provide easy way of applying them to new setup
- Create a directory standardize structure for all my project:
.
|_ src
|_ bin
|_ dependencies
|_ ...

### IDEAS
*Dependencies*

1) Manual implementation: disco add dependencies
-  Save in project folder a disco configuration file which will list all dependencies for project.
- Expose a feature "disco add dependencie project_name, which will save it to disco conf file
2) Automatic:
- Each time packet manager is called during project development, save history in disco conf file
3) All .deb file installed with packet manager are stored in /var/cache/apt/archives. An implementation could be to save all those files in a package repo at the end of each working sessions.
[more on this here](https://askubuntu.com/questions/408608/saving-a-apt-get-file-for-future-installations-how-do-i-do-it)

*Configurations*
- Each time a conf file in home directoy is modify, trigger a cron job that save the diff changes in disco conf file

1) 
## TODO
- Add descrription as an optinal arg to cmd: disco new bash . -d "Descriptions"
