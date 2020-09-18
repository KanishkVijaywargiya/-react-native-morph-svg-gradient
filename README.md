### -react-native-morph-svg-gradient
### Developed in React Native Expo
### To choose your gradient textures for colors use this wonderfull tool specially designed for developers & awesome designers:- https://kanishkvijaywargiya.github.io/uicolorpicker.github.io/
### To run this app use following commands:- 
    npm install 
    expo start
    
![morph_svg](https://user-images.githubusercontent.com/43451046/93579605-4ed57000-f9bc-11ea-853d-7a225cf72c02.gif)

### Libraries used are:- 
    "@expo/vector-icons": "^10.2.1",
    "flubber": "^0.4.2",
    "popmotion": "^8.7.5",
    "react-native-css-gradient": "^0.4.0",
    "react-native-svg": "12.1.0"
### Used to show the Rate Us Page for app.

### gradient colors used are:- 
    const GRADIENTS = {
      "upset": "linear-gradient(to bottom, rgb(231, 97, 97), rgb(236, 49, 49))",
      "sad": "linear-gradient(to bottom, rgb(247,152,48), rgb(231, 97, 97))",
      "neutral": "linear-gradient(to bottom, rgb(243, 189, 67), rgb(203,96,32))",
      "smile": "linear-gradient(to bottom, rgb(238,172,77), rgb(187, 230, 95))",
      "excited": "linear-gradient(to bottom, rgb(95,230,118), rgb(46, 232, 78))",
    };
### methods used are:-
    interpolatePaths = (type, index) => {
    const interpolator = interpolate(this.state.path, PATHS[type], { maxSegmentLength: 2 });
    tween({
      duration: 400,
      ease: easing.easeInOut,
      from: { i: 0, background: this.state.background },
      to: { i: 1, background: GRADIENTS[type] }
    })
      .pipe(({ i, background }) => ({ path: interpolator(i), background }))
      .start(({ path, background }) => {
        this.setState({
          path, background, type, index
        })
      })
  }

![morph_svg](https://user-images.githubusercontent.com/43451046/93579605-4ed57000-f9bc-11ea-853d-7a225cf72c02.gif)

BlaceNova Inc. [TM]
