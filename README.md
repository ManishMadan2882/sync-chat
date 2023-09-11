SynChat using React Js, Firebase-v9 and Material UI with Google Login
=====================================

Live [demo](https://sync-chat-neon.vercel.app/)

## Features
### Login with Google
![image](https://github.com/ManishMadan2882/sync-chat/assets/96079232/2f0042f9-27ed-4a23-a0dc-2ba266ae0fd9)
### Connect with other users
![image](https://github.com/ManishMadan2882/sync-chat/assets/96079232/973fec55-6c15-4a99-a9c5-17375c3951aa)
### Realtime communication
![image](https://github.com/ManishMadan2882/sync-chat/assets/96079232/9c82a7f4-7888-4fc2-85ac-c7121cc30c11)


Quick Start:
------------

- ``` git clone ```
- ``` cd sync-chat ```
- Add your firebase configuration to firebase.js file on /src
- ``` npm install ```
- ``` npm start ```


Additional Configuration:
-------------------------

1. Create Firestore Database
2. On firebase console navigate to Firestore Database -> Rules -> Edit Rules 
   replace the entire code to this:




```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if request.auth != null;
    }
  }
}
```
