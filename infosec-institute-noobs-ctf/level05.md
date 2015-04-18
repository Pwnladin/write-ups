# Level 5

- Download `aliens.jpg`
- Analyze with StegHide

```sh
root@sanctuary:~/ctf/Infosec Institute n00bs CTF Labs/level5# steghide --info aliens.jpg
"aliens.jpg":
  format: jpeg
  capacity: 4.2 KB
Try to get information about embedded data ? (y/n) y
Enter passphrase:
  embedded file "all.txt":
    size: 201.0 Byte
    encrypted: rijndael-128, cbc
    compressed: yes
root@sanctuary:~/ctf/Infosec Institute n00bs CTF Labs/level5# steghide extract -sf aliens.jpg -xf all.txt
Enter passphrase:
wrote extracted data to "all.txt".
root@sanctuary:~/ctf/Infosec Institute n00bs CTF Labs/level5# cat all.txt
01101001011011100110011001101111011100110110010101100011010111110110011001101100011000010110011101101001011100110101111101110011011101000110010101100111011000010110110001101001011001010110111001110011
root@sanctuary:~/ctf/Infosec Institute n00bs CTF Labs/level5#
```

- Press enter for passphrase and convert binary to ascii

> Flag: `infosec_flagis_stegaliens`


