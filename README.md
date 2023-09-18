# UberEatsClone
A food delivery app suite consisting of three apps: one for users, one for delivery drivers, and one for restaurants. The user and delivery driver apps are developed using React Native, while the restaurant app is developed using React.
# Features
The UberEatsUser app contains
1) A registration and login interface that uses AWS User Pool as the backend user database, allowing users to create their accounts and use the email associated with their accounts for password changes and recovery.
2) A restaurant list that utilizes AWS Amplify as the backend database. It allows users to browse and select restaurants from a list and then choose dishes from the restaurant's menu to place an order.
3) An order tracking system with AWS Amplify as the backend database. This system enables users to check the status of their placed orders and provides information about the distance and estimated arrival time of delivery drivers to the user's location. It also utilizes the Google Maps API to display the locations of delivery drivers, restaurants, and users on a map.
4) A user profile interface that allows users to modify their address and username while providing the option to log out of their account. This interface incorporates the Google Places Autocomplete API to automatically populate user addresses and utilizes lazy loading to reduce data consumption. All data is stored in AWS Amplify.

The UberEatsDriver app contains
1) A registration and login interface that allows users to log in as delivery drivers using accounts registered within the UberEatsUser system.
2) A large map and order list that retrieves order information from AWS Amplify and uses a pubsub system to update information in real-time. It will only display orders with a status of "cooked" and within a certain distance from the delivery driver. The interface will also show the total distance, tip amount, and estimated travel time based on the chosen mode of transportation. The map is provided by Google Maps and will display the locations of all orders.
3) A order delivery system that, when a delivery driver accepts an order, uses the react-native-maps-directions library to display the route from the current location to the restaurant, along with the remaining distance and estimated time of arrival. When the delivery driver is within 100 meters of the restaurant, the order status can be switched to "PICKED_UP," and the route to the customer's address can be displayed. Once the driver is within 100 meters of the customer's location, the order can be marked as completed.
4) A user settings interface that allows users to modify their chosen mode of transportation (bicycle or car) and provides the option to log out of their account.

The UberEatsDashboard app contains
1) An interface that displays the orders received by restaurant. Restaurant can click on an order to view its details and choose whether to accept it. After accepting an order, the restaurant can indicate whether the dishes are ready. If the dishes are marked as ready, the order will be visible to delivery drivers for delivery. All orders are sorted by time.
2) A restaurant menu management interface that allows users to add new dishes to the menu and select existing dishes for removal.
3) A settings menu that enables users to modify the restaurant's name, address, images, and other detailed information. It incorporates validator functionality to verify if the provided information meets the required criteria. Additionally, users have the option to log out of their account.
# How to use
1. Install React and React Native on your computer
2. Open the folder of the software you want to launch using the terminal e.g. '/Desktop/UberEatsUser'
3. Install npm on your computer and run 'npm install'
4. Run 'npm start'
5. If you want to run the mobile application, please download Expo Go on your mobile device and scan the QR code displayed in the terminal to launch the program.













