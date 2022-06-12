# Mobile and Embedded Computing : Exam questions

## Introduction

These questions come from an old exam that has been retrieved from somewhere. If you think of additional questions that might be interesting and relevant to help people to study, feel free to add them even if they don't come from an exam.

Questions have been splited in two categories :

- **Embedded questions** : Questions relative to the first part of the course, concerning subjects such as CoAP, MQTT or RPL.
- **Mobile questions** : Questions relative to the second part of the course, which is the whole GSM part.

Have fun !

## Embedded questions

### Scheduling

>- Explain *Priority Inversion*. Draw a picture of an example (i.e. a timeline with several tasks) and show on that picture where and why the priority inversion happens.
>- Explain the *Immediate Priority Ceiling protocol* and show why and how it solves the problem of priority inversion in your example at the previous point.

### CSMA

>- How can a CSMA/CA give higher priorities to certain frame types ?
>- What problem of CSMA/CA does CSMA/CA with RTS/CTS solve ? *Explain the problem*.
>- Can collisions happen in CSMA/CA with RTS/CTS ? Explain.

### CoAP

>- What are tokens used for in CoAP ?
>- Describe a possible attack against CoAP's token mechanism. How can you defend against such an attack ?
>- Give two major differences between CoAP and HTTP/1 that make CoAP suitable for constrained environments such as networks with IEEE 802.15.4 . Explain briefly.

### RPL

>- Draw a small wireless network (3 or 4 nodes) and explain how the RPL control messages are used to build the initial RPL DODAG (For sake of simplicity, ignore version numbers and trickle timers).
>- What are Tickle timers used for in RPL ? (You don't have to explain how it works).
How would you implement a HELLO Flooding attack against a RPL network ? What is a possible defense ?

### Mobility

>- Assume a computer with a mobile address that is brought into a foreign network. Explain the steps done by Mobile IP, so that the computer gets connectivity.
>- What is Triangular Routing ? Explain it and describe why we cannot always use it.
>- In CDMA, an important parameter is the length of the code. What is the advantage of using a long code ? What is the disadvantage ?

## Mobile questions

### In-band signaling vs Out-of-band signaling

>Does TCP/IP uses in-band or out-of-band signaling for its control information ?

### GSM FDMA

>GSM-900 uses FDMA with 124 downlink and 124 uplink frequencies. In practice, why a BTS cannot use all frequencies ?

### GSM logical channels

>Why does GSM use logical channels that are mapped to physical channels ? Could we not just use physical channels directly ? For example we could define Physical channel 1 = FCCH, Physical Channel 2 = AGCH, etc.

### GSM call setup

>- To save resources, the base station does not allocate a dedicated channel for every phone in a cell, since most are idle most of the time. But if a phone does not have a dedicated channel, how can it send a message to the base station to start a Phone call ?
>- Can you imagine a concrete situation where the mechanism used by GSM in the previous question fails ?
>- Imagine you are in LLN and you want to call your friend in Sydney (you and your friend have mobile phones). How is the connection established? In particular, how does the network find the destination? (we have not seen all the details in the course, but you should have a rough idea how it’s done)

### Logical channel mapping

>There is an important question that has not been addressed on the slides: How does a MS know the mapping of the logical channels to the physical channels? For dedicated channels like SDCCH and TCH, the answer is on the slides (where?). But how does a MS that enters a cell know what frequencies are used by the BTS of the cell and which timeslots are used for the broadcast and common channels? Try to find some possible solutions. (Be creative. Don’t worry if you don’t find the solution actually used by GSM.)

### From circuits to packets

>The first GSM networks were only used for voice calls, but later GSM was extended to also allow Internet traffic. How would you transport Internet traffic over GSM (without modifying too much the existing infrastructure)? What problems could appear?
