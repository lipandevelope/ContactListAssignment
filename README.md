Tribal Scale Interview Assignment

Li Pan

Mobile Assignment:

Address book application - ability to launch an app and display contacts. Perform an API call from the http://randomuser.me/ API and display 20 users. Show what seems most applicable (eg: loading indicator, list of contacts, details of the each person, etc.)

Git Repository: https://github.com/lipandevelope/ContactListAssignment

Deployment/Running Instruction: 

•	Open GitHub Repository Link

•	Download project via “Download Zip”

•	Unzip compressed file and run TribalScaleInterviewAssignment.xcodeproj

•	When project finishes indexing, run by pressing “Play” Button on top left corner of Xcode, or by pressing Command “R”

•	Scroll TableView to access all 20 contacts,

•	Swipe left on cell to access detailed view,

Approach:

I started off the project by building the model for incoming data. Using the Master-Detail-View template thinking that it would be intuitive to have the list of contacts populate a TableView and allow users the ability to go into the contact to view details. A ContactBuilder class is created to mirror the JSON data provided by the Randomuser API with local constants as identifiers for their respective values once the data is fetched.

Using apple’s GCD library, the method to fetch data is put to a background thread, while a nested custom block updates TableView in main thread as fetch finishes. The Contact object fetched is added to an array nested in a for-loop to obtain 20 contacts.

I decided that it is better to present the DetailView from the left when users swipes left, and have it take up half the screen instead of seguing into a detailed view controller.

Some UI Elements were modified for aesthetic purposes by manipulating their layers.

If given more time, I would add abilities for users to directly access email, phone, and message features via DetailView through pressing on the corresponding pieces of contact information. I will also work on polishing the UI.

If given time to make the application more robust. I will make use of the contacts’ nationality to provide approximate distance between users. As a stretch, I would implement geo-location features to provide more precise distance between users and his/her contacts. I will also implement features where users can organize the contacts into sections and different TableViews based on the range of data provided through the API; as well as give users ability to tag and un-tag certain contacts at times for customizable purposes to provide versatility to its usage.
