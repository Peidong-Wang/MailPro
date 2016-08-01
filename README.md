## MailPro
A command line tool notifying the user via email when a program finishes (the command and output of the program). Useful when running a time consuming program.

### Download

You may fork the source code of MailPro or simply download and extract **mailpro.tar.gz** to use MailPro. The following instructions work for both.

### Install (configure, more precisely)

<code>cd</code> to the folder containing mailpro. Then run <code>configure</code> as follows.

<code>./configure</code>

Set the email address to which you wish to send the notification and the subject (title) of the notification according to the guidance of the message shown on command line.

If an error occurs saying that executability is needed for <code>./configure</code>, grant executability with the following code.

<code>chmod u+x configure</code>

###Test

You may use the following command to test that mailpro has been successfully configured.

<code>mailpro expr 1 + 1</code>

The content of the message you received should be as follows.

> Command:
> 
> expr 1 + 1
> 
> Output:
> 
> 2

You may notice that the email is in your junk mail box. You may need to follow the steps in the next section.

###Avoiding Spam Filtering

I only tested on Gmail account, but it is very likely that there are similar methods with other mainstream email service providers.

First, log on your Gmail account using a web browser.

Second, find the test message you received in the previous step in "More->Spam".

Third, click on the tag near the title of your email, which means that this email is important.

With the configuration in this section, you will find your notification email goes into the ordinary mailbox.

###Usage

The usage of mailpro is quite simple. Just add <code>mailpro</code> before any command.

<code>mailpro _your command_</code>

