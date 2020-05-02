---
    title: An Example of a Strategy
---

Given below is the PARASITE strategy
```
Charles Pence
Parasite
12
C, 1, 11
C, 2, 11
C, 3, 11
D,7,4
D,5,6
D,5,5
C,6,6
C,8,8
C,9,9
C,10,10
C,10,11
D,10,11
```
This code corresponds to the PARASITE strategy whose FSA diagram is given below-

<figure>
  <img src="/pd-game/res/cpfsa.png" alt="cpfsa.png"/>
  <figcaption>Figure 5: FSA Diagram for the PARASITE strategy</figcaption>
</figure>

Here is the same PARASITE code with comments to understand the steps-
```
CHARLES PENCE
PARASITE
12 #No. of total states
#	Lead in to handshake -- if this fails, fall back to TfT
#0 	C, 1, 11
#1 	C, 2, 11
#2 	C, 3, 11

#	The handshake itself, if it fails, make up and then play TfT (Tit for Tat)
#3	D,7,4

#	Handshake was successful, this is the identification turn:
    D means we’re a parasite, C means we’re a host
#4	D,5,6

#	I’m a parasite and he’s a host--take advantage loop
#5	D,5,5

#	Two parasites--cooperate loop
#6	C,6,6

#	Three cooperates -- the apology
#7	C,8,8
#8	C,9,9
#9	C,10,10

#	Standard TfT
#10	C, 10, 11
#11	D, 10, 11
```
