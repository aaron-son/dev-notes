# dev-notes
Notes I've made from stuff I've learned.

## Categories
- [My Local Environment](#Environment)
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


## Ngrok
- Multiplatform tunnelling, reverse proxy software that establishes secure tunnels from a public endpoint such as internet to a locally running network service while capturing all traffic for detailed inspection and replay.

# My Local Environment

## iTerm2
- An alternative to default Terminal but includes more features of its own.  
- Can run ZSH, Bash, and other shells in it.
### Oh-My-Zsh
- A plugin that runs on top of ZSH and provides themes and features.
### Installing a Theme
- Open .zshrc  
```
$ open ~/.zshrc
```
## Resources
[iTerm2 + Oh My Zsh + Solarized color scheme + Meslo powerline font + Powerlevel9k]
(#https://gist.github.com/kevin-smets/8568070)

## Ruby

### Rails

- Make sure to migrate the database before you begin working
```
rake db:migrate
```

## Javascript
- State
  * Immutable
  * Stores datas in the current page in controller-view
- Props
  * Mutable
  * Pass data and event handlers down to child class components
  
### React
- Three Tenets of Components
  * Component Nesting
    > A component can be show inside of another

  * Component Reusability
    > Components that can be easily reused through an application

  * Component Configuration
    > Configure a component when it is created

- Rules of Class Components
  * Must be a Javascript Class
  * Must extend (subclass) React.Component
  * Must define a 'render' method that returns some amount of JSX

- Rules of State
  * Only usable with class components
  * 'State' is a JS object that contains data relevant to a component
  * Updating 'state' on a component causes the component to (almost) instantly rerender
  * State must be initialized when a component is created

- Component Lifecycle
  * Constructor
    > Initialize local state
  * Render
    > Content visible on screen
  * ComponentDidMount
    > Sit and wait for updates
  * ComponentDidUpdate
    > Sit and wait until this component is no longer shown
  * ComponentWillUnmount

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
