Two principles are important. First, ==**Product Vision → Persona → Scenario → User Story → Feature**== is the product-oriented flow directly supported by the textbook. Second, ==**Acceptance Criteria**== and the distinction between ==**Functional and Non-functional Requirements**== are not presented in Chapters 1 and 3 as independent requirements-engineering concepts. Therefore, in this course they are clearly identified as **instructor-added engineering practices** that extend the textbook’s discussions of acceptance testing, features, reliability, and performance.

# Software Engineering — Week 1

# Product and Requirements Engineering

## Semester Project

**Global Event Ticket Reservation System**

Students will continuously evolve one software product throughout the semester.

```text
Week 1
Product Vision & Requirements
        ↓
Week 2
Agile + Git
        ↓
Week 3
Architecture
        ↓
Week 4–6
Testing + TDD + Integration
        ↓
...
        ↓
Final
Production-style Software Product
```

The ==`requirements.md`== file created in Week 1 is not a disposable assignment.

It will continue to be used later in architecture, unit testing, TDD, integration testing, deployment, and product evolution.

# Week 1 Learning Outcomes

By the end of this week, students will be able to:

1. Explain the difference between software development and software product engineering.
    
2. Define a clear product vision.
    
3. Identify major stakeholders and users.
    
4. Create realistic personas.
    
5. Describe user needs through scenarios.
    
6. Write well-structured user stories.
    
7. Define measurable acceptance criteria.
    
8. Distinguish functional and non-functional requirements.
    

# The Overall Thinking Process for Week 1

The first idea students need to understand is:

> ==**Software engineering does not begin with code.**==

==Before building a product, we first need to answer questions such as:==

```text
What problem are we solving?
        ↓
What product should we build?
        ↓
Who will use it?
        ↓
What are they trying to do?
        ↓
What should the product provide?
        ↓
How do we know it works?
```

In this course, we organize that thinking as follows:

```text
Opportunity / Problem
        ↓
Product Vision
        ↓
Users / Customers / Stakeholders
        ↓
Personas
        ↓
Scenarios
        ↓
User Stories
        ↓
Features
        ↓
Acceptance Criteria
        ↓
Functional Requirements
        +
Non-functional Requirements
        ↓
Product Requirements Document
```

The core flow that is directly supported by the textbook is:

```text
Product Vision
      ↓
Personas
      ↓
Scenarios
      ↓
User Stories
      ↓
Features
```

Chapter 1 explains that user stories and scenarios are widely used to refine a product vision and identify product features. **Chapter 1, p.24.**

![[Pasted image 20260902170731.png|514]]


# Learning Outcome 1

# 1. Explain the Difference Between Software Development and Software Product Engineering

A useful opening question is:

> ==**“Who decides the requirements?”**==

==This provides a simple way to distinguish traditional project-based software engineering from product-based software engineering.==

## 1.1 Traditional Project-Based Software Engineering

==Many traditional software systems were developed as **custom software** for a specific customer.==

For example, imagine a university asking a software company:

> “Please build a Student Registration System specifically for our university.”

In this case, development begins with the customer’s problem.

```text
Customer
   ↓
Problem
   ↓
Requirements
   ↓
Software Development
   ↓
Software
```

The textbook explains that in traditional project-based development, the software system was based on a set of **software requirements**, and the contract between the customer and the development company included a requirements document. Customers worked with developers to define the functionality and critical attributes of the software in detail. **Chapter 1, pp.11–12.**

In other words:

```text
Customer decides
WHAT should be built.
```

![[Pasted image 20260902171149.png|431]]
## 1.2 Product-Based Software Engineering

Now consider our **Global Event Ticket Reservation System**.

Nobody gives us a 50-page requirements document.

==We have to ask the questions ourselves.==

```text
Is there a problem?

Is there an opportunity?

Who might use this product?

What features would be valuable?

Which features should we build first?
```

==In product-based software engineering, an external customer does not define all the product requirements.==

The textbook explains that the product developer decides:

- which features the product should contain,
    
- when releases should be made,
    
- which platforms should be supported.
    

**Chapter 1, pp.12–13.**

Figures 1.1 and 1.2 illustrate the distinction clearly.

### Project-Based

```text
CUSTOMER

Problem
   ↓
Requirements
   ↓
Software
```
![[Pasted image 20260902171149.png|425]]
### Product-Based

```text
DEVELOPER

Opportunity
    ↓
Product Features
    ↓
Software
```

![[Pasted image 20260902171813.png|439]]
The textbook explains that the starting point for product development is an **opportunity** identified by the developer, and the developer selects product features intended to appeal to potential customers. **Chapter 1, pp.13–14.**

## 1.3 Applying This to the Global Event Ticket Reservation System

A traditional requirements-driven approach might begin like this:

```text
Customer says:

"The system shall have:
- login
- event search
- payment
- 4 user roles
- seat map
- email
..."
```

