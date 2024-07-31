# Final_Kiranpreet Chat Application

## Project Description

**The project name:** Final_Kiranpreet Chat Application

**Description:**  
The goal of this project is to create a chat program that will help one client and one server communicate with one another. Using Java sockets, it facilitates user private messaging. Secure, real-time message transmission is guaranteed by the server, which also handles client connections.

**Revision History:**

| Date     | Comment                                 | Author          |
|----------|-----------------------------------------|------------------|
| [Date]   | Initial document creation                | Kiranpreet Kaur  |

## Overview

**Purpose:**  
This module focuses on the functionalities of both the client and server components of the chat application, including and private messaging. It is intended for users who need a secure platform for one-to-one communication and for developers implementing the system.

**Scope:**  
- **Client:** User interface for registration, login, and private messaging.
- **Server:** Handles the single client connection, manages messaging, and ensures secure communication.

## Requirements

### Functional Requirements

| Requirement ID | Description                                                         |
|----------------|---------------------------------------------------------------------|
| R1             | The client shall enable users to send and receive messages privately. |
| R2            | The server shall handle the client connection and manage message routing. |
| R3            | The server shall ensure secure transmission of messages between the client and server. |

### Non-Functional Requirements

| Requirement | Description                                                        |
|-------------|--------------------------------------------------------------------|
| Performance  | The server shall efficiently handle a single client connection without performance issues. |
| Reliability  | The system shall ensure reliable message delivery with minimal latency. |

### Technical Requirements

| Requirement | Description                                                        |
|-------------|--------------------------------------------------------------------|
| Hardware    | The server shall run on machines with at least 4GB of RAM and 2 CPUs. |
| Software    | Developed using Java. The client uses JavaFX for GUI, and the server utilizes Java Sockets for communication. |

### Estimates

| # | Description                            | Hrs. Est. |
|---|----------------------------------------|-----------|
| 1 | Client GUI Development                 | 25        |
| 2 | Server-side Messaging Logic            | 20        |
| 3 | Client-Server Communication             | 15        |
| 4 | User Authentication Implementation      | 15        |
| 5 | Testing and Debugging                  | 15        |
| TOTAL: |                                    | 90        |

### Traceability Matrix

| SRS Requirement | SDD Module                                 |
|-----------------|--------------------------------------------|
| Req 1           | 5.1.1 (Client Authentication), 5.2.1 (Registration & Login) |
| Req 2           | 5.2.2 (Private Messaging)                  |
| Req 3           | 6.1.1 (Server Handling Single Client)      |
| Req 4           | 6.2.1 (Secure Communication)               |

## System Architecture

**Overview:**  
The system consists of:
- **Client:** Provides the user interface for interacting with the chat application. Users can register, log in, and send/receive private messages.
- **Server:** Manages the single client connection, handles message routing, and ensures security and data integrity.

**Architectural Diagrams:**  
- **Component Diagram:** Illustrates the relationship between the client and server components.
- **Sequence Diagram:** Shows the interaction between the client and server during a messaging session.
- **Data Flow Diagram (DFD):** Depicts data flow between the client and server.
- **Deployment Diagram:** Details how the client and server components are deployed.
- **Class Diagram:** Defines the classes used in both client and server components.
- **Use Case Diagram:** Highlights user interactions with the client and server.

## Data Dictionary

**Table**

| Field | Notes | Type    |
|-------|-------|---------|
| ID    | Unique Identifier for messages and users | DECIMAL |
| NAME  | The Name in Object.Name() | VARCHAR |
| VALUE | The Value output from messages | VARCHAR |

## Data Design

### Persistent/Static Data
- **Dataset:** User data (UserID, Username, Password, Email) and message data (MessageID, SenderID, Content, Timestamp).

### Dataset

- **User**

  | Attribute | Description                 |
  |-----------|-----------------------------|
  | UserID (PK)| Primary Key for user data   |
  | Username  | User’s login name            |
  | Password  | User’s encrypted password    |
  | Email     | User’s email address         |

  - Relationships: One-to-One with Messages
  
- **Message**

  | Attribute  | Description                       |
  |------------|-----------------------------------|
  | MessageID (PK) | Primary Key for message data   |
  | SenderID (FK) | Foreign Key linking to User     |
  | Content     | Message content                   |
  | Timestamp   | Time the message was sent         |

  - Relationships: One-to-One with User

## User Interface Design

**User Interface Design Overview:**  
Screens include user registration, login, and chat interfaces. Mockups should show how users interact with the client component.

**User Interface Navigation Flow:**
- Registration → Login → Chat Interface

**Use Cases / User Function Description:**
- **Login Screen:** Users enter credentials to access the application.
- **Chat Interface:** Displays messages and allows users to send new messages in real-time.

---

Feel free to adjust the content or formatting based on your specific needs!
