# meta-acrn-manifest
Xml manifest files used by project meta-acrn. (Provides a docker based build environment to bundle AGL, Celadon Android, ACRN together to a single image)

Set up the development environment

meta-acrn consist of multiple Git repositories and repo is the tool that makes it easier to work with those repositories as a whole. Create a local bin/ directory, download the repo tool to that directory, and allow the binary executable with the following commands:

$ make -p ~/bin
$ curl https://storage.googleapis.com/git-repo-downloads/repo >  ~/bin/repo
$ chmod a+x ~/bin/repo
$ export PATH=~/bin:$PATH


Download the source

Create an empty directory that will hold the meta-acrn source files and serve as the working directory. Enter the following commands to bring down the latest version of repo tool, including its most recent fixes. The URL specifies the manifest that refers various repositories used by meta-acrn, which are placed within the working directory. For now, a .repo folder is created to store the manifest and the metadata of the source repositories.

$ mkdir celadon
$ cd celadon
$ repo init -u https://github.com/liuming50/meta-acrn-manifest.git

Enter the following command to pull down the meta-acrn source tree to your working directory. The repo sync operation might take time depending on your Internet download speed.

$ repo sync
