# ReactNative-ReactNativeWebDemo

A step by step guide on creating a new React Native Web App on macOS using expo (Web/Android/iOS - Single Code Base)

## Steps to Create project:

1. Run the following commands in terminal:

- Create a new project named ReactNativeWebDemo: `npx create-expo-app ReactNativeWebDemo`
- Change directory to project folder `cd ReactNativeWebDemo`
- install required dependencies: `npx expo install react-dom react-native-web @expo/webpack-config`

2. Update App.js file with new code:

```
import React from 'react';
import {
StyleSheet,
Text,
View,
useWindowDimensions,
} from 'react-native';

export default function App() {
const {height} = useWindowDimensions();

return (
  <View style={[styles.container, {height}, StyleSheet.absoluteFill]}>
    <Text>Hello from React Native</Text>
  </View>
);
}

const styles = StyleSheet.create({
container: {
  flex: 1,
  backgroundColor: '#fff',
  alignItems: 'center',
  justifyContent: 'center',
}
});
```
3. Run your project from project directory: ```npm run web```
   - View the menu for options (press i for launching iOS simulator, a for launching Android simulatot, w for launching web app)
