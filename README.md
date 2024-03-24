# Easy Peasy (picoctf)
## Description

** A one-time pad is unbreakable, but can you manage to recover the flag? (Wrap with picoCTF{}) nc mercury.picoctf.net 64260 otp.py **



```
└─$  nc mercury.picoctf.net 64260
```
```                  
******************Welcome to our OTP implementation!******************
This is the encrypted flag!
51466d4e5f575538195551416e4f5300413f1b5008684d5504384157046e4959

What data would you like to encrypt?

```
```
python3 -c "print('a'*49968);print('a'*32)" | nc mercury.picoctf.net 64260
```
```
******************Welcome to our OTP implementation!******************
This is the encrypted flag!
51466d4e5f575538195551416e4f5300413f1b5008684d5504384157046e4959

What data would you like to encrypt? Here ya go!
...
What data would you like to encrypt? Here ya go!
03463d190702003d195004133d190356433d1902503d1950563d1900513d1959

```
```
$ python
Python
Type "help", "copyright", "credits" or "license" for more information.
```
```
>>> ef=0x51466d4e5f575538195551416e4f5300413f1b5008684d5504384157046e4959
```
```
>>> ef = 0x51466d4e5f575538195551416e4f5300413f1b5008684d5504384157046e4959
```
```
>>> ea = 0x03463d190702003d195004133d190356433d1902503d1950563d1900513d1959
```
```
>>> a = 0x6161616161616161616161616161616161616161616161616161616161616161
```
```
>>> "{:x}".format(ef^ea^a)
```
>Output
```
'3361313639343464616434333237313763636333393435643364393634323161'
```

** Go to https://www.rapidtables.com/convert/number/hex-to-ascii.html form Hex to ASCII **

``Flag``
```
picoCTF{3a16944dad432717ccc3945d3d96421a}
```
