# Bottom drawer for React Native

## Content

- [Bottom drawer for React Native](#bottom-drawer-for-react-native)
  - [Installation](#installation)
  - [Usage Example](#usage-example)
  - [Configuration](#configuration)
    - [Questions?](#questions)

## Installation

Install `react-native-bottom-drawer`.

```
npm install react-native-bottom-drawer --save
```

## Usage Example
(go to the example folder for a more fleshed out example)

```javascript
import React from 'react';
import { View, Text } from 'react-native';
import BottomDrawer from 'react-native-bottom-drawer';

const TAB_BAR_HEIGHT = 49;

export default class App extends React.Component {
  renderContent = () => {
    return (
      <View>
        <Text>Get directions to your location</Text>
      </View>
    )
  }

  render() {
    return (
      <BottomDrawer
        containerHeight={100}
        offset={TAB_BAR_HEIGHT}
      >
        {this.renderContent()}
      </BottomDrawer>
    )
  }
}

```
This project is based on [jacklein/rn-bottom-drawer](https://github.com/jacklein/rn-bottom-drawer/) and there are few new things handled and optimized here

## Configuration

| Prop | Type | Default | Description |
| ---- | ---- | ----| ---- |
| containerHeight | number | -- | The height of the drawer. | 
| offset | number | 0 | If your app uses tab navigation or a header, **offset** equals their combined heights. In the demo gif, the offset is the header + tab heights so that the drawer renders correctly within the map view. |
| downDisplay | number | containerHeight / 1.5 | When the drawer is swiped into down position, **downDisplay** controls how far it settles below its up position. For example, if its value is 20, the drawer will settle 20 points below the up position. The default value shows 1/3 of the container (if containerHeight = 60, the default downDisplay value = 40). |
| backgroundColor | string | '#ffffff' | The background color of the drawer. |
| startUp | bool | true | If **true**, the drawer will start in up position. If **false**, it will start in down position. |
| roundedEdges | bool | true | If **true**, the top of the drawer will have rounded edges. |
| shadow | bool | true | if **true**, the top of the drawer will have a shadow. |
| onExpanded | func | -- | A callback function triggered when the drawer is swiped into up position |
| onCollapsed | func | -- | A callback function triggered when the drawer is swiped into down position |    
    

| Method  | Description |
| ---- | ---- |
| toggleDrawerState() | Open/Close drawer based on previous state   |
### Questions?
Feel free to contact me at [zadehdolatabad@gmail.com](mailto:zadehdolatabad@gmail.com) or [jackdillklein@gmail.com](mailto:jackdillklein@gmail.com) or [create an issue](https://github.com/matinzd/react-native-bottom-drawer/issues/new)   