But in this course, we begin differently.

```text
Problem

People often discover events
through many disconnected channels.

They may not know:
- which seats are available
- whether a reservation succeeded
- whether the same seat was already sold
```

Then:

```text
Opportunity

Build one simple cloud-based system
where users can discover events
and reserve available seats reliably.
```

## 1.4 Software Product Engineering Is Not Just Advanced Programming

Students may initially think:

> “Software Engineering = better programming.”

The textbook explicitly describes this as a **misconception**.

==A successful software product also requires thinking about:==

```text
Customers
Users
Architecture
Cloud Computing
Security
Testing
Code Management
```

**Chapter 1, p.17.**

Therefore:

```text
Software Product Engineering
≠
Programming only
```

Instead:

```text
Software Product Engineering

= Product Thinking
+ Users
+ Requirements
+ Design
+ Programming
+ Testing
+ Deployment
+ Operation
+ Evolution
```

### LO1 Key Message

> **In project engineering, the customer’s problem and requirements are the starting point.**

> **In product engineering, the developer’s identified opportunity and product features are the starting point.**

**Textbook:** Chapter 1, pp.11–14; p.17.

# Learning Outcome 2

# 2. Define a Clear Product Vision

Before coding, students should ask:

> **“What exactly is the product we are trying to build?”**

## 2.1 What Is a Product Vision?

The textbook explains that the starting point for product development should be an informal **product vision**.

A product vision:

- briefly defines the essence of the product,
    
- explains how it differs from competing products,
    
- provides a basis for developing detailed features and attributes.
    

When new features are proposed, they should be checked against the product vision to make sure they contribute to it.

**Chapter 1, p.17.**

## 2.2 The Three Questions a Product Vision Should Answer

The textbook identifies three fundamental questions.

```text
WHAT?
What is the product?
How is it different?

WHO?
Who are the target users and customers?

WHY?
Why should customers buy/use it?
```

**Chapter 1, p.17.**

Students can remember this as:

```text
PRODUCT VISION

WHAT
+
WHO
+
WHY
```

## 2.3 A Weak Product Vision

Consider:

```text
"We will build a ticket website."
```

Ask students:

> Who is it for?

Unknown.

> Why should people use it?

Unknown.

> What makes it different?

Unknown.

Therefore, it is not a strong product vision.

## 2.4 A Better Product Vision

For example:

> **A cloud-based event ticket platform that enables students and young adults to discover events and reserve available seats quickly and reliably from any device.**

Now we can identify:

```text
WHAT
cloud-based event ticket platform

WHO
students and young adults

WHY
quick and reliable event discovery
and seat reservation
```

## 2.5 The Product Vision Template in the Textbook

Chapter 1 introduces Geoffrey Moore’s structured template:

```text
FOR
(target customer)

WHO
(statement of need or opportunity)

THE
(product name)

IS A
(product category)

THAT
(key benefit)

UNLIKE
(primary alternative)

OUR PRODUCT
(primary differentiation)
```

**Chapter 1, p.18.**

Applied to our Ticket System:

```text
FOR
students and young adults

WHO
need a simple way to discover events
and reserve tickets

THE
Global Event Ticket Reservation System

IS A
cloud-based ticket reservation platform

THAT
allows users to find events
and reserve available seats quickly

UNLIKE
fragmented event pages
and manual reservation processes

OUR PRODUCT
provides one simple and reliable
reservation experience
```

## 2.6 Product Vision Is Refined Over Time

Students should not expect their first vision statement to be perfect.

The textbook explains that successful product visions usually evolve through discussion and experimentation.

Possible information sources include:

```text
Domain experience

Product experience

Customer experience

Prototyping and experimentation
```

**Chapter 1, p.19.**

Therefore, the Week 1 vision may change as the semester progresses.

## 2.7 Product Vision as a Feature Filter

Show students the following proposed features:

```text
A. Search events by date

B. Reserve a seat

C. Event notification

D. Play online games

E. Chat with friends
```

Ask:

> “Which features support our Product Vision?”

A and B clearly do.

C may fit depending on the product direction.

D does not.

E requires discussion.

The decision process can be represented as:

```text
New Feature
       ↓
Does it support Product Vision?
       ↓
 YES            NO
  ↓              ↓
Consider       Reject
or Prioritize  or Postpone
```

A Product Vision is therefore not merely an introduction paragraph.

It is a filter for engineering decisions.

### LO2 Key Message

> **A Product Vision explains WHAT we build, WHO it is for, and WHY it matters.**

**Textbook:** Chapter 1, pp.17–20.

# Learning Outcome 3

# 3. Identify Major Stakeholders and Users

We first need to distinguish:

> **Are User and Customer always the same?**

No.

## 3.1 Customer and User

In the textbook’s iLearn example, teachers and students may use the system.

