## MailPro
A command line tool notifying the user via email when a program finishes (the command and output of the program). Useful when running a time consuming program.

### Install (configure, more precisely)

First, make sure you have /usr/bin/mail and /usr/sbin/sendmail installed on your computer. If the following commands return paths, then they have been installed on your computer.

<code>which mail</code>

<code>which sendmail</code>

Second, <code>cd</code> to the folder containing mailpro and assgin executability to this shell program.

<code>chmod +x mailpro</code>

Third, add the following variables to your bash_profile (or alternatives such as bashrc and profile (default profile on Ubuntu)).

<code>export PATH="_the folder containing mailpro_:$PATH"</code>

<code>export MAILPRO_SUBJECT=_the subject you want to show in the email notifications_</code>

<code>export MAILPRO_ADDRESS=_the email address you want to receive the notifications_</code>

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

### ToDo (For Developers Only)

1. Show output on screen (terminal) as well as in the email.

2. Support other mailing commands such as mutt (for ones who don't have root privilege on servers like me).

3. Compose an iteractive Makefile to make it easier to configure the environment.
