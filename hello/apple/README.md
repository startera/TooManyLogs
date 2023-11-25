# Challenge Description 
## To read this again, please use the command "cat README" while in the challenge folder

            ~~ OH NO! TOO MANY LOGS ~~

The year is 2083 and we just found that some IoT devices from the 
early 2000s have been erroring all this time!
Here at digital_goose_light_and_magic_(TM) industries we take our 
users seriously and it is finally time to patch them! 
You see, every day we are getting many requests from the devices
to our backend, however some are erroring and we need to have 
our engineers look more into what causes the errors.

Since we are running multiple servers, we have here in each directory
the logs for that server. Each file has a filename of the form
YEAR-MONTH-DAY-HOUR-MINUTE-SECOND.log
Each logged line is in CSV (comma separated values) of the form
client IP, base64(client request), status
status can be either "OK" (no error) or something else (error).

Here is an example line without error
1.2.3.4, dGhpcyBpcyBhIHRlc3QgcmVxdWVzdAo=, OK
and here is an example line with error
1.2.3.4, dGhpcyBpcyBhbiBlcnJvcmVkIHRlc3QgcmVxdWVzdAo=, something-went-wrong

Certainly a digital forensics investigator in training like you can
help! You will need to write commands (preferably in UNIX shell, but
if you can do it with any other language and provide correct answers,
that is fine with us*) to answer the following questions:

y) what is the md5sum of the .tar.gz file we sent you?
z) after decompressing the archive, what is the total size in MB of the dir containing this README?
a) How many directories are there and what are their names?
b) How many .log files are there in total in all the above directories?
c) How many .log files fall in the (inclusive) time range of March 2030 to November 2051 in all the above directories?
d) In total how many errored lines have been logged in all the directories?
e) How many entries do we have from IP addresses starting with 177 ? (belonging to the 177/8 subnet)
f) Can you give us a list of all the requests that errored along with their decoded message that caused the error for the server
   kCo6 during 2063-08-23-10-18-38?

Hints / commands that you might find useful:
 ls, grep, sort, wc, find, cut, base64, du, md5sum, date
 using pipes to chain commands and redirects to save/read to/from temporary files

Writing your report:
Please include at least screenshots with the commands that you run to get the result along with (at least) part of it's output.
Also please explain why you are using this command and what it does (or what you think it does).
If you get stuck and can't produce a result at least write what type of command you would try to find and
how you would want it to operate on the data in order to give you the correct result

Good luck! :)

*however if you avoid learning some shell commands now you will just have a harder time later in the course...