However, the organization purchasing the software may be:

```text
School
University
Training Center
```

Therefore:

```text
USER
≠
CUSTOMER
```

in some situations.

**Chapter 1, p.20.**

## 3.2 In the Ticket System

For example:

```text
Concert Attendee
→ User

Event Organizer
→ User + possibly Customer

Venue Operator
→ User

Platform Company
→ Product Owner

Payment Provider
→ External Partner
```

## 3.3 What Is a Stakeholder?

An important academic clarification is needed here.

**Chapters 1 and 3 do not contain a separate section called “stakeholder identification.”**

Therefore, stakeholder mapping in this class is an instructor-added extension of the textbook’s discussion of users, customers, and product management.

The textbook explains that the Product Manager acts as an interface among:

```text
Software Development Team
          ↕
   Product Manager
          ↕
Broader Organization
          ↕
Customers
```

**Chapter 1, p.21.**

It also explains that product managers should understand customer experience, user types and backgrounds, and how the product may be used. **Chapter 1, p.22.**

## 3.4 Global Event Ticket Reservation System Stakeholder Map

```text
                       Event Organizer
                             │
                             │
                             ▼
Payment Provider ─── Ticket Platform ─── Attendee
                             │
                             │
              ┌──────────────┴──────────────┐
              ▼                             ▼
        Venue Manager                 Administrator
                                             │
                                             ▼
                                      Customer Support
```

Different stakeholders care about different things.

| Stakeholder      | Main Concern                        |
| ---------------- | ----------------------------------- |
| Attendee         | Easy and fast reservation           |
| Event Organizer  | Ticket sales and reservation status |
| Venue Manager    | Accurate seat management            |
| Administrator    | System operation                    |
| Customer Support | Errors, cancellations, and refunds  |
| Payment Provider | Accurate and secure transactions    |
| Product Company  | Product adoption and success        |
| Development Team | Reliable and maintainable software  |

This table is an **instructor-created application** for the Ticket System, not a table directly reproduced from the textbook.

## 3.5 Student Discussion Question

Ask:

> “What happens if we design only for the ticket buyer?”

Possible answers:

- organizers cannot create events,
    
- venue managers cannot manage seats,
    
- support staff cannot investigate problems,
    
- administrators cannot manage incorrect reservations.
    

Therefore, product design should consider multiple perspectives.

### LO3 Key Message

> **A product may have different users, customers, and other parties whose needs affect the product.**

**Textbook foundation:** Chapter 1, pp.20–22.  
**Stakeholder mapping:** Instructor-added application.

# Learning Outcome 4

# 4. Create Realistic Personas

Now we change the question:

> **“What kind of person is our user?”**

## 4.1 “Our User Is Everyone” Is Not a Useful Answer

Compare these two users.

```text
Naraa

20 years old
University student
Uses smartphone every day
Frequently attends concerts
```

and:

```text
Bat

42 years old
Event organizer
Mostly uses desktop
Manages 1,000-seat events
```

The two people may need different interfaces and features.

## 4.2 What Is a Persona?

The textbook describes personas as **“imagined users”**, or character portraits representing types of users who may adopt the product.

Personas help developers think about:

```text
What might this user want?

How might this user use the product?

What difficulties might this user have?
```

**Chapter 3, p.65.**

## 4.3 Why Do We Create Personas?

Chapter 3 states that one of the first questions in product development should be:

> **Who are the target users for my product?**

Understanding potential users helps developers design useful features and an appropriate user interface.

**Chapter 3, p.64.**

## 4.4 Ticket System Persona Example

### Persona 1 — Naraa

```text
Name:
Naraa

Age:
20

Role:
University student in Ulaanbaatar

Technology:
Uses a smartphone for most online activity

Background:
Frequently attends university events
and concerts

Why she may use the product:
She wants a quick way to discover events
and reserve seats.

Typical activities:
- Search events
- Compare dates and prices
- Check seats
- Reserve a ticket

Possible difficulties:
- Slow mobile interfaces
- Complicated registration
- Unclear seat availability
```

## 4.5 What Should a Persona Include?

Figure 3.4 and Table 3.2 emphasize:

```text
Personalization

Job-related information

Education

Relevance
```

**Chapter 3, pp.66–67.**

Therefore, instead of:

```text
Student
Age: 20
Likes music
```

we should describe:

```text
What is this person like?

What is their technical experience?

Why might they use our product?

What might they try to do?
```

## 4.6 Personas Prevent Developers from Designing Only for Themselves

Software developers often have higher technical skill than typical users.

This can lead to thinking:

> “Everyone should understand this.”

But actual users may not.

The textbook explains that personas help team members **“step into the users’ shoes.”**

So instead of asking:

```text
"What would I do?"
```

we ask:

```text
"What would Naraa do?"
```

**Chapter 3, p.68.**

## 4.7 How Many Personas Do We Need?

