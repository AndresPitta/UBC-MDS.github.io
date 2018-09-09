---
layout: page
title: Slack usage guidelines
---

## The Slack app

We will be using [Slack](https://slack.com/) as our primary means of electronic communication in the MDS program. We will invite you to our Slack workspace when the program starts.


#### Channels

Our Slack workspace, `UBC-MDS`, contains many _channels_ for conversation. We will enrol you in the channels for the 25 MDS courses, as well as [#data-science-careers](https://ubc-mds.slack.com/messages/data-science-careers/details/), [#git-general](https://ubc-mds.slack.com/messages/git-general/details/), [#python-general](https://ubc-mds.slack.com/messages/python-general/details/) and [#r-general](https://ubc-mds.slack.com/messages/r-general/details/). You should be automatically enrolled in the [#general](https://ubc-mds.slack.com/messages/general/details/) and [#random](https://ubc-mds.slack.com/messages/random/details/) channels when you join Slack.

These channels are all public. You can create private channels as well. For example, each year the students
typically create a private channel for students only. At some point we will also invite you to the UBC MDS Alumni Slack workspace, which is completely disconnected from the main UBC MDS Slack workspace you use as a student.


#### Direct Messages

A direct message thread is different from a private channel. To open a direct message, go to "Direct Messages" on the left-hand sidebar and click on the little `+` sign. Then, type in the names of the people who should be part of the direct message thread.


#### Usernames

Unlike other messaging platforms you might be used to, the namespace of usernames is specific to an individual Slack workspace. In other
words, if your name is Jamie it's perfectly fine to have your username be `@jamie` even though there are certainly a lot of Jamies out
there in the world and you might have no hope to get `jamie@gmail.com` or a CWL of `jamie`, etc. As long as you are the only `jamie` in UBC-MDS, you're good. It's generally easier to figure out who's who
if we all keep our usernames simple. If you've already created a complicated username, you can change it at any time; see instructions [here](https://get.slack.help/hc/en-us/articles/216360827-Change-your-username).


#### Formatting

Slack has a lot of nice features for formatting text, links, etc. For MDS, one important feature is for formatting code within Slack.
To do this, we use the single backtick (`` ` ``) and triple backtick (```` ``` ````), for inline code and code blocks respectively. As it
turns out, these conventions are the same in Markdown! Here is a `some inline code` and here is a code block:

```
First line
Second line
etc.
```

#### Browser vs. desktop app
Slack can be accessed via the [web interface](https://ubc-mds.slack.com) or via the [desktop app](https://slack.com/downloads/). You are free to decide which one you prefer. We do suggest that you consider the desktop version, however, since we will be using Slack so much in the program. There is also a mobile app for your phone, if you want to be extra connected.


#### Notifications
We don't want to wake you up with our Slack annoucements! You can edit your notification settings by clicking on the "UBC-MDS" at the upper-left and selecting "Preferences". From here you can decide how invasive you want Slack to be. One useful feature is the Do Not Disturb period, which by default is from 10 PM to 8 AM. If you have different hours you may want to adjust this accordingly.

Sometimes we will use `@students` when we make announcements that we want all students to receive. This has the same effect as directly mentioning everyone in the `students` user group and will make it more likely for you to receive a notification. However, once again, we don't want to wake you up to read these announcements immediately! We just want you receive them reasonably soon. Please set your notification preferences accordingly.

#### Reactions

On the subject of notifications, one nice feature of Slack is the reactions. Anyone can react to a message by anyone else, for example with a thumbs up emoji. This is different from sending a message containing that emoji in that it doesn't trigger notifications. This is hugely helpful. For example, if someone tells you something and you just want to say "OK" or "thanks", try a reaction instead of a new message, since you don't really need to notify the person of your response -- they will see it next time they are on Slack. Reactions are also useful when a large number of people need to respond affirmatively to something. For example if I ask "who is available to study Thursday night?" and then 30 people respond with "me!" -- well, that triggers a lot of notifications. Instead, if someone reacts with a check mark then others can simply click the check mark to add to the reaction. This way everyone can see who is available without any notifications being triggered. 


## Using Slack to ask for help in MDS

#### Asking about the course content

One reason we use Slack is so that you can ask for help. If you have a general question that is not about your specific situation or work, **we strongly encourage you to post it in a public course channel or the #general channel.** If you message us privately we may ask you to re-post in a public channel.
The reason for this is that often many students have the same question and it is much more efficient to have them answered in a public forum. Beyond that, it's often comforting for students to see other students asking questions,
and generally encourages a vibrant Slack ecosystem.

If you need to ask a course-related question privately, please open up a direct message thread with the lab instructor _and_ the TA(s) for the relevant course. This allows the most qualified/available person to answer, and also keeps the others up to date on what is happening in the course.

#### Asking a procedural question

If you want to ask a procedural question (not about the material, for example asking to reschedule a quiz due to an important event or job interview) then you can leave out the TA(s) and just communicate with the lab instructor.


#### Asking about your marks

If you have a question about how your lab or quiz was marked, please contact the TA who marked it. Typically, this will be the person who opens the notification issue in your personal grades repository.

#### How to ask

We illustrate best practices via two examples.


##### Example of a bad post

> @instructor For question 1(b) I get an error when I run the code, should I try removing missing data? Error: computer$ python test.py
Traceback (most recent call last):
  File "test.py", line 1, in <module>
    hello, world
NameError: name 'hello' is not defined

This post is problematic for the following reasons:

- it tags the instructor for no particular reason. The question could just as likely be answered by the TAs or other students.
- it does not provide context, or a link to the lab in question.
- it asks whether something should be tried, even though the student could have tried this before asking.
- the code and error message are not formatted properly with `code font`.
- the actual command used to run the code is not specified.


##### Example of a good post

> For question 1(b) I get the following error when I run the code with `python test.py`:
```
computer$ python test.py
Traceback (most recent call last):
  File "test.py", line 1, in <module>
    hello, world
NameError: name 'hello' is not defined
```
> I tried the approach suggested by @otherstudent above, and I also tried removing missing data but the problem wasn't solved. Any help appreciated. Link: https://github.ubc.ca/mds-org/DSCI_513_database-data-retr_students/blob/master/labs/lab2/lab2.md#1b

This post is well-crafted for the following reasons:

- a link to the lab is provided. Note that if the lab is an `.md` or `.Rmd` file then you can link to the actual question itself, but if it's a `.pdf` or other formats then you can only link to the top of the document.
- the specific error message is given.
- the student made a reasonable effort to solve the problem but still encountered difficulties.
- it indicates that the student has read the preceding conversation and is still stuck.
- The code and error message are formatted properly.
- the actual command used to run the code (`python test.py`) is specified.

#### Where to ask

Slack is intended for ephemeral content. If you have a question/post/comment that may be useful in the long-term, please
instead open an Issue in the students repo of the relevant course on GitHub. Examples of content that is better posted on GitHub include:

- useful resources/readings that the instructor may want to add to the course README for future years.
- hints/workarounds/fixes for the labs that the instructor may want to incorporate into the lab for current/future years.

Examples of content that are better posted on Slack include:

- a conceptual question about something covered in lecture/lab
- asking for help with a bug in your code

#### Privacy

Slack is not hosted on Canadian servers, and thus we recommend keeping the discussions and private messages on Slack to those related to course content, organization, etc. For personal and sensitive issues, communication between MDS students and instructional staff should be carried out using UBC email.
