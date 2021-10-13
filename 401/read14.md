# BCrypt

## Hashed password solutions fall short
Many password solutions simply are not good enough and put your data and resources at risk.

1. **Plain text passwords:**
>As its name infers, a plain text password makes use of only letters. Should a hacker gain access to passwords such as these, they can easily pose as a user on your system.

2. One way hash
> With a one-way hash password, a server does not store plain text passwords to authenticate a user. Here, a password has a hashing algorithm applied to it to make it more secure. 


3. ‘Salting’ the password
> A ‘salt’ adds a very long string of bytes to the password. So even though a hacker might gain access to one-way hashed passwords, they should not be able to guess the ‘salt’ string.

4. Random ‘salt’ for each user
>  This will increase encryption significantly as hackers will have to try to find a password for a single user at a time.


## The BCrypt Solution

- `BCrypt` is based on the Blowfish block cipher cryptomatic algorithm and takes the form of an adaptive hash function.
- Using a `Key Factor`, `BCrypt` is able to adjust the cost of hashing. With Key Factor changes, the hash output can be influenced.
- This Key Factor will continue to be a key feature as computers become more powerful in the future. 
- It compensates for these powerful computers and slows down hashing speed significantly. 
- Ultimately slowing down the cracking process until it’s no longer a viable strategy.
<hr>

## **Hashing Passwords: One-Way Road to Security**
A strong password storage strategy is critical to mitigating data breaches that put the reputation of any organization in danger. Hashing is the foundation of secure password storage.

- Storing Passwords is Risky and Complex
    - A simple approach to storing passwords is to create a table in our database that maps a username with a password. 
    - When a user logs in, the server gets a request for authentication with a payload that contains a username and a password. 
    - We look up the username in the table and compare the password provided with the password stored. 
    - A match gives the user access to the application.


- What's Hashing About?

>*In cryptography, a hash function is a mathematical algorithm that maps data of any size to a bit string of a fixed size. We can refer to the function input as message or simply as input.*

>The fixed-size string function output is known as the hash or the message digest. As stated by OWASP, hash functions used in cryptography have the following key properties:

    - It's easy and practical to compute the hash, but "difficult or impossible to re-generate the original input if only the hash value is known."
    - It's difficult to create an initial input that would match a specific desired output.


![img](https://images.ctfassets.net/23aumh6u8s0i/ES2U6Gx7w0yVF9Asidr26/75531c3695f09272142b543a94acc0de/hash-flow)

- Cryptographic Hash Functions are Practically Irreversible
>Hash functions behave as one-way functions by using mathematical operations that are extremely difficult and cumbersome to revert such as the modulo operator.

- A Small Change Has a Big Impact
```java
from hashlib import sha256
h = sha256()
h.update(b'<STRING>')
hash = h.hexdigest()
print(hash)
```
- Using Cryptographic Hashing for More Secure Password Storage
> Whereas the transmission of the password should be encrypted, the password hash doesn't need to be encrypted at rest. When properly implemented, password hashing is cryptographically secure. `This implementation would involve the use of a salt to overcome the limitations of hash functions.`



- Limitations of Hash Functions
> The attacker could then either steal the cleartext password from the user through modern phishing and spoofing techniques or try a brute force attack where the attacker inputs random passwords into the hash function until a matching hash is found.


- No Need for Speed
> A well-intended user won't have a noticeable performance impact when trying a single valid login.

- Collision Attacks Deprecate Hash Functions
![IMG](https://images.ctfassets.net/23aumh6u8s0i/42yHOvIZclBjHBUuWRIXDN/de827a6af59f7a647db421daea5bce3c/Collision-illustrated)

### Summary:
- The core purpose of hashing is to create a fingerprint of data to assess data integrity.
- A hashing function takes arbitrary inputs and transforms them into outputs of a fixed length.
- To qualify as a cryptographic hash function, a hash function must be pre-image resistant and collision resistant.
- Due to rainbow tables, hashing alone is not sufficient to protect passwords for mass exploitation. To mitigate this attack vector, hashing must integrate the use of cryptographic salts.
- Password hashing is used to verify the integrity of your password, sent during login, against the stored hash so that your actual password never has to be stored.
- Not all cryptographic algorithms are suitable for the modern industry. At the time of this writing, MD5 and SHA-1 have been reported by Google as being vulnerable due to collisions. The SHA-2 family stands as a better option





