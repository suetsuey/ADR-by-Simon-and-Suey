# Architecture Decision Record (ADR)

## Introduction

### Prologue (Summary)

In the context of developing a new food ordering mobile application, we are facing the need for a robust, user-friendly, and secure platform. Therefore we decided for a native application approach, leveraging the React Native as UI framework. With a modern backend language Node.JS, we aim to achieve high performance, seamless user experience, and secure transactions.We also accept the increased development and maintenance costs associated with native app development.

### Discussion (Context)

Our team is tasked with creating a mobile app that must offer a speedy and reliable user experience, accurate location tracking, real-time order updates, secure payment processing, up-to-date menu synchronization, user review management, and efficient order history retrieval. The app should provide push notifications for order and delivery updates as well as promotional content.

The key considerations include:

- The need for a responsive and intuitive user interface that works well across different devices and operating systems.
- Ensuring the app can gain access to and use location information for delivery and restaurant suggestions.
- Real-time data updates the requires a constant and instantaneous flow of information.
- Security and privacy concerns, especially regarding payment information and user data.
- Integration complexity with third-party services like payment gateways and restaurant inventory systems.
- Data storage solutions that should offer quick access to historical data and support for user-generated content.

### Solution

The decision to go with a native app is based on the need for high performance and access to the full feature set of the underlying platform, which includes GPS for location tracking and seamless integration with push notifications. We will use React Native as our UI framework to strike a balance between performance and development efficiency. React Native offers a vast ecosystem and codes can be shared between iOS and Android platforms if needed.

For the backend, we have selected Node.js due to its scalability, it can handle user and software growth effectively. Node.js is also a widely used backend language therefore large amount of tools and support are available. It can also process data efficiently without delay, which best suits our food ordering mobile app.

Permissions will be managed according to the principles of least privilege. It means that our app are requesting location data, notifications, and payment information only when necessary.
Users are fully informed and they can easily control these permissions.

Data storage will be handled by a NoSQL database MongoDB. MongoDB offers flexibility in managing the varied data structures we expect from user accounts, order history, and restaurant menus. MongoDB stores data in a format similar to JSON, which aligns well with our backend language Node.JS. Data manipulation and transfer between client and server are much easier with MongoDB.

For additional frameworks and technology stacks, we will use:

- Socket.IO for real-time communication to power live order tracking.
- Stripe as a payment gateway API for its robust security measures.
- RESTful APIs for the integration with restaurant inventory management systems and menu synchronization.
- Firebase for managing push notifications and for additional user analytics and performance monitoring.

### Consequences (Results)

Over the long term, the decision to build a native app are expected to offer a smooth and engaging user experience, with efficient use of device capabilities and quick, responsive interfaces. The choice of React Native and Node.js allows a relatively fast development cycle.

The app are expected to successfully handles location tracking, real-time updates, and secure transactions, providing users with a reliable and convenient food ordering experience. The integration of user reviews and ratings would create a valuable feedback loop for restaurants and users.

The use of MongoDB would facilitate easy management of dynamic data structures and rapid retrieval of historical data. The notification system powered by Firebase would prove effective in keeping users informed and engaged.

Ongoing maintenance and updates are required to keep up with the native platform. In case of any security concerns that arise, immediate updates would be scheduled.
