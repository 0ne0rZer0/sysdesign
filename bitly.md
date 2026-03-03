
Design a URL shortener.

----
## Functional Requirements

### Core requirements (given)
- Submit long URL, receive short
	- Optionally, custom alias (/my-custom-alias)
	- Optionally, expiration date
- Redirects to original URL
-
### Out of scope (given)
- Auth
- Analytics

## Non Functional Requirements
- Uniqueness of short urls, 1 to 1 mapping
- Redirection has minimal delay (<100ms)
- 99.99% (4 nines) availability
	- Availability > consistency
- Scale to 1B shortened URLS, and 100M DAU

### Out of scope
- Consistency in real time analytics
- Spam detection and malicious filtering

### System usages
- Read to write ratio is skewed heavily towards reads.
	- Why?
		- Users will frequently access shortened URL 
		- Compared to that 1 shortening for 1 long url
- This behaviour impacts are 
	- caching strat
	- db
	- overall arch

> I'm going to start with just a simple list, but as we get to the high level design, I'll document the data model thoroughly
### Core entities

- Original URL
- Short URL
- User

## API

- We want to create a short url from long url
	- POST
		- with optional parameters
		- custom alias
		- expiry
- For redirection we need
	- GET 
		- queries the short url /
		- returns the long url with 302 HTTP code


## High level design

### 1. Submit long url, receive short

