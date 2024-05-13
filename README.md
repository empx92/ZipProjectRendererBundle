# ZipProjectRendererBundle

A Kimai 2 plugin that allows to create a separate PDF file per project for several selected projects in the export. The PDF-Files which are then packed into a zip archive that is downloaded.
This Plugin was originally created by Jens Seldes from gbs-it.de and edited to work with newer Versions of Kimai.


## Installation

Unpack the zip file into the Kimai Plugin directory, make sure the directory structure looks like this (especially the directory name 'ZipProjectRendererBundle'):


var/plugins/ 
├── ZipProjectRendererBundle
│ ├── ZipProjectRendererBundle.php.
| └ ... more files and directories follow here ... 

Move the file var/plugins/ZipProjectRendererBundle/Resources/export/default.zip.twig
to
kimai2/var/export

See also https://www.kimai.org/documentation/export.html#adding-export-templates


## Permissions

This bundle does not require any special permissions.

## Storage

This bundle stores the files to be created in the system temp directory. [PHP function sys_get_temp_dir()]
Make sure that this directory is writable for your web server. The files are automatically deleted after download.

## Usage
In the Export section you will see a new button called "zip" to export your projects seperately


