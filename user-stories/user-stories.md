### As a User (Guest):
As a user, I want to register, so I can create an account on the platform.

As a user, I want to log in, so I can access my profile and use the platform.

As a user, I want to search for properties, so I can find places to stay.

As a user, I want to view property details, so I can make informed decisions.

As a user, I want to book a property, so I can reserve it for specific dates.

As a user, I want to make payments for my bookings, so I can confirm my stay.

As a user, I want to leave a review after my stay, so I can share my experience with others.

As a user, I want to view my bookings, so I can manage or review my past and upcoming stays.

### As a Host:
As a host, I want to log in, so I can manage my properties and bookings.

As a host, I want to add a new property, so I can list it on the platform.

As a host, I want to edit my property, so I can update its details.

As a host, I want to manage the pricing of my property, so I can adjust it as needed.

As a host, I want to delete a property, so I can remove it from the platform.

As a host, I want to view bookings, so I can see who booked my property and when.

### As an Admin:
As an admin, I want to log in, so I can manage the backend system.

As an admin, I want to manage users, so I can approve, edit, or remove accounts.

As an admin, I want to monitor all payments, so I can ensure financial accuracy and prevent fraud.

As an admin, I want to block users, so I can handle abusive or fraudulent behavior.

As an admin, I want to view all bookings, so I can oversee platform activity.

Optional Story Relations (from diagram <<include>>, <<extend>>):
These represent relationships between use cases, not separate stories, but here’s how to understand them:

Booking includes Payment → A booking always includes a payment step.

Search Property includes View Details → Viewing property details is part of the search process.

Add Property includes Manage Pricing → A host sets pricing when adding a property.

All actions require Login first → Every action (booking, adding property, etc.) assumes the user is authenticated.