More is not always better.

The textbook explains that **one or two personas** may be enough for a narrowly targeted group.

In general, more than **five personas** are usually unnecessary for identifying key product features.

**Chapter 3, pp.66–67.**

Therefore, requiring students to create **2–3 personas** in Week 1 is appropriate.

## 4.8 Proto-Personas

In real product development, detailed user research may not always be available.

The textbook calls personas created from limited available information **proto-personas**.

They are less reliable than research-based personas, but they still help the team build a shared understanding of potential users.

**Chapter 3, p.69.**

Week 1 can therefore be framed as a **proto-persona exercise**.

### LO4 Key Message

> **A persona is not “every user.” It is a concrete representation of a typical kind of user.**

**Textbook:** Chapter 3, pp.64–69.

# Learning Outcome 5

# 5. Describe User Needs Through Scenarios

A persona alone is not enough.

Now we ask:

> **“What does Naraa actually do with the product?”**

This is where scenarios are useful.

## 5.1 What Is a Scenario?

The textbook describes a scenario as a narrative in which a user uses product features to do something they want to do.

The scenario should briefly explain the user’s problem and an imagined way in which it may be addressed.

**Chapter 3, pp.69–70.**

## 5.2 Ticket Reservation Scenario

### Scenario: Reserving a Concert Seat

```text
Naraa sees a concert announcement
on social media.

She opens the Global Event Ticket System
on her smartphone.

She searches for the concert
and opens the event page.

She checks the date, price,
and available seats.

She chooses seat A15
and makes a reservation.

The system confirms the reservation
and shows her ticket.
```

At this stage, we do not yet need:

```text
REST API
Database schema
Cloudflare Worker
SQL transaction
TypeScript class
```

because the main question is:

> **How does the user want to use the product?**

## 5.3 Key Elements of a Scenario

The textbook identifies the following major elements:

```text
1. Overall objective

2. Persona involved

3. What is involved in the activity

4. Problems that cannot readily be addressed

5. Possible way the problem could be addressed
```

**Chapter 3, pp.70–71.**

Applied to the Ticket System:

```text
Persona
Naraa

Overall Objective
Reserve one concert seat

Activity
Find event
→ inspect seats
→ select seat
→ reserve

Problem
Another user may reserve
the same seat first.

Possible Solution
The system checks seat availability
before confirming the reservation.
```

## 5.4 A Scenario Is Not a Specification

This distinction is important.

The textbook explicitly states that scenarios are **not specifications**.

Scenarios:

- support communication,
    
- stimulate design creativity,
    
- may lack detail,
    
- may be incomplete,
    
- may not represent all possible interactions.
    

**Chapter 3, pp.70–71.**

Therefore:

```text
Scenario

Naraa reserves a ticket.
```

does not immediately require us to decide:

```text
POST /api/v1/reservations
```

Implementation details can be decided later.

## 5.5 Use Narrative Scenarios in Early Product Design

The textbook recommends **narrative scenarios** rather than overly structured scenarios during early product design because they are easier for users to understand.

**Chapter 3, p.72.**

Therefore, Week 1 scenarios can be written as:

```text
Scenario 1
2–5 paragraphs

Scenario 2
2–5 paragraphs
```

## 5.6 Scenarios Begin with Personas

The textbook states that scenario writing should start with the personas that have already been developed.

**Chapter 3, p.73.**

Therefore:

```text
Persona
  ↓
Scenario
```

is an important relationship.

## 5.7 Scenarios Generate Feature Ideas

For example, from:

```text
searches for the concert
checks available seats
selects seat A15
makes a reservation
```

we can derive potential features:

```text
Event Search

Seat Availability

Seat Selection

Reservation

Confirmation
```

The textbook explains that writing scenarios naturally generates ideas for product features. **Chapter 3, p.75.**

### LO5 Key Message

> **A Persona tells us WHO the user is.**

> **A Scenario tells us WHAT that user is trying to do in context.**

**Textbook:** Chapter 3, pp.69–75.

# Learning Outcome 6

# 6. Write Well-Structured User Stories

A scenario is a relatively large story.

Now we break it into smaller units.

## 6.1 Scenario vs. User Story

The textbook describes scenarios as **high-level stories of system use**.

User stories are finer-grain, more structured narratives describing **a single thing a user wants from the system**.

**Chapter 3, p.76.**

For example:

```text
Scenario
Naraa reserves a concert ticket.
```

can be decomposed into:

```text
Search event

View event information

View available seats

Choose a seat

Reserve a seat

Receive confirmation
```

## 6.2 Standard User Story Format

The textbook presents:

```text
As a <role>,
I <want / need> to <do something>
```

and the version with rationale:

```text
As a <role>,
I <want / need> to <do something>
so that <reason>
```

**Chapter 3, p.76.**

## 6.3 Ticket System Examples

### Story 1

