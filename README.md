# Longhorn-Walk
iOS application programmed in Swift that helps incoming university students get familiar with the campus by using our app to score points when they visit pre-defined locations (inspired by pokemon go)

![Simulator Screen Shot - iPhone 14 Pro - 2022-12-04 at 13 40 01](https://user-images.githubusercontent.com/113384816/233766185-f953a0cb-a5ad-419f-aec3-aaa2c5fb60f7.png)

README file: 
Name of project: LonghornWalk
Team members: Katrina Aliashkevich, Matthew Galvez, Rayna Sevilla, Yousuf Din
Dependencies: Xcode 13.0, Swift 5 
Special Instructions: 
• Use an iPhone 14 Pro Simulator in Portrait Mode
• Install the Firebase package dependency 
• If you want to test the app without going to each location on campus uncomment the “return true” on “LocationViewController” (Line 142)


Main Features
* Login/register path with Firebase. 
* “Settings” screen. The three behaviors we implemented are:
Change Fonts, Night Mode/ Day Mode, and Mute Sound  
* Non-default fonts and colors used 


Major Elements: 
   * Core Data 
   * User Profile path using camera and photo library
   * Gesture Recognition 
   * Animation 
   * Core Location / MapKit 
   * Core Audio 
Minor Elements:
   * Segmented Control 
   * Switch
   * TextView
   * Bar Buttons
   * Table View 
   * Alerts 
   * User Defaults 


Work Distribution Table
Required Feature
	Description
	Who / Percentage worked on
	Launch Screen with Animation & Sound
	Animated logo appears on launch along with sound
	Yousuf 100%
	Login/Register Path (Firebase)
	Check the entered email and password to either log the user into their existing profile, or create a new profile with those credentials.
	Katrina 80%
Matthew 10%
Rayna 10%
	Homescreen (check date)
	- The Home Screen acts as the hub of the app where the user can see their name, score, profile picture, and status label that is derived from their score. 
- On launch the app will check for the day and compare it with the user’s last update. If there is a difference the “recently visited” locations will be refreshed and the user will be able to go to the locations again for points.
- When the user taps on a visited location, a detailVC opens up that displays the location image and name. 
	Katrina 25%
Matthew 25%
Rayna 25%
Yousuf 25%
	Logout Function 
	Logs the user out of their profile and returns to the LoginVC.
	Katrina 100%
	LocationVC
(Check Locations)
	- The LocationVC hosts 10 locations at UT Austin campus where users can visit and acquire points. 
- The “LocationVC” uses CoreLocation to determine the location of the user to determine if they are at the selected location. If the user is at the location, 25 points will be added to their score.
- The location also has a “Directions” button that will segue into a mapview where the user will get directions to the selected building.
	Matthew 70%
Yousuf 20%
Rayna 10%
	MapView and Directions
	MapView that provides directions from current location to selected location. Route line appears and textView for walking directions appears. 
	Yousuf 100%
	User() Class & Firebase Firestore
	Create a class to store all the fields of the current user in as parameters. 
This makes it easier to adjust the data inside of Firestore at the same time as the user changes it in the app. When that user logs back in with their credentials, all of their previous data is loaded back into the app.
	Katrina 100%
	User Profile VC
	View Controller displays all of the user’s information including their score, display name, email, profile picture, and status level. ViewController gets updated every frame to reflect the changes the user makes inside the app
	Katrina 100%
	Edit User Profile VC
	Lets the user edit their profile by changing their display name
	Katrina 100%
	Delete Profile Function
	Button that deletes the user’s credentials from Firebase as well as deleting all of the data connected to that user from Firestore.
	Katrina 100%
	Profile Picture Upload/Download (Firebase Storage /Firestore)
	 - The user can upload a profile picture from their photo album, or their camera. The picture then gets saved onto our Firebase Storage and the filepath gets saved in their Firebase Firestore in order to get downloaded and presented.
	Katrina 50%
Matthew 50%
	Settings
	iPhone system settings clone with switches for dark/light mode and audio on/off. Action sheet for user to select font. Course website button opens safari to bulko’s website. 
	Yousuf 100%
	User Defaults
	Settings preferences (dark/light mode, sound, and font type) stored in user defaults and persists. 
	Yousuf 100%
	Alerts
	-Alerts for when incorrect credentials are entered for login/registration
- Alerts for successful location visit and invalid location visit
- Alert for CoreData refresh due to a new day on “HomeScreenVC”
-Settings alerts for terms of service, privacy policy, and learn more. 
- Alerts on EditUserProfile to pick between camera and photo gallery for profile pic
-Alert on EditUserProfile to let the user know their changes were saved when they press save button
	Katrina 25%
Matthew 25%
Rayna 25%
Yousuf 25%
	Segmented Control
	 - Segmented control in the “LoginVC” allows for users to switch between login and sign-up mode.
	Matthew 100%
	Navigation/Bar Buttons
	Embed navigation controller and show segues. Created bar button items with images.
	Rayna 100%
	UI Design
	Initial VC layouts and overall design of app functionality 
	Yousuf 70%
Rayna 30%
	CoreData
	Passing information from Location VC to HomeScreen VC through prepare for segue to store in core data
	Rayna 100%
	TableView on Homescreen
	Table view delegates and datasource retrieved core data
	Rayna 50%
Yousuf 50%
	Gestures
	 - Swipe left and right on the “LocationVC” to select a different location.
 - Tap to dismiss the keyboard.
	Matthew 50%
Yousuf 50%
	Core Audio
	Audio plays upon launching the app and fades as the login/registration VC appears. 
	Yousuf 100%
