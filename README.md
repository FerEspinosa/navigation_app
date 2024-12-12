# Navigation App

## Steps:

1. **Add dependencies to Gradle:**

   [developer.android.com/jetpack/androidx/releases/navigation#kts](developer.android.com/jetpack/androidx/releases/navigation#kts)

2. **Create Navigation Resources:**

    * Inside the `resources` folder, create a new directory called `navigation`.
    * Inside the `navigation` directory, create a new navigation resource file called `navigation_graph.xml`.

3. **Add FragmentContainerView to activity_main.xml:**
   xml <androidx.fragment.app. FragmentContainerView android:id="@+id/nav_host_fragment_container" android:name="androidx. navigation. fragment. NavHostFragment"  android:layout_width= " match_ parent"  android:layout_height= " match_ parent"  app:defaultNavHost=" true"  app:navGraph="@navigation/ navigation_ graph"  />



4. **Add NavHostFragment to activity_main.xml:**

    * In the `activity_main.xml` file (Design view), search for "nav" in the Component Palette.
    * Drag and drop the `NavHostFragment` component to the layout.
    * Select `navigation_graph.xml` and click OK.
    * Infer constraints.

5. **Add Destinations to navigation_graph.xml:**

    * Click the "New Destination" button (upper left corner of the design panel).
    * Press "Create new destination".
    * Select a fragment (Blank).
    * Name it and click Finish.

6. **Create Buttons in Fragments:**

   Create buttons in each fragment and assign IDs to them.

7. **Implement Navigation in FirstFragment.java:**

    // Inflate the layout for this fragment 
    View view = inflater.inflate(R.layout. fragment_ first,  container, false);
    
    // Initialize Button 
    Button btn = view.findViewById(R. id. go2_ button) ;  
    btn.setOnClickListener( new View.OnClickListener( )  { 
    @Override public void onClick(View v) { 
    
   // Create an action to navigate to the second fragment Navigation.findNavController( v)  
       .navigate(R.id.action_ firstFragment_ to_ secondFragment) ;  } });
       return view;

8. **Repeat for SecondFragment.java:**

   Repeat the previous step for `SecondFragment.java`, 
   adjusting the button ID and navigation action accordingly.