```text
As an attendee,
I want to search for events by date
so that I can find events
that fit my schedule.
```

### Story 2

```text
As an attendee,
I want to see available seats
so that I can choose where to sit.
```

### Story 3

```text
As an attendee,
I want to reserve an available seat
so that I can attend the event.
```

### Story 4

```text
As an event organizer,
I want to create an event
so that customers can reserve tickets.
```

### Story 5

```text
As an attendee,
I want to cancel my reservation
so that the seat can become available again.
```

## 6.4 Three Questions for Checking a User Story

Students can use a simple check:

```text
WHO?
Who wants this?

WHAT?
What single thing do they want?

WHY?
Why is it useful?
```

For example:

```text
As a user,
I want the ticket system
so that I can use tickets.
```

is much less useful than:

```text
As an attendee,
I want to reserve an available seat
so that I can attend the event.
```

## 6.5 Large Stories Become Epics

The textbook explains that a story used for sprint planning should focus on a clearly defined feature or aspect of a feature.

A story that is too large is an **epic** and should be decomposed into smaller stories.

**Chapter 3, pp.76–77.**

Example:

```text
EPIC

As an organizer,
I want to manage everything about an event.
```

can be divided into:

```text
Create an event

Update an event

Configure seats

Set ticket price

Publish an event

Cancel an event
```

## 6.6 Scenario → User Stories

The textbook states that user stories may be used to:

```text
1. Extend and add detail to a scenario

2. Describe an identified feature
```

**Chapter 3, p.77.**

Therefore:

```text
Scenario
Naraa books a concert seat
           ↓
User Stories
           ↓
Search event
View event
View seats
Select seat
Reserve seat
Receive confirmation
```

## 6.7 Why Do We Need Both Scenarios and User Stories?

Students may ask:

> “Why not use only user stories?”

The textbook argues that scenarios are valuable because they read more naturally and provide context about what users are actually doing.

User stories are more focused and structured, so they work well for implementation planning.

**Chapter 3, pp.79–80.**

So:

```text
Scenario
= Context

User Story
= Focused Need
```

### LO6 Key Message

> **A Scenario tells a larger story. A User Story isolates one thing the user wants.**

**Textbook:** Chapter 3, pp.76–80.

# Connecting to Product Features

At this stage, we complete the Chapter 3 flow:

```text
Persona
   ↓
Scenario
   ↓
User Story
   ↓
Feature
```

The textbook explains that a feature allows users to access and use product functionality and that the feature list defines the overall functionality of the system.

**Chapter 3, p.80.**

Example:

```text
Scenario

Naraa wants to attend a concert.
```

↓

```text
User Story

As an attendee,
I want to reserve an available seat
so that I can attend the event.
```

↓

```text
Feature

Seat Reservation
```

## Features Should Have Three Qualities

The textbook recommends that features should ideally be:

```text
Independent

Coherent

Relevant
```

**Chapter 3, p.80.**

For example:

```text
"Manage everything"
```

is not very coherent.

But:

```text
Reserve Seat
Cancel Reservation
Search Event
```

are more clearly defined.

# Feature Creep

When students brainstorm, feature lists often grow rapidly.

The textbook calls this **feature creep**.

Feature creep can increase:

- product complexity,
    
- bugs,
    
- security vulnerabilities,
    
- UI complexity.
    

**Chapter 3, p.83.**

Therefore, not every proposed feature should be implemented.

Return to the Product Vision:

```text
Feature Proposal
      ↓
Does it support the Product Vision?
      ↓
Is it relevant to important users?
      ↓
Does it duplicate another feature?
      ↓
Keep / Reject / Postpone
```

# Learning Outcome 7

# 7. Define Measurable Acceptance Criteria

A distinction is important here.

## Textbook-Direct Concept

Chapter 1 includes **Acceptance Testing**.

## Instructor-Added Concept

In Week 1, we extend this idea to requirements by asking students to define **Acceptance Criteria**.

Acceptance Criteria are not presented as a separate formal concept in Chapters 1 and 3.

## 7.1 Why Do We Need Acceptance Criteria?

Consider:

```text
As an attendee,
I want to reserve an available seat
so that I can attend the event.
```

Ask:

> **“When can we say this story is complete?”**

A developer may say:

> “I wrote the code.”

But from a product perspective, that is not enough.

## 7.2 Acceptance Testing in the Textbook

The textbook explains that acceptance testing verifies whether a software release:

- meets the goals in the product roadmap,
    
- is efficient,
    
- is reliable.
    

Product managers may also develop feature tests that reflect how customers use the product and work through usage scenarios to decide whether the product is ready for release.

**Chapter 1, p.25.**

## 7.3 User Story → Acceptance Criteria

In this course, we extend the idea as:

```text
User Story
      ↓
Acceptance Criteria
      ↓
Acceptance Test
```

Example:

