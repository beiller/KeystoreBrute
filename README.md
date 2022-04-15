KeystoreBrute
=============
A program that uses a brute-force attack to find the password for a given .keystore file (Java KeyStore).

My Contributions (@beiller)
=============
I enabled a prefix, because I lost my password but knew the prefix. Example usage:

```
java se.bes.br.BruteMain ~/laydelmi.jks 1 16 myprefix
Breaking: /home/bill/laydelmi.jks
Characters to test: 83
abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ[[\{}| 0123456789-=!@#$%^&*()_+

Starting search for depth: 1

Starting search for depth: 2
Tested 5327 pws (15 s -- 298 pw/s):

Passphrase found: myprefix42
```

Took approx 30 seconds

Please note
-----------
Please note that this program will only try to find the password to the Keystore,
not to any of the keys inside.

Usage
-----
If you are using the binary found in the directory with the same name:

    java -jar Breaker.jar <keystore file> <startdepth> <number of threads>

If you are compiling the program yourself and want to use those classfiles:

    java se.bes.br.BruteMain <keystore file> <startdepth> <number of threads>

Performance
-----------
On Linux with a Core2Quad I got about 150000 keys / second, 
but on a Windows 7 machine (Also Core2Quad) I only got about 100000 keys / second.

Proof of concept
----------------
There is a .keystore file in the test/ directory that has been prepared with the
password 'abc123'. Feel free to try it out.