# Cedric's Notes for code-301n24 course

## Application Program Interface

### API Design Best Practices

- What does REST stand for?

Representational state transfer


- REST APIs are designed around a resource.


- What is an identifer of a resource? Give an example.

URIs for an endpoint are used as resource identifiers

- What are the most common HTTP verbs?

The most common operations are GET, POST, PUT, PATCH, and DELETE.

- What should the URIs be based on?

When possible, resource URIs should be based on nouns (the resource) and not verbs (the operations on the resource).

- Give an example of a good URI.

Adopt a consistent naming convention in URIs. In general, it helps to use plural nouns for URIs that reference collections. It's a good practice to organize URIs for collections and items into a hierarchy. For example, /customers is the path to the customers collection, and /customers/5 is the path to the customer with ID equal to 5. This approach helps to keep the web API intuitive.

- What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?

Another factor is that all web requests impose a load on the web server. The more requests, the bigger the load. Therefore, try to avoid "chatty" web APIs that expose a large number of small resources.

- What status code does a successful GET request return?

200

- What status code does an unsuccessful GET request return?

404


- What status code does a successful POST request return?

201

- What status code does a successful DELETE request return?

204


## Things I want to know more about

How are we going to use REGEX moving forward - I'm curious.
