# rest-challenges

Designing REST APIs can be challenging sometimes. I created this project to answer some of those challenges collaboratively.

## Who is this supposed to work?

1. Someone opens an issue with your challenge
2. Community members are invited bring on their solutions
3. Once the solution is agreed by the majority it gets documented

We should try to find and define common patterns and will turn eventually into a nice generic guide for anyone who wants to learn more about RESTful APIs.

## Challenges

### How do I implement login and logout in a RESTful service?

GENERAL NOTE
> REST APIs should use only the available HTTP verbs. Whenever you need extra verbs you should try create a different resource where the verb is one of the HTTP verbs.

So, my solution for this challenge is to create a new resource called `SESSION`. Instead of thinking that the endpoint "should `LOGIN` the `USER`", think that the endpoint "should `CREATE` a `SESSION`". `LOGIN` is not an allowed verb but `CREATE` can be associated with the `POST` method.

**Example endpoints**

Login

```
POST /sessions
{
  "username": "example@gmail.com",
  "password": "secret123"
}
```

Logout

```
DELETE /sessions/{token}
```

### How do I do X?

Just open a new issue and I will be more than happy to try to answer it.