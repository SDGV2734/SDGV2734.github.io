---
Title: Try Hack Me (Crack the Hash)
categories: [SWS101, Try Hack Me CTF ]
tags: [SWS101]
---

### Topic: Crack the Hash

![Alt text](../image/crack.png)

Hello everyone! In this room we will be learning about cracking the hash

**Hash**: Hashing refers to the process of generating a fixed-size output from an input of variable size using the mathematical formulas known as hash functions. This technique determines an index or location for the storage of an item in a data structure.

#### Task1 Level 1

To crack the hash in this room I used crack station with is and online platform for cracking hashes.

    1. 48bb6e862e54f2a795ffc4e541caed4d

    2. CBFDAC6008F9CAB4083784CBD1874F76618D2A97 

    3. 1C8BFE8F801D79745C4631D09FFF36C82AA37FC4CCE4FC946683D7B336B63032

    4. $2y$12$Dwt1BZj6pcyc3Dy1FWZ5ieeUznr71EeNkJkUlypTsgbX1H68wsRom

    5. 279412f945939ba78ce0758d3fd83daa

![Alt text](../image/crackstation.png)

As you can see we could crach the hash for 1, 2, 3, and 5 but for 4 it came with an error so to check what was wrong with I tried googling it and I found out that it was a different type of hash  

![Alt text](../image/btype.png)

So therefore, it was a bcrypt hash and this type are more difficult to crack than compared to others. 

In the terminal I tried to know more about the hash so I used `hashid` command followed a parametre and I also added `\` infront of every `$` to make the hash see like a string.

![Alt text](../image/hashid.png)



    










