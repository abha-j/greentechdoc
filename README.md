[Greentechdoc](https://github.com/sabuj000/greentechdoc/wiki)

[![Importance of API Documentation](https://i9.ytimg.com/vi/0ZW9yL6hEfg/mq2.jpg?sqp=CICTxfkF&rs=AOn4CLBiJO7zXbM682ScwVuULZ6pD4oolg)](https://www.youtube.com/embed/0ZW9yL6hEfg "Importance of API Documentation - Click to Watch!")

# API Documentation Proccess Guide
This	is	a	suggested	structure,	but	is	by	no	means	the	only	way	to	structure	the	documentation.	Many	of	
these	sections	are	optional,	depending	on	the	complexity	of	the	API,	and	whether	it	is	a	web	API	or	
platform	API.

- Overview (Why	use	the	API?	Provide	use	cases)
  - Getting	Started
  - Key	Concepts
  - Workflow
  - Architecture (primarily	for	platform	APIs or	complex	web	APIs)
  - Authentication (primarily	for	web	APIs)
  - Tutorials
    - How	to…
    - How	to…
    - How	to…
### Sample	Code
- Reference
  - Classes	(for	platform	APIs)
  - Endpoints	(for	web	APIs)
  - Status	codes	and	errors	(for	web	APIs)

# Example
## Login

Used to collect a Token for a registered User.

**URL** : `/api/login/`

**Method** : `POST`

**Auth required** : NO

**Data constraints**

```json
{
    "username": "[valid email address]",
    "password": "[password in plain text]"
}
```

**Data example**

```json
{
    "username": "iloveauth@example.com",
    "password": "abcd1234"
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "token": "93144b288eb1fdccbe46d6fc0f241a51766ecd3d"
}
```

## Error Response

**Condition** : If 'username' and 'password' combination is wrong.

**Code** : `400 BAD REQUEST`

**Content** :

```json
{
    "non_field_errors": [
        "Unable to login with provided credentials."
    ]
}
```