### User Story

```text
As an attendee,
I want to reserve an available seat
so that I can attend the event.
```

### Acceptance Criteria

```text
AC1
Available seat
→ Reservation succeeds.

AC2
Already occupied seat
→ Reservation is rejected.

AC3
Invalid event
→ Error is returned.

AC4
Successful reservation
→ Seat becomes unavailable.

AC5
One seat cannot have
two active reservations.
```

## 7.4 Weak Acceptance Criterion

```text
The reservation should work well.
```

The problem is:

> What does “well” mean?

It is not measurable.

A stronger form is:

```text
Given an available seat,
a valid reservation request
creates exactly one reservation.
```

## 7.5 Given–When–Then

**Given–When–Then is not a format presented in Chapters 1 and 3 of the textbook.**

It is used here as an instructor-added engineering practice.

```text
Given
Seat A15 is available.

When
Naraa requests Seat A15.

Then
the reservation is created
and Seat A15 becomes unavailable.
```

Failure case:

```text
Given
Seat A15 is already reserved.

When
another user requests Seat A15.

Then
the reservation is rejected.
```

This naturally connects Week 1 to later testing work.

```text
Week 1
Acceptance Criteria
        ↓
Week 4
Unit Tests
        ↓
Week 5
TDD
        ↓
Week 6
Integration Tests
```

### LO7 Key Message

> **A User Story says what the user wants. Acceptance Criteria say how we know the story is satisfied.**

**Textbook foundation:** Acceptance Testing — Chapter 1, p.25.  
**Acceptance Criteria / Given–When–Then:** Instructor-added practice.

# Learning Outcome 8

# 8. Distinguish Functional and Non-functional Requirements

Another source distinction is important here.

Chapters 1 and 3 do not formally define:

```text
Functional Requirements
vs.
Non-functional Requirements
```

as separate requirements-engineering sections.

Therefore, this course uses the textbook’s discussion of **features, efficiency, reliability, and performance** as the foundation and adds the FR/NFR distinction as an instructor-added requirements concept.

## 8.1 Functional Requirement

The key question is:

> **What should the system do?**

Chapter 3 explains that features allow users to access and use product functionality, and that the feature list defines overall system functionality.

**Chapter 3, p.80.**

We can express this in traditional requirements language:

```text
FR-1
The system shall allow users
to search for events.

FR-2
The system shall display
available seats.

FR-3
The system shall allow users
to reserve an available seat.

FR-4
The system shall allow users
to cancel a reservation.

FR-5
The system shall allow organizers
to create events.
```

So:

```text
Functional Requirement
=
What behavior or capability
does the system provide?
```

## 8.2 Non-functional Requirement

Now change the question:

> **How well must the system work?**

or:

> **Under what constraints must it operate?**

Chapter 1 discusses **efficiency** and **reliability** as important concerns in acceptance testing. **Chapter 1, p.25.**

The textbook also explains that prototypes may temporarily ignore issues such as **reliability and performance** to accelerate development. **Chapter 1, p.26.**

We extend these ideas into NFR examples.

## 8.3 Ticket System NFR Examples

### Performance

Weak:

```text
The system should be fast.
```

Better:

```text
95% of event search requests
shall complete within 500 ms.
```

### Reliability

Weak:

```text
The system should be reliable.
```

Better:

```text
A confirmed seat shall not have
more than one active reservation.
```

### Security

```text
Only authenticated users
may modify their reservations.
```

### Observability

```text
All critical reservation failures
shall be logged.
```

### Availability

```text
The production service
shall maintain 99.9% monthly availability.
```

## 8.4 Functional vs. Non-functional Requirements

A simple way to remember the distinction:

```text
Functional Requirement

WHAT?
What should the system do?
```

Example:

```text
Reserve a seat.
```

In contrast:

```text
Non-functional Requirement

HOW WELL?
Under what quality or constraint?
```

Example:

```text
Complete the reservation
within 500 ms.
```

## 8.5 Where Does “No Double Booking” Belong?

This is a good discussion question.

```text
No double booking
```

is not perfectly classified as only a non-functional requirement.

A more precise interpretation is:

```text
Business Rule
or
Integrity Constraint
```

For example:

```text
For each seat,
there may be at most
one active reservation.
```

This rule affects functional behavior:

```text
IF available
→ reserve

IF occupied
→ reject
```

It also affects reliability and concurrency.

```text
User A ─┐
        ├─ reserve A15
User B ─┘
   same time
```

Even when two requests arrive at the same time, only one should succeed.

Therefore, emphasize:

> **The label of a requirement is less important than whether the requirement is clear and testable.**

### LO8 Key Message

> **Functional requirements describe WHAT the system does.**

> **Non-functional requirements describe HOW WELL or under what constraints it must do it.**

