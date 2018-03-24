# AngstromCTF2018_XOR

## XOR Challenge

We found these mysterious symbols hidden in ancient (1950s-era) ruins. We think a single byte may be key to unlocking the mystery. Can you help us figure out what they mean?  
  
Hint: "I cancel myself out, create from nothing, and negate from everything. What am I?" The hint answer I think is XOR which doesn't really help solve this as the title of the challenge gives this away.  

Alright, so clicking the link leads us to a page which just has this string:    
`fbf9eefce1f2f5eaffc5e3f5efc5efe9fffec5fbc5e9f9e8f3eaeee7`  
  This looked to be hexadecimal. I checked on Cryptii.com and this is what this is in binary:  
`11111011 11111001 11101110 11111100 11100001 11110010 11110101 11101010 11111111 11000101 11100011 11110101 11101111 11000101 11101111 11101001 11111111 11111110 11000101 11111011 11000101 11101001 11111001 11101000 11110011 11101010 11101110 11100111`  
# How XOR works
XOR works by taking two binary numbers and comparing them and outputting based on the comparison. 
From the http://www.xcprod.com
> The binary XOR (exclusive OR) operation has two inputs and one output. It is like the ADD operation which takes two arguments (two inputs) and produces one result (one output). The inputs to a binary XOR operation can only be 0 or 1 and the result can only be 0 or 1.
  
To clarify, if we "add" or combine in an XOR function,   
  1 + 1 = 0  
  1 + 0 = 1  
  0 + 1 = 1  
  0 + 0 = 0  


  
  Well, we know that the the first letter of our flag is a lower case a with the binary value of `01100001` and the first bit of hex is `11111011`. We need to find the key that will change this to an `a`.  
  We will just work through this backwards. To put 11111011 through a XOR function and get 01100001 on the other side we would use 10011010 as the key. I converted this to hex which is 9a. I ran this on Crytii and got the key!  
  
![Image of Capture](https://github.com/BicNasty/AngstromCTF2018_XOR/blob/master/Xor%20Challenge.png)  
  # Great Success.
