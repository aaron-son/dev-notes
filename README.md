# dev-notes
Notes I've made from stuff I've learned.

## Categories
- [Ruby](#Ruby)
- [Javascript](#javascript)
- [Python](#python)
- [Java](#java)
- [CSS](#css)
- [GIT](#git)
- [HTML](#html)
- [NPM / Yarn](#npm-yarn)
- [Terminal](#terminal)
- [AWS](#aws)
- [Other](#other)

## Ruby

### Rails

- Make sure to migrate the database before you begin working
```
rake db:migrate
```

## Git

#### Creating a Repository
- Initialize a local directory as a Git repository
```
$ git init
```
- Add the files in your new local repository
```
$ git add .
```
- Commit your files you staged for commit
```
$ git commit -m "First commit"
```
#### Cloning a Repository
- Navigate to the main page of the repository
- Click clone or download
- Copy the URL
- Open Terminal and paste the URL in the path listed below
```
$ git clone *** insert the URL here ***
```

## Redis
- How to install Redis
- Download redis to your source directory
- In your shell
```
$ brew install redis
To run redis
$ redis-server
```

### General

## CSS

- The .class selector selects elements with a specific class attribute.
- To select elements with a specific class, write a period (.) character, followed by the name of the class.


#### SASS
- Compass is built ontop of SASS
- We can write maintainable code faster
- Provides variables and functions to reuse properties
