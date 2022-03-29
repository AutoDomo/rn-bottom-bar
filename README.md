## 💾 Installation

Make sure you installed `react-native-safe-area-context` before installing the library : https

```
yarn add @phoenix/rn-bottom-bar
```

or

```
npm install @phoenix/rn-bottom-bar --save
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
