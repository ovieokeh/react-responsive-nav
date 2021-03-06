# React Navbar

> A responsive react navbar component

[![NPM](https://img.shields.io/npm/v/react-navbar.svg)](https://www.npmjs.com/package/react-navbar) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

This is a simple, extensible Navbar component for React. I built this because I realised that I kept creating navbars from scratch on every project.

It is responsive and the navbar items collapse into a hamburger menu on mobile.

## Install

```bash
npm install --save @ovieokeh/react-navbar
```

## Available Props

You can customise the look and content of the navbar by passing in the following props:

#### Navbar Props

| name               | type        | default value | isRequired |
| ------------------ | ----------- | ------------- | ---------- |
| className          | string      |               | false      |
| menuClassName      | string      |               | false      |
| brand              | JSX.Element |               | true       |
| leftLinks          | JSX.Element |               | false      |
| rightLinks         | JSX.Element |               | false      |
| theme              | ThemeProps  |               | false      |
| shouldHideOnScroll | boolean     | true          | false      |
| shouldAnimate      | boolean     | true          | false      |

If you pass in a `className` prop, you can style this class in your custom css to customize the look and feel of the navbar even more.

#### ThemeProps

| prop            | type   | default value |
| --------------- | ------ | ------------- |
| mainColor       | string | "#333333"     |
| backgroundColor | string | "#ffffff"     |
| menuBgColor     | string | "#ffffff"     |
| height          | string | "55px"        |
| sliderWidth     | string | "100%"        |

## Usage

Play with a

- [live CodeSandbox here (JS)](https://codesandbox.io/s/react-navbar-demo-48g1c)
- [live codeSandbox here (TS)](https://codesandbox.io/s/react-navbar-demo--typescript-gm15y)

```tsx
import * as React from 'react'
import Navbar from '@ovie/react-navbar'

const navTheme = {
  mainColor: '#52b788',
  menuBgColor: '#edf7f3'
}

const navBrand = <a href={ROUTES.HOME}>Base Corp.</a>

const leftLinks = (
  <>
    <a href={ROUTES.PLANS}>Our Plans</a>
    <a href={ROUTES.FAQ}>How It Works</a>
    <a href={ROUTES.MENU}>Our Menus</a>
  </>
)

const rightLinks = (
  <>
    <a href={ROUTES.SIGNUP}>Get Started</a>
    <a href={ROUTES.SIGNIN}>Sign In</a>
  </>
)

const Example = () => {
  return (
    <div className="app">
      <Navbar
        className="navbar" // style .navbar in your css
        menuClassName="navbar--menu" // style .navbar--menu in your css
        brand={navBrand}
        theme={navTheme}
        leftLinks={leftLinks}
        rightLinks={rightLinks}
      />
    </div>
  )
}
```

![Example](example-demo.gif)

## License

Apache-2.0 © [Ovie Okeh](https://github.com/ovieokeh)
