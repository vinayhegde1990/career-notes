# Getting Started

## This document helps you to setup a Staging Environment for Sphinx & Read the Docs

1. Assuming you've Python already, install Sphinx. Otherwise, please follow [steps](https://realpython.com/installing-python/) to install Python. Then do:

```bash
pip3 install sphinx sphinx-autobuild
```

2. Create a directory inside your project to hold your docs:

```bash
cd /path/to/project
mkdir docs
```

3. Run `sphinx-quickstart` in there:

```bash
cd docs
sphinx-quickstart
```

4. This walks you through creating the basic configuration; in most cases, you can just accept the defaults. When done, you'll have an *index.rst*, a *conf.py* and some other files. Add these to revision control. Now, edit your *index.rst* and add some information about your project. Include as much detail as you like. Build them to see how they look:

```
make html
```

**Note:** *You can use sphinx-autobuild to auto-reload your docs. Run sphinx-autobuild . _build/html instead.*

5. To publish only relevant code files but NOT `build`, `_static` & `_templates` directories - please add a `.gitignore` in the root directory. A sample is below

```python
#Folders to ignore
build
_templates
_static

#Extensions to ignore
*.pyc
*.diff
*.err
*.orig
*.rej
*.swo
*.swp
*.vi
*.cache
*.egg-info
*~
*#

#Logs and database files to be ignored
*.log
*.sql
*.sqlite

#OS or Editor folders
.DS_Store
Thumbs.db
.cache
.project
.settings
.tmproj
*.esproj
nbproject
*.sublime-project
```

6. Edit your files to rebuild and test, then commit your changes and push to your public repository. Once you have **Sphinx** documentation in a public repository, you can start using **Read the Docs**.
