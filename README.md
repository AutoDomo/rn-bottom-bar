## 💾 Installation

Make sure you installed `react-native-safe-area-context` before installing the library : https

```
yarn add @phoenative/rn-bottom-bar
```

or

```
npm install @phoenative/rn-bottom-bar --save
```

## 📋 Requirements

- React-Navigation v6 installed : https://reactnavigation.org/

## ⚒️ Usage

```jsx
<Tab.Navigator
  screenOptions={{
    tabBarActiveTintColor: '#5F0B65',
    tabBarActiveBackgroundColor: '#5F0B65',
    tabBarInactiveBackgroundColor: 'red',
  }}
  tabBar={(props) => (
    <BottomFabBar
      mode={'square' | 'default'}
      focusedButtonStyle={{
        shadowColor: '#000',
        shadowOffset: {
          width: 0,
          height: 7,
        },
        shadowOpacity: 0.41,
        shadowRadius: 9.11,
        elevation: 14,
      }}
      bottomBarContainerStyle={{
        position: 'absolute',
        bottom: 0,
        left: 0,
        right: 0,
      }}
      {...props}
    />
  )}
>
  <Tab.Screen
    options={{
      tabBarIcon: tabBarIcon('aliwangwang-o1'),
    }}
    name="Home"
    component={generateScreen('Home')}
  />
  <Tab.Screen
    name="Meh"
    options={{ tabBarIcon: tabBarIcon('meh') }}
    component={generateScreen('Meh')}
  />
  <Tab.Screen
    options={{
      tabBarIcon: tabBarIcon('rocket1'),
      tabBarActiveBackgroundColor: '#45014A',
      tabBarActiveTintColor: 'purple',
    }}
    name="Settings"
    component={SettingsScreen}
  />
  <Tab.Screen
    options={{ tabBarIcon: tabBarIcon('Trophy') }}
    name="Trophy"
    component={generateScreen('Trophy')}
  />
  <Tab.Screen
    options={{ tabBarIcon: tabBarIcon('wallet') }}
    name="Wallet"
    component={generateScreen('Wallet')}
  />
</Tab.Navigator>
```

## 🔧 Props

| Prop         |          Type           |           Description           |
| :----------- | :---------------------: | :-----------------------------: |
| springConfig | `Animated.SpringConfig` | Spring config for the animation |

## Compatibility

✅ Support to Android, IOS and Expo.

## License

```LICENSE
MIT License

Copyright (c) 2022 Ronald Guilherme P. dos Santos

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
