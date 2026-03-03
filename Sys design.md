
## Functional Requirements
1. Always get clear understanding of clear requirements
	1. Sometimes it is given as the core 
	2. Sometimes you need to determine these
		1. ask clarifying questions
		2. Zero in top features 3-4, rather than bells and whistles

## Non Functional Requirements

1. Means how system operates rather than how task perofrms
2. Scalability, latency, security, availaibility are benchmarks like ability to handle 100 million daily users or latency 200 ms


### Scoping
- For both requirements analyze what is out of scope refer [[bitly]]
## Usual considerations

- Read to write ratios

## Defining the core entities

Start with a broad overview of primary entities rather than knowing every specific col or detail. Intricaies will come later, when we have clearer grasp. This helps set foundation and develop upon it. Do communicate this thought process to the interviewer. 

> I'm going to start with just a simple list, but as we get to the high level design, I'll document the data model thoroughly

## API

- Helps set contract between client and server
- Good point of refrence for the HLD
- Simply go over the functional requirements, and map 1:1
- Sometimes you will need multiple APIs to satisfy individual requirements
- 9/10 you will create REST API and focus on choosing the right HTTP method
	- POST: Create resource
	- GET: Read
	- PUT: Update
	- DELETE: delete

## High level design

Start by going one by one through functional requirements and designing single system to satisfy them, once we have this in place we layer and deep dive

![[Drawing 2026-03-04 00.49.44.excalidraw]]

