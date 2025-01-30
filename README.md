# Silent Failure of useAsyncStorage with Large Data in Expo

This repository demonstrates a bug in Expo's `useAsyncStorage` hook where storing large JSON objects causes a silent failure. The error is not clearly reported, making debugging challenging.

## Bug Description
When attempting to store a large JSON object using `useAsyncStorage`, the operation fails without providing a clear or informative error message. This makes it difficult to identify and resolve the issue, especially in large applications.

## Reproduction
1. Clone this repository.
2. Run `npm install`.
3. Run the app using Expo Go or a similar Expo client.
4. Attempt to store a large JSON object using the `storeData` function. Observe the lack of error messages even though the operation fails.

## Solution
The solution involves splitting the data into smaller chunks and storing them separately.  This workaround addresses AsyncStorage limitations and ensures data persistence.

## Additional notes
Consider using alternative data storage solutions such as SQLite, Realm, or a cloud-based database for managing larger amounts of data in your Expo applications.  This allows for better handling of larger datasets and easier management of data.