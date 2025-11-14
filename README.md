# PRACTICUM 12 
## Practical 1 : Dart Streams

**Question 1**
![alt text](img/Question1.png)

**Question 2**
![alt text](img/Question2.png)

**Question 3** 
![alt text](img/Question3.png)

**Explanation of yield**

yield* in an async* function is used to forward all events from another stream directly into the current one. Rather than emitting each value manually, it automatically relays every event produced by the other stream.

**Explanation of the Code**

The getColors() function produces a stream of color values. It relies on Stream.periodic to emit a new color every second, and the expression t % colors.length makes the sequence cycle continuously. Using yield*, the function passes along every emitted value from the periodic stream, allowing each generated color to be produced as an event in its own stream.