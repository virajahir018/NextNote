# Redux :

  Redux = Global Memory
  Jaise mobile me Contacts save hote hain.
  Har app access kar sakta hai.
  Waise hi Redux Store me data save hota hai.
  Har component access kar sakta hai.

  Redux ek State Management Library hai.
  Iska kaam hai application ke data (state) ko ek hi jagah store karna aur kisi bhi component ko us data tak access dena.

      Component

         │

      dispatch()

         │

      Action

         │

      Reducer

         │

      Store Update

         │

      useSelector()

         │

      Component Re-render

  1. Store :

     Store matlab
     Global Data.
 
  2. Slice

     Slice matlab
     Store ka ek part.
 
  3. Reducer

     Reducer data change karta hai.

  4. Dispatch

     Dispatch matlab
     Reducer ko bolna
     "Bhai ye action chala."

  5. Selector

     Store se data nikalna.



  # Redux Toolkit (RTK) :
    
    # Redux Toolkit kya provide karta hai? :

      configureStore()
      createSlice()
      createAsyncThunk()
      Immer (state mutation ko internally handle karta hai)
      Better performance
      Less code

      # Topic	Simple Meaning :

        Redux	          -    Application ki shared state ko ek central store me manage karta hai.
        Need	          -    Shared data ko aasani se manage karna aur Prop Drilling se bachna.
        Prop Drilling	 -    Data ko beech ke kai components ke through pass karna.
        Global State	    -    Aisa state jo poori application me kahin se bhi access ho sake.
        Redux Toolkit	 -    Redux ka modern, simple aur recommended version.
        Redux Flow	    -    User Action → dispatch() → Reducer → Store Update → useSelector() → UI Update   

   # Redux Persist :

     Redux Persist Redux Store ka data browser ke storage me save karta hai. 
     Isliye page refresh karne ke baad bhi Cart aur Wishlist ka data delete nahi hota. 
     User ke products waise hi rehte hain.

     Redux Persist khud hi Redux Store ko save aur restore kar deta hai.

   # Ye code kya karta hai? :

     # 1.
     const rootReducer = combineReducers({
        cart,
        search,
        wishlist,
     });

     Saare reducers ko ek jagah combine karta hai.

# Ye redux-persist ka configuration hai. Line by line samajhte hain. :


  const persistConfig = {
    key: "root",
    storage,
  };
  persistConfig kya hai? 
  
  
  Ye ek configuration object hai jo redux-persist ko batata hai:
  
  Data kahan save karna hai.
  Kis naam se save karna hai.
  key: "root"
  key: "root"
  
  key ka matlab hai Local Storage me kis naam se data save hoga.