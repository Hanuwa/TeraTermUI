# `FEEDBACK.md`

A quiet, anonymous inbox for your thoughts about the app.

## What it is  
A tiny button inside "Status" window in the program labelled *“Send feedback”*. type what’s on your mind, hit *Send*.  
The message slips out, no name attached, and lands in a private Google Sheet only I can read.

## Why it exists  
Bugs and big features belong on GitHub, but the small stuff like *“this icon looks off”* or *“the click feels slow”*, rarely makes it there.  
This gives those whispers a place to go.

## How it works (the short version)  
1. You write your submission.  
2. The app ships four things: your words, your OS, your CPU, the app version.  
3. A small server catches it, checks you’re not a robot, queues it.  
4. A background worker writes the row to my sheet.  
5. I read, tally, and act.

**Client side implementation is available to read in the repository if interested in more details**

## Privacy promise  
No e-mail, no IP in the sheet, no tracking.  
If you want to be reached, put your contact in the message; otherwise I can’t reply.
