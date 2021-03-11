# Issue Reproduction Steps
1. Run the server by running `cd server && npm install && node index.js`
1. Run the Flutter app in `app/`
1. The `HomeScreen` fetches a list of `Books` via a `WatchQuery`
1. After the list of books loads, kill the server and change the title or author of book in `index.js`
1. Reboot the server and tap the book in the list you just changed 
1. Notice the `DetailScreen` has the updated data model
1. Go back to the home screen and notice the book in the list is showing the title or author before the change


### What does work
1. Navigate to the books `DetailScreen`
1. Tap the update book title button (this makes a mutation that returns the updated object)
1. Navigate back to the `HomeScreen`
1. Notice the book is updated