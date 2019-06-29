# Python-On-Pails(PyOP)
<img src="https://tg21.github.io/img/pyop.png" alt="PyOP_LOGO" width="300px"><br>
## You all have seen Ruby on Rails now get ready for python on pails.
#### So what is Python on Pails?
Q: Is it something like Ruby on Rails ,but in python?\
Answer :No Idea(Maybe). Never used Rails. All I can say is this program is a "framework wannabe".

##### [Visit Official Website for more Information](https://tg21.github.io)
- Python-On-Pails(PyOP) is just a simple "kind of a framework" programmed in python. It is cool and it also  eliminates the need to install apache2, xampp ,wamp or lamp on systems that already have python(Python3 to be precise) installed.
- PyOP can use python3 as the main server side language, so you won't have to rely on PHP.(Not that I think anything is wrong with you using PHP but other programmers might make jokes on you.
- PyOP can serve almost all(more than 500) mimeTypes as it should, and on plus point It can run PHP too if you want(not encouraged).

# Why Make it?
Currently most developer use flask or django as frameworks for web-development with python.\
But I found that Django has a steep learning curve, You can't just use it to build web-applications after learning python, you have to watch and read tutorials on Django too.\
same case exists with flask too. So, I wanted to make a framework anybody who has working knowledge of python could use to create Web-Apps.

# New Features!

  - Every feature is "new" feature as this is recently baked code.
  - Express links feature is now live.(add your links in /config/express.json)
  - PyOP has wildcard response enabled by default.(but hackers can exploit other vulnerabilities and this project has many).

## Changelog
- fixed a bug where python files were not being served on unix based systems.
- Added a feature to serve files from anywhere.
- Server can now process inline-python code from HTML files.
- added some new bugs to hunt later.
- made commits with "unhelpful" messages.

### Installation
PyOP requires [python3](https://www.python.org/) to run.

add your project files in www folder.\
run server.py to start the server.\
all files presnent in www folder will be served to client.


```sh
$ cd python-on-pails
$ sudo python3 server.py
```

For production environments...

```sh
do the same as above but at your own risk.
```

#### To output HTML from python file
write whatever you want to be shown on web in print() statement. 
``` python
# print files of a folder as follow
print("""
<html>
<head>
<title>Files</title>
</head>
""")
from os import listdir
print(listdir())
print("foo bar")
```

#### To output Python from HTML file
write whatever you want to be shown on web in print() statement. 
``` HTML
<html>
    <body>
        <!-- generete random numbeers in HTML as follow
            put python code within <py>...</py> block
            I encourage you to use on-liners or lambda function,
            otherwise properly indent your code (like I have done here).
            that's it now when you request this html file, its python code will be processed first.
         -->
            <h1><py> print("hello there") </py></h1>
            <p>
                <py>
                    import random
                    print("hello there<br>general kenobi "+str(random.randint(1,101)))
                </py>
            </p>
        </form>
    </body>
</html>
```

## Also, a new feature
instead of using only one folder to serve files.\
run surver.py from whichever folder you want, and that server's file will be served.
```sh
$ cd folder/with/your/project/files
$ sudo python3 ~/path_to_pyop_directory/server.py -g
```

## Additional Instructions
PyOP can run PHP too but If you wish to use that , then you you'll need to install it yourself and make sure that you can access those files from terminal.\
e.g.-In windows you add path of directories(containing the executable) to environment variables.

 \
 If you want to access GET/POST data sent by server in you python file then you'll need to import pyGet() from /helperfiles/receiver.py. and then simply call the function with variable name as argument.





### Development

Want to contribute? Great! \
If you know how and want to contribute [contact](https://tg21.github.io/about.html) me.\
Help is always welcome.

### TODOs

 - Add easy express links feature (DONE).
 - Add a GUI for to start and manage server
 - package for pypi
 - Easy TLS encryption
 - Make things like cookies and $_SERVER kind of thing available
 - find and better name and logo for this project(LOGO done and love project name so not gonna change it now).
 - Make server understand inline python code from html files (DONE).

License
----

It has none.(what is this deal with all license stuff and how do I get one?)


**Free Software Open-Source Software, yeah enjoy!**
