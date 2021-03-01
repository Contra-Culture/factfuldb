# FactfulDB

FactfullDB is an **EXPERIMENTAL**  fact-based DBMS framework.

---

## Storage Engine

### Formats

#### JSON

#### GOP

### Methods

#### Facts timeseries

#### Columns-based store

#### Tables

---

## Philosophy / Onthology / Model

### Fact

A fact is a change. Every fact represents new information. For example, if content manager have changed publication title in the admin Web GUI, the corresponding request to a server could be represented by the following fact:
```json
{
  "publicationID": 100500,
  "publicationTitle": "The New Title",
  "authorID": "james.dirk@some-corp.com",
  "meta": {
    "preparedAt": "2021-01-02 12:11:16",
    "source": {
      "type": "WEB GUI",
      "ipAddress": "121.10.102.56",
      "macAddress": "..."
    },
    "reason": "simple edit",
  }
}
```

### Arrow

Arrow represents bi-direction associations between two facts. Each direction of a fact has its own name, for example:
```parent:<fact-type>.<primary-key> | child:<fact-type>.<primary-key>```


### Questions and Answers

You can ask database with some questions. Every question contains the answer, in the FactfulDB case, question represents a pattern of the answer, so that every answer is a product of pattern matching, using a question (pattern) and a universe of known facts.


### Aggregate / Perspective / Entity

An aggregate consists of facts and also is a fact. For example, an entity's state could be calculated from its history that is nothing else but an aggregate of facts. Entities are presented in the system as self-perspectives.

A perspective is a kind of an aggregate which has direction, list of kinds of facts and aggregation rules. Self-perspective is a special kind of perspectives, that views on facts from the viewpoint of self and constructs self state for a particular moment.

An entity is a tuple of self-perspective and a predicate-function, that is also a change application funtion.

### Epoch / Schema change

---

## Performance optimization reasoning and strategies


---
