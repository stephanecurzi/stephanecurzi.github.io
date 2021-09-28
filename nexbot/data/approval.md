# Beginning
* Hi, You have a new approval waiting<br>Do you want to approve it now ?
* <b>Yes</b> - <b>No</b>
* `input()`	
1. [Yes]
	* `goto(ApprovalYes)`
2. [Not]
	* `goto(ApprovalNo)`

---

# ApprovalYes
* `goto(Expense1)`

# ApprovalNo
* OK then…
* Do you want me to remind you later ?
* <b>Yes</b> - <b>No</b>
* `input()`	
1. [Yes]
	* `goto(Later)`
2. [Not]
	* `goto(NoReminder)`
	
---		

# Later
* I’ll send you a reminder later
* `goto(Finish)`

# NoReminder
* Ok
* You can always find your waiting approvals on the web
* `goto(Finish)`

---

# Expense1
* You have one Expenses Report from Stephane Curzi<br>The expense total is <b>$31.83 USD</b>
* Do you want to see the details ?
* <b>Yes</b> - <b>No</b> - <b>Approve All</b>
* `input()`	
1. [Yes]
	* `goto(ExpenseDetail)`
2. [Not]
	* `goto(NoDetail)`
3. [Approve]
	* `goto(ApproveAll)`
4. [Reject]
	* `goto(RejectAll)`

---

# ExpenseDetail
* There are 2 items
* <b>1</b><br>Taxi & Transit Services<br>Uber, $12.63
* <b>2</b><br>Taxi & Transit Services<br>Uber, $19.20
* You can <b>Approve</b>, <b>Reject All</b>
* Or approve one item at a time using the item number
* `input()`	
1. [ApproveAll]
	* `goto(ApproveAll)`
2. [RejectAll]
	* `goto(RejectAll)`
3. [Item1]
	* `goto(ApproveItem1)`
4. [Item2]
	* `goto(ApproveItem2)`

---

# NoDetail
* Just type <b>Approve</b> or <b>Reject</b>
* `input()`	
1. [Approve]
	* `goto(ApproveAll)`
2. [Reject]
	* `goto(RejectAll)`

---

# ApproveItems
* `goto(NothingLeft)`

# RejectItems
* `goto(RejectMessage)`

---

# ApproveAll
* `goto(NothingLeft)`

# RejectAll
* `goto(RejectAllMessage)`

---

# ApproveItem1
* Ok, the item 1 is approved
* What do you want to do for the item 2
* <b>Approve</b>, <b>Reject</b> or <b>Skip</b>
* `input()`	
1. [Approve]
	* `goto(NothingLeft)`
2. [Reject]
	* `goto(RejectMessage)`
3. [Skip]
	* `goto(Skip)`

---

# RejectItem1
* Ok, the item 1 is rejected<br>I’ve send an email informing Stephane of the rejection
* What do you want to do for the item 2
* <b>Approve</b>, <b>Reject</b> or <b>Skip</b>
* `input()`	
1. [Approve]
	* `goto(NothingLeft)`
2. [Reject]
	* `goto(RejectMessage)`
3. [Skip]
	* `goto(Skip)`

---

# ApproveItem2
* Ok, the item 2 is approved
* What do you want to do for the item 1
* <b>Approve</b>, <b>Reject</b> or <b>Skip</b>
* `input()`	
1. [Approve]
	* `goto(NothingLeft)`
2. [Reject]
	* `goto(RejectMessage)`
3. [Skip]
	* `goto(Skip)`

---



---

# RejectMessage
* I’ve send an email informing Stephane of the rejection
* `goto(Finish)`

# RejectAllMessage
* I’ve send an email informing Stephane of the rejections
* `goto(Finish)`

---

# Skip
* Ok, you can still find it on the web
* `goto(Finish)`

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

[Not]
	* No
	* Not really
	* nope

[Approve]
	* approve
	* approve all

[Reject]
	* reject
	* reject all

[ApproveAll]
	* approve all

[RejectAll]
	* reject all

[Item1]
	* 1
	* approve item 1
	* item 1

[Item2]
	* 2
	* approve item 2
	* item 2
