# Support Message Triage System - Interview Task

## Overview
You are tasked with building a FastAPI application for Seaside Bistro, a local seafood restaurant, to automatically process customer inquiries received through social media direct messages. The system should analyze each message, determine the appropriate action, and either respond to the customer or route to the appropriate team.

## Requirements

### Core Functionality 
1. Create a FastAPI application with the following endpoints:
   * POST `/process-message`: Accepts a customer message and returns a response or routing decision
   * GET `/messages`: Returns a history of processed messages and their outcomes
   * POST `/reservation`: Makes a reservation using the extracted details
   * GET `/reservations`: Returns all current reservations

2. Implement a ticket classification system that can:
   * Categorize messages into one of these categories:
     - General Questions (menu, hours, location, etc.)
     - Catering/Events inquiries
     - Reservation requests
     - Spam/Irrelevant (should be ignored)

3. Implement the following business logic:
   * For General Questions: Use the provided restaurant documentation to generate a helpful response
   * For Catering/Events: Route to a human (simply output a message indicating this decision)
   * For Spam/Irrelevant: Mark as such with no response needed
   * For Reservation requests: Extract reservation details and use the reservation endpoint to book it (HINT: TOOL USE/FUNCTION CALLS)


4. Store both message processing history and reservation data in a simple database