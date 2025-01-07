# Expo Camera Inconsistent Barcode Scanning

This repository demonstrates a bug in Expo's Camera API where the `onBarCodeScanned` callback is not always triggered when a barcode is detected. The issue seems to be related to the reliability of barcode detection under certain conditions, such as low lighting or partial barcode visibility.

## Bug Description
The `onBarCodeScanned` callback function is intermittently failing to fire, making the barcode scanning functionality unreliable.  This can occur without any apparent errors or warnings in the console.

## How to Reproduce
1. Clone the repository.
2. Run `npm install` to install the dependencies.
3. Run the app using Expo Go or a similar method.
4. Point the camera at barcodes under varying lighting conditions and observe the inconsistent behavior of the callback.

## Solution
The solution involves adding more robust error handling and potentially implementing additional barcode detection logic (e.g., using a library like ZXing) as a fallback mechanism.
The solution file (`bugSolution.js`) provides an improved implementation.