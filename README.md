# @syahiidkamil/react-native-header-zoom-scroll

this is a lib forked from https://github.com/thanhvd152/react-native-header-zoom-scroll

Easily create ScrollView with Animation zoom header, with lots of customization



<p align="center">
<img src="https://github.com/thanhvd152/react-native-header-zoom-scroll/blob/main/demo/demo.gif?raw=true" height="500" />
</p>

# Features
* Smooth animation
* Custom background header
* Custom small header
* Transparent small header

# Setup


This library is available on npm, install it with: `npm i @syahiidkamil/react-native-header-zoom-scroll` or `yarn  add @syahiidkamil/react-native-header-zoom-scroll`.

# Usage

```javascript
import React from 'react';
import type { Node } from 'react';
import {
  SafeAreaView,
  Text,
  Image
} from 'react-native';
import ScrollZoomHeader from 'react-native-header-zoom-scroll';
import { View } from 'react-native';

const App: () => Node = () => {


  return (
    <SafeAreaView >
      <ScrollZoomHeader
        showsVerticalScrollIndicator={false}
        smallHeaderHeight={
          60
        }
        contentSmallHeader={<View style={{
          flex: 1
        }}>
          <Text style={{ color: '#fff', fontWeight: '600', marginLeft: 10 }}>CUSTOM SMALL HEADER</Text>
        </View>}
        headerComponent={
          <View>
            <Text style={{ color: '#fff', fontWeight: '600', marginLeft: 10 }}>CUSTOM  HEADER COMPONENT</Text>

          </View>
        }
        headerHeight={300}
        backgroundHeaderComponent={
          <Image
            source={{ uri: 'https://i.9mobi.vn/cf/images/2015/03/nkk/hinh-dep-12.jpg' }}
            style={{
              width: '100%',
              height: '100%'
            }}
          />
        }
      >
        <Text style={{ fontWeight: '600', marginLeft: 10 }}>CONTENT</Text>

        <View style={{
          height: 1000,
        }} />

      </ScrollZoomHeader>
    </SafeAreaView>
  );
};

export default App;

```

## Available props

| Name                           | Type             | Default                        | Description                                                                                               |
| ------------------------------ | ---------------- | ------------------------------ | --------------------------------------------------------------------------------------------------------- |
| headerComponent                | JSXAttribute     |  null                          | Component inside Header                                                                                   |
| headerHeight                  | number            | 0                              | Height of big header                                                                                      |
| backgroundHeaderComponent     | JSXAttribute.     | null                           | Background of header Image,View ...                                                                       | 
| smallHeaderHeight             | number            | 0                              | Height of small header                                                                                    |
| contentSmallHeader            | JSXAttribute      | null                           | content of small header                                                                                   |
| fadeSmallHeader               | bool              | false                          | animation fade smallHeader when scroll                                                                    |
| statusBarBackground           | string            | transparent                    | Background statusbar                                                                                      |
| statusBarCurrentHeight           | number            | 0                    | Android status bar height (StatusBar.currentHeight)                                                                                      |
| scrollViewRef           | Ref<ScrollView>            | undefined                    | Android status bar height (StatusBar.currentHeight)
                                
                                