**Textbook foundation:** Features — Chapter 3, p.80; Acceptance Testing — Chapter 1, p.25; Prototype reliability/performance discussion — Chapter 1, p.26.  
**FR/NFR distinction:** Instructor-added requirements engineering concept.

# Connecting All Eight Learning Outcomes

At the end of Week 1, students should be able to see the entire structure.

```text
[1]
Product Engineering
       ↓
Opportunity

       ↓

[2]
Product Vision
WHAT?
WHO?
WHY?

       ↓

[3]
Users / Customers /
Stakeholders

       ↓

[4]
Persona
WHO is a typical user?

       ↓

[5]
Scenario
WHAT are they trying to do?

       ↓

[6]
User Story
WHAT single thing
do they want?

       ↓

Feature
WHAT capability
will the product provide?

       ↓

[7]
Acceptance Criteria
HOW do we know
it works correctly?

       ↓

[8]
Requirements

Functional
WHAT does it do?

Non-functional
HOW WELL must it work?
```

# Global Event Ticket Reservation System — End-to-End Example

Now complete one example from beginning to end.

## Step 1 — Opportunity

```text
Users often discover events
through disconnected channels.

Ticket availability may be unclear.

Manual booking may result
in reservation errors.
```

## Step 2 — Product Vision

> **A cloud-based event ticket platform that enables users to discover events and reserve available seats quickly and reliably.**

**Textbook connection:** Product Vision — Chapter 1, pp.17–20.

## Step 3 — Users / Stakeholders

```text
Attendee

Event Organizer

Venue Manager

Administrator

Payment Provider

Customer Support
```

## Step 4 — Persona

```text
Naraa

Age:
20

Role:
University student

Technology:
Mobile-first

Context:
Frequently attends concerts
and university events

Needs:
Fast event discovery
Clear seat availability
Simple booking
```

**Textbook connection:** Personas — Chapter 3, pp.64–69.

## Step 5 — Scenario

```text
Naraa sees a concert announcement.

She opens the Ticket System
on her smartphone.

She searches for the concert.

She opens the event details.

She checks available seats.

She chooses A15.

She reserves the seat.

The system confirms her reservation.
```

**Textbook connection:** Scenarios — Chapter 3, pp.69–75.

## Step 6 — User Stories

```text
As an attendee,
I want to search for events
so that I can find events
I want to attend.
```

```text
As an attendee,
I want to view available seats
so that I can choose where to sit.
```

```text
As an attendee,
I want to reserve an available seat
so that I can attend the event.
```

**Textbook connection:** User Stories — Chapter 3, pp.76–80.

## Step 7 — Features

```text
Event Search

Event Details

Seat Availability

Seat Selection

Seat Reservation

Reservation Confirmation
```

Chapter 3 explains that scenarios and stories can be used for feature identification. **Chapter 3, pp.80–86.**

## Step 8 — Acceptance Criteria

```text
AC1
Available seat
→ reservation succeeds.

AC2
Occupied seat
→ reservation fails.

AC3
Invalid event
→ error is returned.

AC4
Successful reservation
→ seat becomes unavailable.

AC5
One seat cannot have
two active reservations.
```

**Instructor-added practice**, based conceptually on Acceptance Testing in Chapter 1, p.25.

## Step 9 — Functional Requirements

```text
FR-1
The system shall allow
users to search events.

FR-2
The system shall display
event details.

FR-3
The system shall display
available seats.

FR-4
The system shall allow
a user to reserve an available seat.

FR-5
The system shall allow
a user to cancel a reservation.
```

## Step 10 — Non-functional Requirements

```text
NFR-1 Performance

95% of reservation requests
shall complete within 500 ms.
```

```text
NFR-2 Reliability

A seat shall have no more than
one active reservation.
```

```text
NFR-3 Security

Only authenticated users
may modify reservations.
```

```text
NFR-4 Observability

Critical reservation failures
shall be logged.
```

```text
NFR-5 Availability

The production system
shall achieve 99.9%
monthly availability.
```

The FR/NFR distinction is instructor-added. The textbook directly connects product functionality to features and discusses quality concerns such as efficiency, reliability, and performance.

# Requirement Traceability

This is one of the most important structures to show students at the end of Week 1.

```text
Product Vision
      ↓
Persona
      ↓
Scenario
      ↓
User Story
      ↓
Feature
      ↓
Acceptance Criteria
      ↓
Test
```

Example:

```text
VISION
Fast and reliable seat reservation

        ↓

PERSONA
Naraa

        ↓

SCENARIO
Naraa books concert seat A15

        ↓

USER STORY
As an attendee,
I want to reserve an available seat

        ↓

FEATURE
Seat Reservation

        ↓

ACCEPTANCE CRITERIA
Available → success
Occupied → reject

        ↓

WEEK 4 TEST

reserveAvailableSeat() → PASS

reserveOccupiedSeat() → REJECT
```

