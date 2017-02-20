# GraphSupport - Intercom Example

## Sections

1. How to create a **data model** with GraphQL?
- How to interact with a GraphQL backend from a **client** application (using _Apollo_)? 
- How to fetch data using **queries**?
- How to create, update or delete data using **mutations**?
- How to get real time updates from the database with **subscriptions**? 
- How to perform actions in reaction to a mutation using **mutation callbacks**?
- How to do **file management** with Graphcool?
- How to constrain read/write access to certain data using **permissions**?


## Features

### Roles

- **Customer:** Comes to website X and asks support question
- **Operators:** Responds to questions
- **Admin:** Configures rules about when conversation is automatically initiated by operator and has access to chats and meta information


### Stories

1. **As a customer, I want to...**

	1. initiate a chat with an operator (Phase: 1️⃣)
	-  chat and see when the operator is currently typing (Phase: 2️⃣) 
	-  upload a file in the chat (Phase: 4️⃣)
	-  leave my email address in case I don't get a response after X min

2. **As an operator, I want to...**

	1. initiate a chat with a customer (Phase: 1️⃣) 
	-  chat see when the customer is currently typing (Phase: 2️⃣)
	-  archive a conversation (Phase: 2️⃣)
	-  receive a notification when a conversation was rated by the admin (Phase: 3️⃣)
	-  see my average rating (Phase: 3️⃣)
	-  view a file that gets sent by a customer in a chat (Phase: 4️⃣)
	-  mention another operator 
	-  get notified when I get mentioned by another operator


3. **As an admin, I want to...**

	1. view all archived and live chats with customers (Phase: 1️⃣)
	-  delete chats from the database (Phase: 1️⃣)
	-  receive a notification when an operator archived a chat (Phase: 3️⃣)
	-  rate the performance of an operator for a specific conversation (Phase: 3️⃣)
	-  delete files from the database (Phase: 4️⃣)
	-  add a new rule that will automatically initiate a conversation
	-  view, add, edit and delete notes to a chat


### Implementation Phases

- 1️⃣ Basic chat
	- **Covers sections**: Data modelling, Queries, Mutations
	- **Includes stories**: 1.1, 2.1, 3.1, 3.2
		- Customer wants to initiate a chat with operator (1.1)
		- Operator wants to initiate a chat with customer (2.1) 
		- Admin wants to see all chats (3.1)
		- Admin wants to delete chats (3.2)

- 2️⃣ Advanced chat
	- **Covers sections**: Subscriptions, Mutations
	- **Includes stories**: 1.2, 2.2, 2.3
		- Customer wants to chat and see when operator is typing (1.2)
		- Operator wants to chat and see when customer is typing (2.2) 
		- Operator wants to archive a conversation (2.3)
	
- 3️⃣ Basic admin functionality
	- **Covers sections**: Mutation Callbacks
	- **Includes stories**: 2.4, 2.5, 3.3, 3.4
		- Operator wants to receive a notification when a conversation was rated (2.4) 
		- Operator wants to see average rating (2.5) 
		- Admin want to receive a notification when an operator archived a chat (3.3)
		- Admin want to rate the performance of an operator for a specific conversation (3.4)

- 4️⃣ File upload & storage	
	- **Covers sections**: File management, Permissions
	- **Includes stories**: 1.3, 2.6, 3.5
		- Customer wants to upload a file in the chat (1.3) 
		- Operator wants view a file that gets sent by a customer in a chat (2.6) 
		- Admin wants to delete files from the database (3.5)


## Questions

- Permissions?
	