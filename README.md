## Setting up and testing jekyll locally.

1. Install ruby and ruby-dev

```
$ sudo apt -y install ruby ruby-dev
```

2. Set gem paths:

```
$ echo 'export GEM_HOME=$HOME/gems' >> ~/.bashrc
$ echo 'export PATH=$HOME/gems/bin:$PATH' >> ~/.bashrc
$ source ~/.bashrc
```

3. Install bundler jekyll and rails

```
$ gem install bundler jekyll rails
```

4. Go to the directory of the webpage and initialize.

```
$ cd [path to srg-web]
$ bundle init
$ bundle add jekyll
$ bundle install
```

5. Due to the baseurl we use two different configuration files: one (\_config.yml) for github page and the other (\_config\_dev.yml) for development. The only difference between these two are the baseurl so if you change either one of the files make sure the same changes are applied to the other file as well.

6. To test the webpage locally use the \_config\_dev.yml file.

```
$ bundle exec jekyll serve --config _config_dev.yml
...
...
Server address: http://127.0.0.1:4000
...
```

7. On your local browser use the address from the output to access the page.

```
http://127.0.0.1:4000/
```

## Adding seminar information entry

* The seminar information should be added as a file in the \_seminars directory.
* The easiest way is to copy an existing file in this directory and modifying the file name and the file contents.
    * The file name should be "**YYYY-MM-DD-\[Speaker's name\].md**" where YYYY-MM-DD corresponds to the seminar date. 
    * The file contains a header (or Jekyll front matter) with multiple fields, abstract, and bio. Modify the fields and contents of the abstract and the bio. The "online" field should be filled with either YES or NO.

## Making changes to the group members

* The group member information is in the \_data directory as tsv (tab separated values) files.
* The first row of each file shows the attribute names of the members in the file.
* Add/remove/modify the information about group members following the existing tsv format.  

