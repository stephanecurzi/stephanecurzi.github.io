# Beginning
* `pause(50)`	// Will wait for 1 seconds
* Hi, You have a new approval waiting<br>Do you want to approve it now ?
* <b>Yes</b> or <b>No</b>
* `input()`	
1. [Yes]
* You have one Expenses Report from<br>Stephane Curzi, the expense total is $34.06 USD<br>Do you want to see the details ?
* <b>Yes</b> - <b>No</b> - <b>Approve</b> - <b>Reject</b>
	* `input()`
	1. [Yes]
		* There are 2 items, first is <br> Taxi & Transit Services <br> Uber, $12.63
		* <b>Approve</b> or <b>Reject</b>
		* `input()`
			1. [Approve]
				* One item left<br>Taxi & Transit Services<br>Uber, $21.43
				* <b>Approve</b> or <b>Reject</b>
				* `input()`
					1. [Approve]
						* `goto(NothingLeft)`
					2. [Reject]
						* I’ll send an email informing Stephane of the rejection
						* `goto(NothingLeft)`
					3. Other
						* `goto(NothingLeft)`
			2. [Reject]
				* I’ll send an email informing Stephane of the rejection
				* One item left<br>Taxi & Transit Services<br>Uber, $21.43
				* <b>Approve</b> or <b>Reject</b>
				* `input()`
					1. [Approve]
						* `goto(NothingLeft)`
					2. [Reject]
						* I’ll add this item to the rejection email
						* `goto(NothingLeft)`
					3. Other
						* `goto(NothingLeft)`
	2. [No]
		* Just type Approve or Reject
		* `input()`
		1. [Approve]
			* `goto(NothingLeft)`
		2. [Reject]
			* I’ve send an email informing Stephane of the rejection
			* `goto(NothingLeft)`
	3. [Approve]
		* No more approval left, Have a great day !
	3. [Reject]
		* I’ve send an email informing Stephane of the rejection
		* `goto(NothingLeft)`
2. [No]
	* OK then…
	* Do you want me to remind you later ?
	* `input()`
		1. [Yes]
			* I’ll send you a reminder later
			* Have a great day !
		2. [No]
			* Ok, you can find your waiting approvals on the web
			* Have a great day !

---

# NothingLeft
* No more approval left
* `goto(Finish)`

# Finish
* Have a great day !

---

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