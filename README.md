<p align="center">
	<b>MD5-BatKill - <a href="https://www.youtube.com/watch?v=t85oQpT_Rqw">YouTube<a/></b>
	<br>
  <i>Fast MD5 cracker (about half a million hashes per second).</i>
	<br><br><br>
	<img alt="Screenshot_1" src="https://user-images.githubusercontent.com/48186982/80112573-8b25b100-8581-11ea-92a4-535e4c759919.png">
</p>

# Installation
`git clone https://github.com/hXR16F/MD5-BatKill.git`\
Or click **Download ZIP**.

# Usage
It's only for Windows. You can use **GUI** or **CLI** version:
* `md5-batkill.bat` **(CLI)** - double-click to run, paste hash and hit enter.
* `GUI.exe` **(GUI)** - double-click to run, paste hash into first input, select method (go to bottom of `README.md`) and click '*Crack*' button.

# Cracking
It uses an optimized wordlist. Here is how `wordlist.lst` looks:
```
fffe:q12q13qq
fffe:thicluv
fffe:wanjirah
ffff:1530257
ffff:17011959
ffff:21101102ab
ffff:4369927
```
`fffe` and `ffff` are the first four characters of hash. So instead of hashing entire dictionary, it only picks some words and then it's checking for valid hash. It's **a lot faster** than hashing every word.\
Why only 4 characters? Because wordlist size could be 2/3 times larger - **it's a balance between speed and size**.

# Wordlists
## Want bigger wordlist?
Go to https://hashkiller.io/listmanager and download some.\
After downloading you need to use `scripts/hashkiller2batkill.py`.\
\
**How to use it:**\
Open `scripts/hashkiller2batkill.py` via notepad (or another text editor) and look at first line:
```python
wordlist = 'my-wordlist.txt'
```
Just replace `my-wordlist.txt` with file you previously [downloaded](https://hashkiller.io/listmanager) and then run: `py hashkiller2batkill.py` while you're in `scripts` folder. It will generate second wordlist for `MD5-BatKill`.

## Or maybe you already have a wordlist that looks like that:
```
password
123456
qwerty
dragon
```
So now you will need `scripts/wordlist2batkill.py`.\
\
**How to use it:**\
Open `scripts/wordlist2batkill.py` via notepad (or another text editor) and look at second line:
```python
wordlist = 'my-wordlist.txt'
```
Just replace `my-wordlist.txt` with file you want to make it readable to `MD5-BatKill` and then run: `py wordlist2batkill.py`. It can take some time so be patient.

# Methods
There are two methods:
* `core\md5.exe -l -d` Faster, don't need to install additional packages. Hasher is from https://www.fourmilab.ch/md5/.
* `py core/md5.py` Slower, needs [python3](https://www.python.org/downloads/) to be installed.

# Donate
If you support my work or like my projects, [you can donate me some money](https://github.com/hXR16F/donate/blob/master/README.md). Thank you 💙
