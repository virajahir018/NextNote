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

   # Aur uske andar Redux ka data rahega. :

       "root" tum koi aur naam bhi rakh sakte ho:
    
       key: "myntra"
       
       Phir Local Storage me key hogi:
       
       persist:myntra
       
       Lekin generally "root" hi use kiya jata hai.
       
       storage
       storage
       
       Ye batata hai data kahan store hoga.

# Who created React?
     React was created by Jordan Walke at              Facebook (now Meta).
 React को Jordan Walke ने बनाया और इसे             Facebook ने विकसित किया।


 ==========================================================================

 # What is a Props ?

     English:
     Props (Properties) are used to pass data from a Parent Component to a Child Component.
   
    Hindi:
    Props ka use Parent Component se Child Component ko data bhejne ke liye hota hai.

    # Parent data bhejta hai :
    Child sirf receive karta hai.
    
    # Destructuring :
    Props ko baar baar likhne ki zarurat nahi.

    Props kisi bhi type ke ho sakte hain

# What is a State ?

    English:
    State stores data that can change over time.
    
    Hindi:
    State wo data hota hai jo application chalne ke dauran 
    change ho sakta hai.
    
    Example
    
    Counter
    Like Button
    Cart
    Dark Mode
    Login
    
    Ye sab state hain.

    count

    Current value.
    
    setCount
    
    Value change karta hai.


#   Props          vs                    State
    Parent se aata hai	            Component ke andar hota hai
    Read-only	                     Change ho sakta hai
    Child change nahi kar sakta	   setState (setCount, setUser, etc.) se change hota hai
    Parent control karta hai	      Component khud control karta hai


# What is a Hook ?
   
    English:
    Hooks allow you to use React features (like state and lifecycle) 
    inside functional components.
    
    Hindi:
    Hooks ki madad se hum Functional Components me State, 
    Side Effects aur doosre React features use kar sakte hain. 

    1. useState :
       Component ke andar data store aur update karna.

    2. useEffect :
       Component render hone ke baad koi kaam karna.

       Empty Dependency Array [] :
          Sirf first render par chalega.

       Dependency [count] :
          Sirf count change hone par chalega.

    3. useRef :
       DOM ko access karna
       Value ko re-render ke bina store karna

       kisi value ko remember rakhta hai bina component ko dobara render kiye.

       Button click karne par :
        Cursor input me aa jayega.

    4. useContext Hook :
       useContext ek React Hook hai jo data ko ek component se dusre component 
       tak bina props pass kiye share karne ke liye use hota hai.

       Isse Prop Drilling ki problem solve hoti hai.

    5. useMemo :
       ek React Hook hai jo expensive calculation ka result memory me save (memoize) karta hai, 
       taaki har render par dobara calculation na ho.

       Dependency badlegi tabhi naya result banega.

    6. useCallback Hook :
       ek React Hook hai jo function ko memory me save (memoize) karta hai, 
       taaki har render par naya function create na ho. 

# Attach Css :
    External CSS
    Inline CSS
    CSS Modules

# Image Attach :

    1. public Folder :
       public folder ki files browser directly access kar sakta hai.

    2. src/assets :
       src/assets ki files React project ka hissa hoti hain aur bundle me include hoti hain.

    3. Image from URL (Online Image) 
   

# What is Routing ?
    English :
    Routing is the process of navigating between different pages in a React application without reloading the entire page.
    
    Hindi :
    Routing ka matlab hai application ke alag-alag pages ke beech bina page reload kiye switch karna.

     Step 1: BrowserRouter :
       React app ko BrowserRouter ke andar wrap karte hain.

       BrowserRouter routing ko enable karta hai.

     Navigation :
       Page change karne ke liye <Link> use karte hain.

     Dynamic Routing :
       <Route path="/product/:id" element={<Product />} />