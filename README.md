# DSByCoursera

```python
import re
my_string = "My luck number are 8755 and 33"
```


```python
 #searing all the digit
print(re.findall(r"\d",my_string))

```

    ['8', '7', '5', '5', '3', '3']



```python
#use greedy appraoch
print( re.findall(r"\d+",my_string))
```

    ['8755', '33']



```python
#use group capturing
print( re.findall(r"(\d+)",my_string))
```

    ['8755', '33']



```python
#use group capturing

print( re.findall(r"(\d)",my_string))
```

    ['8', '7', '5', '5', '3', '3']



```python
#use group capturing
#this will capturing the first whole group then apply all the "+" appoacrh
print(re.findall(r"(\d)+",my_string))
```

    ['5', '3']



```python
#example Tweets sentiments Analysis
```


```python
import re
sentiment_analysis  = "'Just got ur newsletter, those fares really are unbelievable. Write to statravelAU@gmail.com or statravelpo@hotmail.com. They have amazing prices', 'I should have paid more attention when we covered photoshop in my webpage design class in undergrad. Contact me Hollywoodheat34@msn.net.', 'hey missed ya at the meeting. Read your email! msdrama098@hotmail.com'"
print(re.findall(r"([A-Za-z0-9]+)\@\S+",sentiment_analysis))
```

    ['statravelAU', 'statravelpo', 'Hollywoodheat34', 'msdrama098']



```python
# Write a regex that matches email
regex_email = r"([A-Za-z0-9]+)\@\S+"

for tweet in sentiment_analysis:
    # Find all matches of regex in each tweet
    email_matched = re.findall(regex_email, tweet)

    # Complete the format method to print the results
    print("Lists of users found in this tweet: {}".format(email_matched))
```

    Lists of users found in this tweet: ['statravelAU', 'statravelpo']
    Lists of users found in this tweet: ['Hollywoodheat34']
    Lists of users found in this tweet: ['msdrama098']



```python

```



 ## **Flying Home Case Study**
Your boss assigned you to a small project. They are performing an analysis of the travels people made to attend business meetings. You are given a dataset with only the email subjects for each of the people traveling.

You learn that the text followed a pattern. Here is an example:

Here you have your boarding pass LA4214 AER-CDB 06NOV.

You need to extract the information about the flight:

The two letters indicate the airline (e.g LA),
The 4 numbers are the flight number (e.g. 4214).
The three letters correspond to the departure (e.g AER),
The destination (CDB),
The date (06NOV) of the flight.
All letters are always uppercase.

The variable flight containing one email subject was loaded in your session. You can use print() to view it in the IPython Shell.


```python
import re

```


```python
flight = "Subject: You are now ready to fly. Here you have your boarding pass IS3723 AMS-MAD 06OCT Here you have your boarding pass IS3723 A3S-AAD 06OCT"
```


```python
regex = r"([A-Z]{2})(\d{4})\s([A-Z]{3})-([A-Z]{3})\s(\d{2}[A-Z]{3})"
```


```python
# Import re
import re

# Write regex to capture information of the flight
regex = r"([A-Z]{2})(\d{4})\s([A-Z]{3})-([A-Z]{3})\s(\d{2}[A-Z]{3})"

# Find all matches of the flight information
flight_matches = re.findall(regex, flight)
print(flight_matches)
    
#Print the matches
print("Airline: {} Flight number: {}".format(flight_matches[0][0], flight_matches[0][1]))
print("Departure: {} Destination: {}".format(flight_matches[0][2], flight_matches[0][3]))
print("Date: {}".format(flight_matches[0][4]))
```

    [('IS', '3723', 'AMS', 'MAD', '06OCT')]
    Airline: IS Flight number: 3723
    Departure: AMS Destination: MAD
    Date: 06OCT



```python

```


```python

```


```python

```
