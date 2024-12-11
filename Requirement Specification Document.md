# Introduction
**Objective: ** The event planner App is designed to simplify event management for individuals and small temas by enabling them to create, organiise, and monitor seamlessly. It will feature tools for event creation[, participation management and communication, providing a user friendly platform to handle all aspects of event planning
**Scope: ** This app will be available on both Android and IOS Platforms, built using react native. It will leverage Firebase for backend services and intergrate third party APIs for calendar and location features.

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

