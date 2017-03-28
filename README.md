# react-native-AsyncStorage
React native AsyncStorage example

## Installation
Clone repo

```sh
$ git clone https://github.com/pradeep1991singh/react-native-AsyncStorage.git
```

## Run

```sh
$ cd react-native-AsyncStorage

# run ios app
$ react-native run-ios

# run android app
$ react-native run-android
```

## Saving/Retrieving Data

As AsyncStorage name suggests its an asynchronous storage which returns `Promise` object.

### Persisting data

For persisting data in react app there is `AsyncStorage.setItem` method as we have localStorage.setItem in localStorage.
`setItem` takes two parameters as key-value pair. e.g. -

```js
try {
  await AsyncStorage.setItem('@MySuperStore:key', 'hi there');
} catch (error) {
  // Error saving data
  console.log(error);
}
```

### Retrieving data

For getting saved data back there is `AsyncStorage.getItem` method which takes one parameter(key-name). e.g. - 

```js
try {
  const value = await AsyncStorage.getItem('@MySuperStore:key');
  console.log(value); // hi there
} catch (error) {
  console.log(error);
}
```

### Remove saved key

For removing Item for a key there is `AsyncStorage.removeItem` method which takes one parameter(key-name). e.g. -

```js
try {
  await AsyncStorage.removeItem('@MySuperStore:key');
} catch (error) {
  console.log(error);
}
```
