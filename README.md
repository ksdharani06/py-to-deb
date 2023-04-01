# Python-to-Debian-Converter

- This project is a Python script that converts a .py file to a .deb file.
-  The script was developed using Python 3.8.10 and uses the pyinstaller library to package the Python script into a single executable.
- The executable includes a simple calculator developed using the tkinter library
- The fpm utility is used to create a Debian package from the executable.


##Usage 

##### To use the script, follow these steps:      To use the script, follow these steps:    
      
	  Clone the repository to your local machine using the following command:
      
	  `$git clone <repository-url>`
 
 ##### Navigate to the directory where your Python script is located.Then Install the pyinstaller library using the following command:
      
######  1.`$pip install pyinstaller`

 ##### Package the Python script into a single executable using the following command    
 
######  2.`$pyinstaller --onefile calculator calculator.py`
----
 ##### This will create a dist folder containing the executable. Use the following commands to create a Debian package:
      
######  3.`$ls`
######  4.`$apt install ruby-full -y`
######  5.`$gem install fpm`
######  6.`$fpm -s dir -t deb -n calculator -v 1.0 -C dist calculator=/opt/calculator`
######  7.`$ls`
These comments  will create a .deb file in the parent directory.

 ##### Install the package using the following command:
 
######  8.`$dpkg -i --force-overwrite calculator_1.0_amd64.deb`

 ##### To run the calculator, use the following command:
 
######  9.`$/opt/calculator/calculator`


 #Folder and File Structure

       The project contains the following folders and files:
> calculator : This folder contains the source code for the calculator.

          >calculator.py : This file contains the code for the calculator.

>README.md : This file contains information about the project and how to use it.
		  

#Requirements

- Python 3.8.10
- pyinstaller library
- ruby-full package
- fpm utility
- tkinter library


###Credits

This project was developed by Dharani . Special thanks to the creators of the pyinstaller, fpm, and tkinter libraries for their contributions to the Python community.

