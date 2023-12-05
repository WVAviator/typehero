# Fewest Stops

## Problem

You've recently learned that there is an important TypeScript conference set to happen _tomorrow_! You are unsure why you hadn't heard about it until now. Obviously, you cannot miss such an event.

You will need to travel by plane from your home airport of 'ABC' to the destination airport of 'XYZ', where the convention will be held. However, you only have a list of flights, and your usual travel agent is out of town. You will need to find the shortest route to the destination on your own.

## Challenge

Implement the type `FewestStops<T>`, where `T` is a tuple of tuples, with each nested tuple representing a single flight in the format `['ABC', 'XYZ']`. The type should resolve to a tuple representing the path with the fewest stops from the origin to the destination, in the format `['ABC', 'DEF', ... , 'XYZ']`.

For this challenge, assume that the shortest route is the route with the fewest stops. A flight from 'ABC' to 'DEF' does _not_ guarantee that there will also be a flight from 'DEF' to 'ABC'.

If there are multiple possible solutions, return _any_ of them. There will always be at least one possible solution.

## Example

```ts
type Flights = [['ABC', 'DEF'], ['DEF', 'GHI'], ['JKL', 'XYZ'], ['DEF', 'JKL'], ['GHI', 'MNO']];
Expect<Equal<FewestStops<Flights>, ['ABC', 'JKL', 'XYZ']>>;
```
