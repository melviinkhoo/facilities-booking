# Facilities Booking and Reservation with AppSheet
A web app developed using AppSheet to manage Facilities Booking and Reservation

## The introduction of AppSheet 
AppSheet is a no-code platform owned by Google. AppSheet allows us to [build powerful mobile and desktop web apps with no programming knowledge needed](https://shop.cre8tivenow.com/how-to-build-powerful-apps-with-google-appsheet/). You can even use Google Sheets as the backend database.

## The Introduction of Facilities Booking and Reservation System
The system is developed as a demo or sample of what we could do with AppSheet. The initial idea is inspired by a job posting on UpWork.
For a simple facility booking and reservation system, it must include the following:
+ Users & profile (to identify who is booking the facilities)
+ Assets (facilities like rooms and courts)
+ Sessions (The fixed period of booking)
+ Rate (price of the booked session)

From the listing of all the required features, we started to develop the Web App via AppSheet.

### Structure of the System
Before the design of the system begins, we need to identify how we are going to structure our backend database which is coming from Google Sheets.
We separated all the required data into 4 categories which represented 4 tab sheets in Google Sheets.

1. Assets (or Courts) - This record consists of the rooms/courts or assets available in the system, it will be referenced in the next sheet (Sessions).
2. Sessions - This record consists of the fixed period that the user can book together with the room/facilities rate. It will also back reference to the Assets sheet.
3. Bookings - This record contains all the booking referencing from which user booked what facilities under which sessions at which date.
4. Users - This record contains all the users' information and role.

### Logic Flow & Design Thinking
1. The user role of Admin must be able to manage users, assets, sessions, and bookings.
2. The user role of user must be able to sign up (to get information from the user) and to book facilities easily.
3. The web app must be smart enough to prevent users from booking the same facilities with the same date and sessions.

### Limitation
The developed web app currently consists of the following limitation
1. Session pricing is limited to 1 pricing per session, meaning if you need to have different pricing on the same session (in different facilities), you will need to create 2 different sessions for the same period to tie to 2 different facilities.
2. The web app does not allow different rates to be imposed on different days (such as a higher rate for Weekends), although we believe that that can be hard-coded into the system.

### Additional Features
1. The payment system via Stripe can be implemented easily and it is tested working by us.
2. We can utilize Google App Script to get the processed payments' data written back to Google Sheets for payment validation and hence automating the whole payment system.

## Screenshots

