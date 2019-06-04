## I. Install Python3 locally

1. go to https://www.python.org/downloads/source/ and select a relatively new but not the newest release Gzipped source tarball

2. Save the tgz tarball on the server

```
wget https://www.python.org/ftp/python/3.5.7/Python-3.5.7.tgz ## change the version number accordingly
```

3. Locally install it. If you choose the latest version, and it prompts error messages that you eventually cannot solve it afer googling very hard. Try a relatively older but potentially more stable version.

```
cd /path/to/this/python/ ## go to the directory where you store the Python tarball
tar -zxvf Python-3.5.7.tgz ## unzip the tarball
mkdir /path/to/install/python3 ## create another new folder under the directory you like. This folder will be used to install Python3
cd Python-3.5.7 ## go in the unzipped Python tarball
./configure --prefix=/path/to/install/python3 ## give the path where you want to install Python3
make
make install ## now you have successfully installed the Python3
```

4. Run python3 and pip. You can do it in two ways: a. cd /path/to/install/python3/bin/ and run ./python3 ./pip3; b. export the path to the environmental variable $PATH by ```export PATH=/path/to/install/python3/bin:$PATH``` and run python3 or pip3 anywhere you like.

5. Use pip to install module.

```
python3 -m pip install moduleName ## this is a more robust way.
pip3 install moduleName ## most of time this command is good enough.
```


## II. Run a long-time job using screen

To run a long time job on the background so that you can close the terminal or shut down your computer for a while but still be able to come back and check how job is running, go for "screen"!

```
/s/std/bin/stashticket
/s/std/bin/runauth /usr/bin/screen -S nameofthescreen ##create the screen
... ## run the jobs as you do in the terminal
ctrl+A+D ## to exit the screen and leave the job running
screen -r nameofthescreen ## to reopen the screen
```
You can create multiple screens and use ```screen -r``` to check all the active screens and their name

## III. Check the server usage

```
/p/stat/genomics/bin/htop ## htop is installed at /p/stat/genomics/bin
```

## IV. Check the memory usage on the server

```
free -m
```

## V. Write scripts on the server: emacs or vim, and make it reproducible and add sufficient comments/notes

## VI. version control and backup: github.com or https://bitbucket.org.
