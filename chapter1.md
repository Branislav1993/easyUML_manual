# Downloading and Building from Source Code

The best way for you to get the source code is to use the NetBeans IDE.

First of all, fork the [repository](https://github.com/ossdcfos/easyuml). By doing this, you will get the copy of the project on your own profile.

Second of all, you have to clone the repository you just made. You can do that in NetBeans IDE by:

1. In Menu bar, click on Team section, then Git, and clone. (Team -> Git -> Clone...)
2. Enter the address of the repository in the ```Specify Git Repository Location```. 
3. Insert the location on your computer where you want to save the project. Field for the input is ```Specify destination folder```.
4. Click ```Next```.
5. Select check-box next to the ```master``` branch.
6. Click ```Next```, and then click ```Finish```.
7. Wait for NetBeans IDE to download the source code from the remote repository. Speed will depend on your internet connection.
8. Click ```Open Project```.
9. Select check-box ```Open Required```.
10. Select UML project and click ```Open```.

Congratulations, you have cloned the remote repository by using NetBeans IDE!

Now, in ```Projects``` section, you can see all of the modules for the easyUML plugin.

11. Now, you should ```Right Click``` on UML project, it is a module suite. In the menu, select ```Build``` option. Wait a minute or two. Speed will depend on your hardware configuration. You should see **BUILD SUCCESSFUL** message in Output section.
10. To start the project, ```Right Click ```on UML project, and in the menu, select the ```Run``` option. By doing this, you will start a project, and you will see the easyUML graphical user interface.

####Alternative way to download the source code

To download the source code type in your terminal:

```bash
git clone https://github.com/ossdcfos/easyuml.git```

Also, you can download the project in the .zip format by clicking on the ```Download ZIP``` option on the [GitHub repository page](https://github.com/ossdcfos/easyuml).


> Preferable way is to use NetBeans Team option described above.

