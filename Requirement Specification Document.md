# Introduction
**Objective:** The event planner App is designed to simplify event management for individuals and small temas by enabling them to create, organiise, and monitor seamlessly. It will feature tools for event creation[, participation management and communication, providing a user friendly platform to handle all aspects of event planning
**Scope:** This app will be available on both Android and IOS Platforms, built using react native. It will leverage Firebase for backend services and intergrate third party APIs for calendar and location features.

# Functional Requirements
## Event Creation
- Users can create events with the following attributes:
  - Title (Mandatory)
  - Description (Optional)
  - Date and time (Mandatory)
  - Location (Oprional, with google maps intergation)
  - Event category (e.g, meeting, party, wedding)

## RSVP Management
- users can:
  - Send invitations via email or in=app notifications
  - View and Manage RSVP Statuses (e.g attending, not attending, maybe)

## Event Dashboard
- users can
  - View all events in a dashboard
  - Filter events by category

## Calendar Intergration
- Sync with external calenders
- Automatically update synced calendars when event details change

## Notifications
Push notifications for:
- Event reminders
- RSVP Updates
- Change to event details

## Authentication
- secure login and registration using firebase authentication
- Password recovery functionality

# Non-Functional Requirements
## Usability
- The app should have an intuitive and user-friendly interface
- all actions should be accessible within three taps or fewer

## Performance
- Ensure fast loading times ( <2 seconds for all major screens)
- Handle up to 200 active users without significant performance degradation

## Security
- Use HTTPS for all communications
- Store user data securely in Firebase, complying with all relevant standards

## Compatability
The app should function seamlessly on android (version 8.0 and above) and IOS (Version 12 and above)

# User Stories
**As a user, I can:**
- Create an event with relevant details so that I can keep track of my plans.
- Send invitations and track RSVPs to know who is attending.
- View a list of all my events to stay organised.
- Sync my events with my calendar so that I receive timely reminders.
- Receive notifications for changes or updates to event details.

# Assumptions and Constraints
## Assumptions:
- Users have internet access to utilise all features of the app.
- Users will allow permissions for notifications and calendar integration.

## Constraints:
Some features (e.g., calendar sync) depend on third-party APIs, which may have usage limits or require paid subscriptions for high usage.

# Stretch Features
- Group chat for event participants.
- Media sharing for uploading and viewing photos/videos of events.
- QR code-based attendee check-ins.
- Support for recurring events.
