1.1 Project
The project name: Final_Kiranpreet Chat Application

1.2 Description
This project is a chat application designed to facilitate communication between a single client and a server. It supports user registration, login authentication, and private messaging using multi-threading and Java sockets. The server manages client connections and ensures secure, real-time message delivery.

1.3 Revision History

Date	Comment	Author
[Date]	Initial document creation	Kiranpreet Kaur
[Date]	Adjusted to focus on single-user messaging	Kiranpreet Kaur
Section 2 - Overview
2.1 Purpose
This module focuses on the functionalities of both the client and server components of the chat application, including user authentication and private messaging. It is intended for users who need a secure platform for one-to-one communication and for developers implementing the system.

2.2 Scope
The scope includes:

Client: User interface for registration, login, and private messaging.
Server: Handles the single client connection, manages messaging, and ensures secure communication.
2.3 Requirements

2.3.1 Functional Requirements

Requirement 1 (R1): The client shall allow users to register and log in using a username and password.
Requirement 2 (R2): The client shall enable users to send and receive messages privately.
Requirement 3 (R3): The server shall handle the client connection and manage message routing.
Requirement 4 (R4): The server shall ensure secure transmission of messages between the client and server.
2.3.2 Non-Functional Requirements

Performance: The server shall efficiently handle a single client connection without performance issues.
Reliability: The system shall ensure reliable message delivery with minimal latency.
2.3.3 Technical Requirements

Hardware: The server shall run on machines with at least 4GB of RAM and 2 CPUs.
Software: Developed using Java. The client uses JavaFX for GUI, and the server utilizes Java Sockets for communication.
2.3.4 Security Requirements

Authentication: The system shall use secure authentication methods for user logins.
Data Encryption: All messages shall be encrypted during transmission.
2.3.5 Estimates

| Description | Hrs. Est.
---|-------------|----------
1 | Client GUI Development | 25
2 | Server-side Messaging Logic | 20
3 | Client-Server Communication | 15
4 | User Authentication Implementation | 15
5 | Testing and Debugging | 15
TOTAL: | 90

2.3.6 Traceability Matrix

SRS Requirement	SDD Module
Req 1	5.1.1 (Client Authentication), 5.2.1 (Registration & Login)
Req 2	5.2.2 (Private Messaging)
Req 3	6.1.1 (Server Handling Single Client)
Req 4	6.2.1 (Secure Communication)
Section 3 - System Architecture
3.1 Overview
The system consists of:

Client: Provides the user interface for interacting with the chat application. Users can register, log in, and send/receive private messages.
Server: Manages the single client connection, handles message routing, and ensures security and data integrity.
3.2 Architectural Diagrams

Component Diagram: Illustrates the relationship between the client and server components.
Sequence Diagram: Shows the interaction between the client and server during a messaging session.
Data Flow Diagram (DFD): Depicts data flow between the client and server.
Deployment Diagram: Details how the client and server components are deployed.
Class Diagram: Defines the classes used in both client and server components.
Use Case Diagram: Highlights user interactions with the client and server.
Section 4 - Data Dictionary
Table

Field	Notes	Type
ID	Unique Identifier for messages and users	DECIMAL
NAME	The Name in Object.Name()	VARCHAR
VALUE	The Value output from messages	VARCHAR
Section 5 – Data Design
5.1 Persistent/Static Data

Dataset: User data (UserID, Username, Password, Email) and message data (MessageID, SenderID, Content, Timestamp).
5.1.1 Dataset

User
Attributes: UserID (PK), Username, Password, Email
Relationships: One-to-One with Messages
Message
Attributes: MessageID (PK), SenderID (FK), Content, Timestamp
Relationships: One-to-One with User
Section 6 - User Interface Design
6.1 User Interface Design Overview
Screens include user registration, login, and chat interfaces. Mockups should show how users interact with the client component.

6.2 User Interface Navigation Flow

Registration → Login → Chat Interface
6.3 Use Cases / User Function Description

Login Screen: Users enter credentials to access the application.
Chat Interface: Displays messages and allows users to send new messages in real-time.
