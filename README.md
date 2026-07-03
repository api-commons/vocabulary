# API Vocabulary

An API Vocabulary is a machine-readable dictionary of the words and phrases in use across an API, or an entire domain of APIs. Each entry defines a word, records its context, and captures details like its singular and plural forms, whether it is a noun or a verb, whether it can be used in an API path, and whether it should be used at all. Consistent language is one of the hardest and most valuable things to get right in API operations—naming resources, parameters, and paths the same way everywhere reduces confusion for producers and consumers alike. The vocabulary building block gives teams a common, standardized way to agree on the terms they use.

## API Commons

An API Vocabulary is an [API Commons](http://apicommons.org) building block—an open, machine-readable schema for standardizing the words we use across APIs, made interoperable as part of the API contract. It is indexed as a `Common` type within its [APIs.json](apis.yml) index, letting it be discovered, referenced, and reused across the APIs.json ecosystem and surfaced through [apis.io](https://apis.io).

## What's in this repo

- [vocabularies-schema.yml](vocabularies-schema.yml) — The JSON Schema that defines a vocabulary word or phrase.
- [vocabularies-example.yml](vocabularies-example.yml) — A worked example describing a single vocabulary entry.
- [apis.yml](apis.yml) — The APIs.json index for this building block, referencing the schema and example as `Common` artifacts.

## The Schema

The [vocabularies-schema.yml](vocabularies-schema.yml) defines each word or phrase as an object with the following properties:

- **name** — The word or phrase that is part of the vocabulary.
- **definition** — A short definition of what a word or phrase means.
- **notes** — Extra notes about the word that help define the context.
- **related** — An array of related words that are used, but should be transformed.
- **children** — An array of words or phrases that are children underneath this word or phrase.
- **singular** — The singular representation of the word or phrase.
- **plural** — The plural representation of the word or phrase.
- **noun** — Whether the word is a noun, describing a person, place, or thing (boolean).
- **verb** — Whether the word is a verb, providing some sort of action (boolean).
- **path** — Whether the word or phrase can be used as part of the API path (boolean).
- **use** — Whether this word or phrase should be used or not used (boolean).

## Example

The [vocabularies-example.yml](vocabularies-example.yml) file describes a single vocabulary entry:

```yaml
name: APIs
definition: An application programming interface, which is often shortened to just API.
notes: A pretty top-level and ubiquitous term that regularly gets applied across operations.
related:
  - Application Programming Interface
  - Application Programming Interfaces
  - API
children:
  - REST APIs
  - Hypermedia APIs
singular: API
plural: APIs
noun: true
verb: false
path: true
use: true
```

## How It Fits

Vocabulary is one of a growing set of API Commons building blocks that describe the business and technical realities of API operations in a machine-readable way. It cross-links with the [change log](https://github.com/api-commons/change-log), [road map](https://github.com/api-commons/road-map), [teams](https://github.com/api-commons/teams), [use cases](https://github.com/api-commons/use-cases), [guidance](https://github.com/api-commons/guidance), [policies](https://github.com/api-commons/policies), and other building blocks—each a small, reusable schema that can stand alone or be composed together within an APIs.json index.

## Support

This work is in an early stage of development and is rapidly moving as it is applied across a variety of user interfaces and approaches to API operations and governance. If you would like to contribute, have any questions, or would like to inform the work happening, please submit a GitHub issue on this repository or email kin@apievangelist.com.
