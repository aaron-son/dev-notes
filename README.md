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

### RSpec
- A Ruby testing framework
- Use it to test your applications
```
require 'rspec/autorun'

class Calculator
  def add(a,b)
    a+b
  end
end

describe Calculator do
  let (:calculator) {Calculator.new}

  it "adds two numbers" do
    expect(calculator.add(2,3)).to eq(5)
  end

  it "adds 2 & 2" do
    expect(calculator.add(2,2)).to eq(4)
  end
end
```

- Test Error
  Ruby level Error
- Test Failure
  Test is not passing or matching expectation


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
- Is used to queue jobs that fail when a response returns an error
- How to install Redis
- Download redis to your source directory
- In your shell
```
$ brew install redis
To run redis
$ redis-server
```

### General

## Stuff to add about things/projects you've worked on

## Heroku
- Logging history is important to trace compiling errors
-

## CSS

- The .class selector selects elements with a specific class attribute.
- To select elements with a specific class, write a period (.) character, followed by the name of the class.


#### SASS
- Compass is built ontop of SASS
- We can write maintainable code faster
- Provides variables and functions to reuse properties
