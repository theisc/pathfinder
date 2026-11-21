# Project 2 - Python

**Programming Merit Badge · Python**

Open the [Python compiler](https://www.programiz.com/python-programming/online-compiler/). Type each step. Click **Run**.

## 1. A variable is a labeled box

```python
number = 10
print(number)
print("number")
```

Run it. Then change **10** to your age and run it again.

The box holds a value. `print(number)` shows what is inside. `print("number")` shows the word.

- [ ] The first print showed 10
- [ ] The second print showed the word number
- [ ] I changed 10 to my age and ran it again

## 2. Random picks again every run

```python
import random
number = random.randint(1, 10)
print(number)
```

Run it twice. If both numbers match, run it two more times. The code did not change.

`import` borrows the random tool. `randint(1, 10)` picks a new whole number from 1 to 10 every run.

- [ ] I ran it twice
- [ ] I ran extra times if the two numbers matched

## 3. if runs the pushed-in line only when the test is true

```python
number = 7
if number == 5:
    print("Your number is 5")
print("Done")
```

Run it. Then change **7** to **5** and run it again.

`=` puts a value in the box. `==` asks "same?" The line pushed in is inside the `if`. `Done` is outside, so it always prints.

- [ ] With 7, only Done printed
- [ ] With 5, both lines printed

## Now build the card

Use all three ideas in one program. Grow it in order. Click **Run** after each step.

`suit_pick` (1 to 4) → `if` sets the suit → `rank` (1 to 13) → print **7 of Hearts**

### A. Two boxes, random each run

```python
import random
suit_pick = random.randint(1, 4)
rank = random.randint(1, 13)
print(suit_pick, rank)
```

- [ ] I ran it twice and the numbers could change

### B. One if for each suit

Add these **above** the print.

```python
if suit_pick == 1:
    suit = "Clubs"
if suit_pick == 2:
    suit = "Spades"
if suit_pick == 3:
    suit = "Diamonds"
if suit_pick == 4:
    suit = "Hearts"
```

Each pushed-in line stores the suit word in a box named `suit`.

- [ ] I typed the ifs for 2, 3, and 4

### C. Say the card

Replace the old print with this line.

```python
print(rank, "of", suit)
```

Ace = 1, Jack = 11, Queen = 12, King = 13.

Run it 8 times.

- [ ] I saw all 4 suits
- [ ] Every rank was 1–13
- [ ] A counselor saw it

**Stuck?** `IndentationError` means a line under `if` is not pushed in. `NameError: suit` means a number 1–4 has no `if`. Ask a counselor.

### Bonus: Blackjack (not required)

You and the dealer each get 3 cards, from 1 to 10. Add each side's cards. Over 21 is a bust, and a bust loses.

```python
import random

player = random.randint(1, 10)
player = player + random.randint(1, 10)
player = player + random.randint(1, 10)

dealer = random.randint(1, 10)
dealer = dealer + random.randint(1, 10)
dealer = dealer + random.randint(1, 10)

print("You have", player)
print("Dealer has", dealer)

if player > 21:
    print("Bust! Dealer wins.")
elif dealer > 21:
    print("Dealer busts. You win!")
elif player > dealer:
    print("You win!")
elif dealer > player:
    print("Dealer wins.")
else:
    print("Push. It's a tie.")
```

Check a bust before you compare the totals. A bigger number still loses when it is over 21. `elif` tries the next test only when the earlier tests were false.

- [ ] I ran it until someone went over 21
