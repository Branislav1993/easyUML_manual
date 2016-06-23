#Publishing a plugin in Plugin Portal Update Center

Plugins that satisfy minimal [Quality Criteria](http://wiki.netbeans.org/PluginPortalQualityCriteria) and also meet basic [Update Center Requirements](http://wiki.netbeans.org/FaqPluginRequirements) can get to the official NetBeans Plugin Portal Update Center (PPUC).

> To be able to publish a plugin on PPUC, plugin must be **verified**.

##Procedure how to start verification process:

1.	Make sure that plugin satisfies [Update Center Requirements](http://wiki.netbeans.org/FaqPluginRequirements) and also meets [Quality Criteria](http://wiki.netbeans.org/PluginPortalQualityCriteria)
2.	[Login](https://netbeans.org/people/login) to netbeans.org website and go to the [NetBeans Plugin Portal](http://plugins.netbeans.org/PluginPortal)
3.	Click **My Plugins** link from the user navigation toolbar
4.	Click the plugin to be verified
5.	Under **Verifications** for NetBeans versions section select the **NetBeans IDE version** that you want the plugin verified for
6.	Click request Verification button

More details can be found [HERE](http://wiki.netbeans.org/FaqPluginVerificationRequest).

##Requirements for verification process:

If you want to get plugin to the NetBeans [Plugin Portal Update Center](http://wiki.netbeans.org/FaqPluginUpdateCenter), plugin must successfully pass verification process. In order to ask for such verification, the plugin must satisfy the following requirements:

###1. The plugin has author

To make sure plugin has a non-empty author, **right click the project node** in the Explorer view and invoke **Properties** from its popup menu. Select **Build > Packaging** category and write your name to **Author** textfield. This will assure that module descriptor of plugin ```(/Info/info.xml)``` will contain ```<module moduleauthor="Your Name"``` attribute.

**Current value:** Open Source Software Development Center, Faculty of Organizational Sciences, University of Belgrade


###2. The plugin has description

To provide at least short description of the plugin, **right click the project node** in the Explorer view and invoke **Properties** from its popup menu. Select **Display** category and write few words about plugin to **Short Description** textfield. This will assure that module descriptor of plugin``` (/Info/info.xml)``` will contain ```<module ...><manifest OpenIDE-Module-Short-Description="easyUML is simple, easy to use NetBeans UML Plugin"``` attribute.

**Current values**

 **Display Name:** easyUml
 
 **Display Category:** UML
 
 **Short Description:** easyUML is simple, easy to use NetBeans UML Plugin
 
 **Long Description:** easyUML provides UML drawing features, code generation and creation of UML class diagrams from Java code. It is being developed at Open Source Software Development Center at Faculty of Organizational Sciences, University of Belgrade.

###3. The plugin has license

Plugin must bundle its license. In order to do this, create a text file with license terms e.g. My own license and invoke **Properties** action on **plugin's project node**. Select **Build > Packaging** category and click **Browse** button to navigate to **license file**. This will assure that module descriptor of plugin ```(/Info/info.xml)``` will contain ```<module license="..."><license name="...">My own license</license>``` non-default license.

**Current Licence location:** LICENSE-2.0.txt 

> Apache License - Version 2.0, January 2004

###4. The plugin is signed

Finally, plugin **must** be signed. Plugin Portal considers your NBM signed if it finds ```/META-INF/<your_signature>.DSA``` (or ```/META-INF/<your_signature>.RSA```) and ```/META-INF/<your_signature>.SF``` files in it.

####Signing steps:

1.	Create a keystore with **genkey** task.
2.	Using the defined module list (```${modules}``` this is defined by the IDE itself) go to all your modules and add the **keystore location** and **alias information** in its ```nbproject/private/platform-private.properties``` file.
3.	Call Netbeans **build** task so everything keeps going.

Detailed information can be found [HERE](http://wiki.netbeans.org/DevFaqSignNbm#Isn.27t_there_an_easier_way.3F).

##Changing the version of the module

To change the version of the module, **right click the project node** in the Explorer view and invoke **Properties** from its popup menu. Select **API versioning** category and change **Specification version** to desired value.

