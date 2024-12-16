# Expo DocumentPicker Android Bug: Inconsistent Promise Rejection

This repository demonstrates a bug encountered when using the Expo DocumentPicker API on Android.  The issue involves inconsistent promise rejections from the API, providing vague error messages that hinder debugging.  Even with seemingly correct permission handling, the error occurs intermittently.

## Bug Description
The `DocumentPicker.getDocumentAsync()` method occasionally rejects the promise without providing a meaningful error message. This inconsistency makes it difficult to identify and resolve the root cause.  The error message often appears generic, relating to network issues or permissions despite explicit permission requests.

## Reproduction Steps
1. Run the provided `bug.js` example on an Android device or emulator.
2. Attempt to select a file using the DocumentPicker.
3. Observe that the promise sometimes rejects with a non-specific error.

## Solution
The `bugSolution.js` demonstrates a potential workaround involving improved error handling and additional logging to gain insight into the failure.  This doesn't necessarily fix the root cause of the bug in Expo DocumentPicker, but it improves error reporting to help with debugging and potentially identifying patterns in the intermittent failures.  It is also recommended to check for recent updates of Expo and DocumentPicker.