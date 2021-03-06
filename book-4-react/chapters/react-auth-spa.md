# Basic Authentication for a React SPA (NO ROUTES)

## Topics Covered / Functionality Implemented
- Google Auth Login button. Nav bar with Logout link. 

## Where to put Api Keys
- We are now exporting a simple javascript object from a javascript file that holds our apiKeys information. 
  - This file should be added as a new line to your .gitignore file: `/src/helpers/apiKeys.js`.
  - You should make an `apiKeys.js.example` file that will not be ignored.
  
## Firebase Intialization
- In our App component, within the componentDidMount lifecycle method, we are going to have our firebase intialization trigger (via helper function).
```javascript
const firebaseApp = () => {
  // check if firebase app exists.  If not create one.
  if (!firebase.apps.length) {
    firebase.initializeApp(constants.firebaseConfig);
  }
};
```

## State
- In your App component, you will add to the component's state some authentication information. It may look something like (defined directly on the App component): 
```
  state = {
    authed: false,
  };
```
- You will use the value in state for `authed` to conditionally determine which components get rendered in your App. You can access the value in state by the statement `this.state.authed`.

### How to Update State
- You will modify state by using the React.Component method, ex. `this.setState({ authed: true })`
