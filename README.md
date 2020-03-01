# How to Install Only Desired MS Office Apps

Standard MS Office installation packages contain apps you may not want. This guide shows how to install only desired.

## Via Office Deployment Tool

* Download Office Deployment Tool from the [official Microsoft website](https://www.microsoft.com/en-us/download/details.aspx?id=49117) or the repository if the link is unavailable.
* Launch the downloaded file and extract files wherever you are comfortable. Remember the location.
* Go the location where you extracted the files. By default, there must setup.exe and three configurations files. Clone/download configuration.xml from the repository to the folder you are in.
![extracted_files]()
* Open the downloaded file with any text editor and paste the path to the folder you are in (C:\Users\username\Downloads\office_deployment_tool, for example) into the SourcePath quotes (second line (don't remove the quotes)).
![configuration]()
* ExcludeApp lines list the apps that won't be downloaded. Particularly this configuration will install just Word, PowerPoint and Excel, but you can obviously adjust them for yourself. You can also edit OfficeClientEdition, Product and Language.
* Open PowerShell/cmd with `Win + x` and go to the directory where you've done the previous steps with `cd path_to_the_directory` (cd  C:\Users\username\Downloads\office_deployment_tool, for example).
* Enter `./setup.exe /configure configuration.xml` and wait until the installation process ends.
![powershell]()
