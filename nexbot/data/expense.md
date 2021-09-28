# Beginning
* `pause(50)`	// Will wait for 1 seconds
* Hi
* Do you want to create an expense ?
* `input()`
	1. [Yes]
		* What type of expenses was it ?
		* `input()`
		1. [Travel]
			* Is it an expenses for today ?
			* `input()`
				1. [Yes]
					* If you have a receipt, just sent it now
					* `input()`
						1. [img]
							* That’s good for now, you can finish it later
							* See you soon
				2. [No]
					* Just type the date below
		2. [Other]
	2. [No]













---


# Repeat
* Sorry, I didn't get that…
* Can you repeat please ?


# Reject
 * I’ve send an email informing Stephane of the rejection
 * You don’t have any approval left


# LastItem
* One item left <br> Taxi & Transit Services <br> Uber, $21.43
* &lsqb; Approve &rsqb; or &lsqb; Reject &rsqb;
* `input()`
	1. [Approve]
		* `goto(NothingLeft)` 
	2. [Reject]
		* `goto(NothingLeft)`
	3. Other
		* `goto(Repeat)`
		* `goto(LastItem)`


# NothingLeft
* No more approval left
* `goto(Finish)`


# Finish
* Have a great day !



// Possible choices

[Yes]
	* yes
	* sure
	* ok
	* yep

[No]
	* No
	* Not really
	* nope

[Approve]
	* approve
	* yes

[Reject]
	* reject
	* no

// &lsqb; Yes &rsqb; or &lsqb; No &rsqb; 