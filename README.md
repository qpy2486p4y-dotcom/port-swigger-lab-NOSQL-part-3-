# port-swigger-lab-NOSQL-part-3-
looking at lab



Exfiltrating data in MongoDB!

https://insecure-website.com/user/lookup?username=admin
This results in the following NoSQL query of the users collection:

{"$where":"this.username == 'admin'"}
As the query uses the $where operator, you can attempt to inject JavaScript functions into this query so that it returns sensitive data. For example, you could send the following payload:

admin' && this.password[0] == 'a' || 'a'=='b


You could also use the JavaScript match() function to extract information. For example, the following payload enables you to identify whether the password contains digits:

admin' && this.password.match(/\d/) || 'a'=='b

1 log in and go through the source code and look for proof a cookie or token / anything rare is being passed through in short know how to read code 

2 open burp and send the login to repeater than send modify it with code i have given above or code from the other 2 labs you have learnt about 

3 make sure to url encode with ctrl u than swap user weiner to admin 

4 take a copy of the error massage and set up payload by putting number list and character's that are all lower case because it says it in the lab 

5 start attack and run through it than see error   ok let's look for a difference and piece together what the words are trying to say  

6 ok highlight if you get stuck and see that the password to administrator is clyiywzj 

GOOD JOB you are now 1% more professional 
