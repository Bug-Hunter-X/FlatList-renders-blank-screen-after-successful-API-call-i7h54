# React Native FlatList Blank Screen Bug

This repository demonstrates a common bug in React Native where a FlatList component renders a blank screen even after successfully fetching data from an API.  The issue is caused by incorrect handling of the data update within the component's lifecycle.

## Bug Description
The `MyComponent` fetches data from a remote API. The API call completes successfully, but the FlatList remains blank.  No errors are logged to the console.

## Solution
The solution involves ensuring the `keyExtractor` function properly generates unique keys for each item in the data array. In this case, we initially used the index but changed it to use a unique field from the data (item.id).  Improper key extraction can lead to inconsistent rendering.

## How to reproduce
1. Clone the repo
2. Run `npm install`
3. Run `npx react-native run-android` or `npx react-native run-ios`

## Related Issues
* [React Native documentation on FlatList](https://reactnative.dev/docs/flatlist)