The value of this structure is that the requirements created in Week 1 are directly connected to later software engineering activities.

# Lab 1

# Define the Global Event Ticket Reservation System

Students create the following chain as a team:

```text
Product Vision
        ↓
Users / Stakeholders
        ↓
Personas
        ↓
Scenarios
        ↓
User Stories
        ↓
Features
        ↓
Acceptance Criteria
        ↓
FR / NFR
```

# Lab Example

## Product Vision

```text
A cloud-based ticket platform
that allows users to discover events
and reserve available seats
quickly and reliably.
```

## Persona

```text
Naraa

University student
Mobile-first user
Frequently attends concerts
```

## Scenario

```text
Naraa wants to attend a concert.

She finds the event,
checks seat availability,
selects A15,
and reserves the seat.

The system confirms
the reservation.
```

## User Story

```text
As an attendee,
I want to reserve an available seat
so that I can attend the event.
```

## Feature

```text
Seat Reservation
```

## Acceptance Criteria

```text
Available seat
→ reservation succeeds

Occupied seat
→ reservation rejected

Invalid event
→ error
```

## Non-functional Requirements

```text
95% response time < 500 ms

No two active reservations
for one seat

Critical failures are logged
```

# Assignment 1

# Product Requirements Document

### Deliverable

```text
docs/
└── requirements.md
```

Students submit:

1. Product Vision
    
2. Stakeholder / User List
    
3. 2–3 Personas
    
4. 5 User Scenarios
    
5. 10 User Stories
    
6. Initial Feature List
    
7. Acceptance Criteria
    
8. 5 Functional Requirements
    
9. 5 Non-functional Requirements
    
10. AI Use Statement
    

# Recommended `requirements.md` Structure

```text
# Global Event Ticket Reservation System

## 1. Product Vision

## 2. Users and Stakeholders

## 3. Personas

### Persona 1
### Persona 2
### Persona 3

## 4. Scenarios

### Scenario 1
### Scenario 2
...

## 5. User Stories

US-01
US-02
...

## 6. Features

F-01
F-02
...

## 7. Acceptance Criteria

AC-01
AC-02
...

## 8. Functional Requirements

FR-01
FR-02
...

## 9. Non-functional Requirements

NFR-01
NFR-02
...

## 10. AI Use Statement
```

# AI Use Statement for Every Assignment

```text
## AI Tool Used

ChatGPT / Gemini / NotebookLM / Other


## I Used AI For

Brainstorming / Research / Writing /
Data / Coding / Feedback


## What AI Produced

...


## What I Changed

...


## What I Rejected

...
```

One point should be emphasized:

> **AI output itself is not the assignment.**

Students should be able to explain:

```text
What did AI suggest?

Why did I accept it?

What did I change?

What did I reject?

Why?
```

In other words, AI use also requires engineering judgment.

# Week 1 Textbook Reading Map

|Learning Outcome|Textbook|
|---|---|
|LO1 Project vs. Product Engineering|**Ch.1, pp.11–14; p.17**|
|LO2 Product Vision|**Ch.1, pp.17–20**|
|LO3 Users / Customers|**Ch.1, pp.20–22**|
|LO4 Personas|**Ch.3, pp.64–69**|
|LO5 Scenarios|**Ch.3, pp.69–75**|
|LO6 User Stories|**Ch.3, pp.76–80**|
|Feature Identification|**Ch.3, pp.80–89**|
|LO7 Acceptance Criteria|**Instructor-added; related to Acceptance Testing, Ch.1 p.25**|
|LO8 FR/NFR|**Instructor-added; related to Features Ch.3 p.80 and efficiency/reliability/performance Ch.1 pp.25–26**|

The Key Points of Chapter 3 summarize the same progression: personas are “imagined users,” scenarios describe situations in which users access product features to accomplish something, user stories are finer-grain structured narratives, and user actions in scenarios and stories can be used to identify product features. **Chapter 3, p.89.**

# Final Message for Week 1

A useful way to close the lecture is to show this contrast.

```text
Do NOT start here:

        CODE
```

Instead:

```text
Start here:

PROBLEM / OPPORTUNITY

        ↓

PRODUCT VISION

        ↓

USER

        ↓

PERSONA

        ↓

SCENARIO

        ↓

USER STORY

        ↓

FEATURE

        ↓

ACCEPTANCE CRITERIA

        ↓

REQUIREMENTS

        ↓

DESIGN

        ↓

CODE
```

Then conclude with:

> **Good software engineering does not begin with “What should we code?”**

> **It begins with “Whose problem are we solving, and what product should we build for them?”**

This is why Sommerville’s Chapters 1 and 3 emphasize **Product Vision → Personas → Scenarios → User Stories → Features** rather than beginning with a large traditional requirements specification. In product engineering, developers identify opportunities and decide product features, while user understanding and scenario/story-based thinking are used to refine the product incrementally.