# LAMP Automated

Test automated LAMP setup using Vagrant &amp; Puppet

**Additional documentation to install puppet modules which will install apache and my sql**

The puppet binary has a module subcommand that will connect to the Puppet Forge to download Puppet modules and their dependencies. The commands we used will install Puppet Labs’ apache and mysql modules (and their dependencies). We’re also passing the --target-dir argument that will tell the puppet module subcommand to install the module into our shared directory (instead of Puppet’s default module path).

Install apache framework:
```puppet module install puppetlabs/apache --target-dir /puppet/modules/```


Install MYSQL framework:
```puppet module install puppetlabs/mysql --target-dir /puppet/modules/```

Do an `ls /puppet/modules/` to see that all modules are installed. You should see `apache`  `concat`  `firewall`  `mysql`  `stdli`


Though we are using `puppet module` command to install these modules, there are a multitude of other methods you can use (from downloading the modules directly out of `Github` to using a tool like `librarian-puppet`). The point is that we need to ultimately get the modules into the modules directory in our shared puppet folder
>**Disclaimer**: This is a personal repository. All code, views or opinions, and any other content represented here are personal and belong solely to me and do not represent those of people, institutions or organizations that I may or may not be associated with in professional or personal capacity, unless explicitly stated.<br>
<br>*Also **please note**, resources deployed using these example scripts do incur charges. Make sure to terminate the deployed resources/services after your tests, to save/minimize your bills*
