## 6. Bond Graphs

A train of three wagons are being pulled by an ideal speed source according to the figure.

<img src="assets/images/bondgraphstability.png" width="300">

There is a spring and damper between the first and second wagon, and only a spring between the second and the third.

Draw a bond graph of the system.

{::nomarkdown}<details><summary><strong>Answer</strong></summary>{:/nomarkdown}

<img src="assets/images/bondgraphfinal.png" width="300">

(there may also be other correct solutions)

{::nomarkdown}</details>{:/nomarkdown}

{::nomarkdown}<details><summary><strong>Solution</strong></summary>{:/nomarkdown}

First we need to identify the junctions (1 = common speed, 2 = common force):

<img src="assets/images/bondgraphtrainjunctions.png" width="300">

We then begin drawing the bond graph by adding the junctions:

<img src="assets/images/bondgraphjunctions.png" width="300">

Then we can add the elements connectec to each junction. The direction of the arrows does not matter, but we assume that all energy flows from the source to all other elements.

<img src="assets/images/bondgraphelements.png" width="300">

We can now simplify the graph by removing junctions with only two connections:

<img src="assets/images/bondgraphsimplified.png" width="300">

Finally, we need to define causalities, e.g. determine which elements that computes speed and which ones that computes force. See lecture notes for the rules.

<img src="assets/images/bondgraphfinal.png" width="300">

This is the final bond graph for the system, which can be used to derive the equation system!

{::nomarkdown}</details>{:/nomarkdown}
