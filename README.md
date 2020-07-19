# Today I Learned (There are no dumb questions)
Notes I've made from stuff I've learned. This project contains the small things I've learned throughout my career that I would like to share.

I'm trying to make it more of a habit to write things here even if it's not relevant to code. 

Inspired by @charliegerard's [repo](https://github.com/charliegerard/dev-notes)

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

## Front End Applications

Server Side Rendering (SSR)

1. Server sends HTML.
2. Server renders HTML, compiles JS.
3. Browser renders HTML and JS.
4. Page can be used.
   - Compiles and renders JS scripts on the Server.
     - Pages are static.
     - Links and urls redirecting to other server pages are pre-populated by the static page.
   - Faster page loading if rendering frameworks (React, Vue).

Client Side Rendering (CSR)

1. Server sends HTML.
2. Server renders HTML, sends JS.
3. Browser renders HTML and compiles JS.
4. Page can be used after scripts compile.
   - Compiles and renders JS script on Client (their machine)
      - Pages are dynamic.
        - Links and urls redirecting to other server pages are reloaded every time you leave the page.
   - Slower page loading if rendering frameworks (React, Vue) unless you have a fast machine.

[SSR/CSR Resource](https://stackoverflow.com/questions/27290354/reactjs-server-side-rendering-vs-client-side-rendering)

- Single Page Application (SPA)
  - Uses Server Side Rendering.
  - Avoids interruption of the user experience between successive pages.
  - [Single Page Applications according to Wikipedia](https://en.wikipedia.org/wiki/Single-page_application)

- [Webpack](https://github.com/webpack/webpack)
  - Builds (compiles all the Javascript Project Code) to be used in a browser.

## Ngrok

- Multi-platform tunnelling, reverse proxy software that establishes secure tunnels from a public endpoint such as internet to a locally running network service while capturing all traffic for detailed inspection and replay.

## My Local Environment

### iTerm2

- An alternative to default Terminal but includes more features of its own.  
- Can run ZSH, Bash, and other shells in it.

### Oh-My-Zsh

- A plugin that runs on top of ZSH and provides themes and features.

### Installing a Theme

- Open .zshrc  

```bash
$ open ~/.zshrc
```

## Resources

[iTerm2 + Oh My Zsh + Solarized color scheme + Meslo powerline font + Powerlevel9k]
(#<https://gist.github.com/kevin-smets/8568070>)

## Ruby

### Rails

- Run ```bundle install``` to install ruby gems and keep branches from using inconsistent gem versions.
- Run ```rake db:migrate``` to migrate the database before you begin working.
  - This migrates all ActiveRecord database transformation when creating new ActiveRecord models.
  - Prevents merging unrecorded transformations to database schemas.

- Filter Method
  - before_action :method_name
    - Used to halt a request cycle to a controller until the action is run.

- API Versioning
  - [Deep Dive Resource](https://medium.com/swlh/a-deeper-dive-into-api-versioning-938b0cb58765)
  
#### Active Record

#### Shopify

- shop = Shop.find(-shop number-)
- shop.feature_ids = [-feature number-]

## Javascript

- State
  - Immutable
  - Stores data in the current page in controller-view
- Props
  - Mutable
  - Pass data and event handlers down to child class components

### React

- Three Tenets of Components
  - Component Nesting
    > A component can be shown inside of another

  - Component Reusability
    > Components that can be easily reused through an application

  - Component Configuration
    > Configure a component when it is created

- Rules of Class Components
  - Must be a Javascript Class
  - Must extend (subclass) React.Component
  - Must define a 'render' method that returns some amount of JSX

- Rules of State
  - Only usable with class components
  - 'State' is a JS object that contains data relevant to a component
  - Updating 'state' on a component causes the component to (almost) instantly rerender
  - State must be initialized when a component is created

- Component Lifecycle
  - Constructor
    > Initialize local state
  - Render
    > Content visible on screen
  - ComponentDidMount
    > Sit and wait for updates
  - ComponentDidUpdate
    > Sit and wait until this component is no longer shown
  - ComponentWillUnmount

- Hooks
  > Lets you use(State) instead of creating a class to access State.
  > Lets you add React state to function(al) components
  - useState
  > This is function provided by React that lets you "hook" into React features in Function Components.
  > It can take a primitive variable as simple as a string or a set of objects.

    ```javascript
    > ex: const [currentItem, setCurrentItem] = useState();
    > ex: const [items, setItems] = useState([
        {id: 1, item: "hammer"},
        {id: 2, item: "screwdriver"},
        {id: 3, item: "pliers"},
        {id: 4, item: "wrench"}
      ]);
    ```

- Syntax
  - Property Spread Notation

### RSpec

- A Ruby testing framework
- Use it to test your applications

```ruby
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

### Creating a Repository

- Initialize a local directory as a Git repository

```git
git init
```

- Add the files in your new local repository

```git
git add .
```

- Commit your files you staged for commit

```git
git commit -m "First commit"
```

#### Cloning a Repository

- Navigate to the main page of the repository
- Click clone or download
- Copy the URL
- Open Terminal and paste the URL in the path listed below

```git
git clone --- insert the URL here ---
```

## Redis

- Is used to queue jobs that fail when a response returns an error
- How to install Redis
- Download redis to your source directory
- In your shell

```bash
$ brew install redis
To run redis
$ redis-server
```

### General

## Stuff to add about things/projects you've worked on

## Heroku

- Logging history is important to trace compiling errors

## CSS

- The .class selector selects elements with a specific class attribute.
- To select elements with a specific class, write a period (.) character, followed by the name of the class.

### SASS

- Compass is built ontop of SASS
- We can write maintainable code faster
- Provides variables and functions to reuse properties
