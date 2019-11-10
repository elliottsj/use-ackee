# use-ackee (WIP!)

[![Travis Build Status](https://travis-ci.org/electerious/use-ackee.svg?branch=master)](https://travis-ci.org/electerious/use-ackee) [![Coverage Status](https://coveralls.io/repos/github/electerious/use-ackee/badge.svg?branch=master)](https://coveralls.io/github/electerious/use-ackee?branch=master) [![Dependencies](https://david-dm.org/electerious/use-ackee.svg)](https://david-dm.org/electerious/use-ackee#info=dependencies) [![Greenkeeper badge](https://badges.greenkeeper.io/electerious/use-ackee.svg)](https://greenkeeper.io/)

Use [Ackee](https://github.com/electerious/Ackee) in React.

## Install

```
npm install use-ackee
```

or

```
yarn add use-ackee
```

## Usage

> ⚠️ Only use `use-ackee` once in your project to avoid redundant records.

Import and call `use-ackee` in a component responsible for the routing.

```js
const [ attributes ] = useAckee('/current/path', {
	server: 'https://example.com',
	domainId: 'hd11f820-68a1-11e6-8047-79c0c2d9bce0'
}, {
	ignoreLocalhost: true,
	detailed: false
})
```

Ackee will create a new record every time the `pathname` changes. An undefined or empty `pathname` will be skipped. Use `/` for the root instead.

## API

### Parameters

- `pathname` `{?String}` Current path.
- `server` `{Object}` An object that contains details about your [Ackee](https://github.com/electerious/Ackee) installation. The `server` property must not end with a slash.
- `opts` `{?Object}` An object of [Ackee options](https://github.com/electerious/ackee-tracker#options).