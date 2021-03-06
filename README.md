# react-native-single-double-click

A Component Wrapper for Single and Double Click/Tap, made for React Native, works on both Android and iOS.

## Installation
* `npm install --save react-native-single-double-click`

## Usage
```js
import React, { Component } from 'react';
import {
  Text,
  View,
  Alert,
} from 'react-native';
import DoubleClick from 'react-native-single-double-click';

export default class doubleClicker extends Component {
  constructor() {
    super();

    this.handleClick = this.handleClick.bind(this);
    this.handleDoubleClick = this.handleDoubleClick.bind(this);
  }

  handleClick() {
    Alert.alert('Clicked me once');
  }

  handleDoubleClick() {
    Alert.alert('This is awesome \n Double tap succeed');
  }

  render() {
    return (
      <View style={{ flex: 1, marginTop: 50 }}>
        <Text style={{ fontSize: 20 }}>
          Welcome to React Native!
        </Text>
        <DoubleClick onClick={this.handleClick} onDoubleClick={this.handleDoubleClick}>
          <Text style={{ fontSize: 26 }}>
            Please tap me twice or once!
          </Text>
        </DoubleClick>
      </View>
    );
  }
}
```

## Props

| Property | Type | Default | Description |
| --- | --- | --- | --- |
| delay | number | 300 | (in milliseconds) How fast double click/tap be pressed (number below 200 might not worked) |
| radius | number | 20 | Radius for click/tap |
| onClick | function | () => Alert.alert('Press me once') | Execute function after single click/tap pressed |
| onDoubleClick | function | () => Alert.alert('Double Tap Succeed') | Execute function after double click/tap be pressed

## License
MIT

