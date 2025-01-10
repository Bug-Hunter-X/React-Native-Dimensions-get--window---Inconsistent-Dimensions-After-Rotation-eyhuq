# React Native Dimensions.get('window') Inconsistent Dimensions After Rotation

This repository demonstrates a common bug in React Native where the `Dimensions.get('window')` API returns inconsistent or incorrect screen dimensions, particularly after screen rotation or changes in device orientation.  The issue may lead to layout problems where elements are not rendered correctly or are positioned incorrectly.

## Problem

The provided `bug.js` demonstrates the use of `Dimensions.get('window')` to obtain screen dimensions.  However, upon rotation, the dimensions reported may be inaccurate or lag behind the actual screen dimensions.

## Solution

The solution is to use the `Dimensions` API in conjunction with the `Dimensions.addEventListener` to listen for changes in dimensions and re-render the component accordingly.  This ensures that the component always reflects the current screen dimensions.

The `bugSolution.js` file provides a corrected implementation.