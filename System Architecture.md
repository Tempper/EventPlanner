# Overview
The Event Planner App will use a three-tier architecture consisting of the frontend, backend, and database layers, designed in alignment with Australian IT standards and best practices to ensure compliance with local guidelines for software development. The app will leverage React Native for the frontend, Firebase for backend services, and integrate third-party APIs for calendar and location functionalities.

# Frontend

**Technology:** React Native
**Responsibilities:**
- Render the user interface (UI) for event creation, RSVP management, dashboard, and notifications.
- Handle user interactions and input validation.
- Communicate with the backend through RESTful APIs.

**Key Components:**
- **Event Creation Screen:** Form for entering event details.
- **Dashboard:** Displays the list of events (past and upcoming).
- **RSVP Management:** Allows users to track and manage attendees.
- **Calendar Integration:** View synced events.
- **Notifications:** Receive reminders and updates.

# Backend

**Technology:** Firebase Cloud Functions (optional: Node.js with Express)

**Responsibilities:**
- Handle API requests from the frontend.
- Process and store data in the database.
- Communicate with third-party APIs for calendar and location services.
- Send push notifications for event reminders and updates.

Key Endpoints:
****
**/createEvent** (POST):
- Accepts event details from the frontend and saves them in Firestore.

**/getEvents** (GET):
- Retrieves events for a specific user.

**/updateRSVP** (PATCH):
- Updates RSVP status for an event.

**/syncCalendar** (POST):
- Syncs an event with a user's external calendar.

**/sendNotifications** (POST):
- Sends reminders or updates to participants.


# Database

**Technology:** Firebase Firestore

**Responsibilities:**
- Store and manage all app-related data.
- Provide real-time updates to the frontend.

**Schema Design:
**
  **Users**
  - userId (string): Unique identifier for the user.
  - name (string): User’s name.
  - email (string): User’s email.
  - profileImage (string): URL to the user’s profile picture.
  
  **Events**
  - eventId (string): Unique identifier for the event.
  - title (string): Title of the event.
  - description (string): Details of the event.
  - date (timestamp): Date and time of the event.
  - location (string): Event location.
  - createdBy (string): userId of the event creator.

  
  **RSVPs**
  - eventId (string): Reference to the event.
  - userId (string): Reference to the user.
  - status (string): RSVP status (e.g., "Attending", "Not Attending", "Maybe").

# Third-Party Integrations

**Google Calendar API**
  - Sync events with external calendars.
  - Provide reminders and notifications.

**Google Maps API**
- Enable location selection during event creation.
- Provide navigation links for attendees.

# Communication Flow

**Frontend to Backend:**
  - The mobile app sends API requests (e.g., to create an event).

**Backend to Database:**
 - The backend processes the request and updates the database.

**Database to Frontend:**
  - Real-time updates (e.g., new RSVP statuses) are pushed to the app.
  - 
**Backend to Third-Party APIs:**
- The backend communicates with Google Calendar and Maps APIs for additional features.

# Security Considerations
- Use Firebase Authentication to secure user accounts, ensuring compliance with local data sovereignty regulations if user data is stored outside Australia.
- Implement role-based access control (RBAC) for sensitive operations.
- Ensure all communications use HTTPS, adhering to Australian cybersecurity standards such as the ACSC Essential Eight to strengthen security.
- Limit API key usage for third-party services.
