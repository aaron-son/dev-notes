# Today I Learned

Notes from things I've learned throughout my career. This project is a collection of small lessons and tips I want to share. Inspired by [@charliegerard's dev-notes repo](https://github.com/charliegerard/dev-notes).

I'm trying to make it a habit to write things here.

## Categories

- [My Local Environment](#my-local-environment)
- [Ruby](#ruby)
- [SQL](#sql)
- [Javascript](#javascript)
- [Python](#python)
- [Java](#java)
- [CSS](#css)
- [Git](#git)
- [HTML](#html)
- [NPM / Yarn](#npm--yarn)
- [Terminal](#terminal)
- [AWS](#aws)
- [Other](#other)

---

## My Local Environment

### Mac Setup

#### Homebrew

Install Homebrew:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

#### Oh-My-Zsh

A plugin for ZSH that provides themes and features.  
[Oh My Zsh](https://github.com/ohmyzsh/ohmyzsh)

#### iTerm2

An alternative to the default Terminal with more features.  
[iTerm2 Download](https://iterm2.com/downloads.html)

Install Oh My Zsh:

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

##### One Dark Pro iTerm Theme

- Clone:  
  `git clone https://github.com/chinhsuanwu/one-dark-pro-iterm.git`
- Or download the [.zip](https://github.com/chinhsuanwu/one-dark-pro-iterm/archive/master.zip)
- [One Dark Pro.itermcolors](https://github.com/chinhsuanwu/one-dark-pro-iterm/blob/master/One%20Dark%20Pro.itermcolors)

**Activate Theme:**  
`iTerm2` → `Preferences` → `Profiles` → `Colors` → `Color Presets` → `Import` → Select `.itermcolors` file → Choose "One Dark Pro".

##### Mac Typing Shortcuts in iTerm2

Preferences (`⌘ + ,`) → Profiles → Keys → Presets → Select "Natural Text Editing".

#### Powerlevel10k Theme

```bash
brew install powerlevel10k
echo "source $(brew --prefix)/share/powerlevel10k/powerlevel10k.zsh-theme" >>~/.zshrc
```

#### Powerline Fonts

```bash
brew install python
pip install --user powerline-status
```

### VSCode

Theme: One Dark Pro

---

## Resources

- [iTerm2 + Oh My Zsh + Solarized + Meslo Powerline + Powerlevel9k](https://gist.github.com/kevin-smets/8568070)

---

## Front End Overview

- [Babel](https://babeljs.io/): Transpiles JS to browser-friendly code.
- [Webpack](https://webpack.js.org/): Bundles files for production.

**Server Side Rendering (SSR):**
- Server sends HTML and JS, browser renders both.
- Faster initial load, static pages.

**Client Side Rendering (CSR):**
- Server sends HTML and JS, browser compiles JS.
- Dynamic pages, slower initial load.

[SSR/CSR Resource](https://stackoverflow.com/questions/27290354/reactjs-server-side-rendering-vs-client-side-rendering)

**Single Page Application (SPA):**
- Uses SSR, avoids page reloads.
- [SPA Wikipedia](https://en.wikipedia.org/wiki/Single-page_application)
- [react-router](https://github.com/rackt/react-router): Manage page changes without refresh.

---

## Ngrok

Multi-platform tunneling and reverse proxy software for secure tunnels from public endpoints to local services.

---

## Ruby

### Rails

- `bundle install`: Install gems and keep versions consistent.
- `rake db:migrate`: Migrate database before working.
- `before_action :method_name`: Filter method to halt request cycle.

**API Versioning:**  
[Deep Dive Resource](https://medium.com/swlh/a-deeper-dive-into-api-versioning-938b0cb58765)

### RSpec

Ruby testing framework.

```ruby
require 'rspec/autorun'

class Calculator
  def add(a, b)
    a + b
  end
end

RSpec.describe Calculator do
  let(:calculator) { Calculator.new }

  it "adds two numbers" do
    expect(calculator.add(2, 3)).to eq(5)
  end

  it "adds 2 & 2" do
    expect(calculator.add(2, 2)).to eq(4)
  end
end
```

- **Test Error:** Ruby-level error.
- **Test Failure:** Test does not match expectation.

#### Active Record

#### Shopify

```ruby
shop = Shop.find(shop_number)
shop.feature_ids = [feature_number]
```

---

## SQL

- MySQL
- PostgreSQL
- SQLite3

---

## Javascript

### React

- **State:** Immutable, stores data in the current page.
- **Props:** Mutable, pass data/event handlers to child components.

**Functional Component:**  
Plain JS function accepting props and returning a React element.

**Class Component:**  
JS class extending React.Component, must define `render`.

**Component Tenets:**
- Nesting
- Reusability
- Configuration

**Class Component Rules:**
- Must be a JS class
- Must extend React.Component
- Must define `render`

**State Rules:**
- Only in class components
- JS object with relevant data
- Updating state rerenders component

**Lifecycle:**
- Constructor → Render → ComponentDidMount → ComponentDidUpdate → ComponentWillUnmount

**Hooks:**  
Use state in functional components.

```javascript
const [currentItem, setCurrentItem] = useState();
const [items, setItems] = useState([
  { id: 1, item: "hammer" },
  { id: 2, item: "screwdriver" },
  { id: 3, item: "pliers" },
  { id: 4, item: "wrench" }
]);
```

**JSX:**  
Syntactic sugar for `React.createElement`.

### Redux

Predictable state mutations.

- Pass state between components
- Fetch/store API data (redux-saga, redux-thunk)
- Store forms (redux-form)

**Principles:**
- Single source of truth
- State is read-only
- Changes via pure functions (reducers)

**Pure Functions:**  
Accept input, return output, no side effects.

### Typescript

---

## Git

### Creating a Repository

```bash
git init
git add .
git commit -m "First commit"
```

### Cloning a Repository

```bash
git clone <repo-url>
```

---

## Redis

- Queue jobs that fail on error response.
- Install:

```bash
brew install redis
redis-server
```

---

## Stuff to add about things/projects you've worked on

---

## Heroku

- Logging history is important for tracing compile errors.

---

## CSS

- `.class` selector selects elements with a specific class.

### SASS

- Compass is built on top of SASS.
- Write maintainable code faster.
- Provides variables and functions for reuse.

---

## Python

`virtualenv` creates a subfolder for a Python environment using the global Python version.

