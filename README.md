# redux-ecq

**E** for Entity: an entity is a business object that has identity in the domain which we are building a front-end for. Typically, in any real-world application, a business domain can be seen as a collection of entities that refer to each other by identity.

**C** for Command: a call to a remote backend to modify the state of that backend, to execute a side-effect that changes the state of the world, e.g. place an order on an e-store, triggers a shipment ... etc.

**Q** for Query: On the other side, a query is a call to a remote backend to retrieve data without changing anything.

Redux ECQ is a library that allows developers to run commands and queries against backends while managing all the involved state, including query / command execution states and the state of data entities coming back from queries or being updated by commands. The library helps bring the following merits to front-end applications:

## Less or No Side-Effect-Managing Business Inside Components
The library offers hooks for watching query state and firing query requests in one-way fashion. The following code snippet shows how queries are created and run as hooks using this library:

```ts
import { queryHook } from "redux-ecq";

const useShipmentFinder = queryHook(entityModel, "shipment", (req:ShipmentFindReq) => {


});

```

## Reactive-Readiness
Redux CQ is a library that leverages Redux to enable building React components that are really "reactive" in that they are agnostic to a backend's communication patterns (request-reply or push-based). A reactive component is one that does not "ask" for data but instead "tells" its need for data and then reacts to state changes as data arrives back.

TBD

## Normalized State of Front-end Data
In Redux documentation, the author recommends keeping data entities in a normalized state shape. 

TBD




