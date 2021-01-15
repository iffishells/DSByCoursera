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
