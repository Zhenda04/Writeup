# swampCTF 2025
<img src="image.png" alt="swampCTF logo" width="300" height="300">

I was invited by my friend to join swampCTF 2025 this weekend. I immediately accpet the inviation just because the logo is soooooo CUTEEEE! >3<

## Forensic
### Homework Help (50 pts)
 >I accidently lost some of my class notes! Can you help me recover it? (Note: Unzipped size is 4GB)

 ![FTKimager](image-1.png)

 Open the downloaded image file in the FTK imager. Since the question mentioned about class notes. Navigate to **\school\Hacking**, there are a few deleted notes in it, export the '**Hacking Notes.docx**'. 

 ![Note content](image-2.png)

 Once exported open the docx file, and the flag found.

 `swampCTF{n0thing_i5_3v3r_d3l3t3d}`

 ### Preferential Treatment (150 pts)
  >We have an old Windows Server 2008 instance that we lost the password for. Can you see if you can find one in this packet capture?

![Wireshark](image-3.png)

From the downloaded .pcap file. Follow the TCP stream for any packets. From the stream there is a cpassword, which is used for setting passwords from the Group Policy Preferences (GPP) and this can be easily decrypte using the gpp-decrypt tool.

![gpp-decrypt](image-4.png)

Copy the cpassword and decrypt it using gpp-decrypt and the flag found.

`swampCTF{4v3r463_w1nd0w5_53cur17y}`

 ### Planetary Storage (200 pts)
 >My friend found this strange file while perusing his computer, but we can't read it. Can you figure out what it is and get the information from it?

![check ldb content](image-5.png)

Check each of the .ldb file content and their payload. The file 000010.ldb payload have the flag. 

![alt text](image-6.png)

Decode the payload in cyberchef from Base64.

![alt text](image-7.png)

Decode the payload value with Base64 again and the flag found.

`swampCTF{1pf5-b453d-d474b453}`

 ### MuddyWater (200 pts)
 >We caught a threat actor, called MuddyWater, bruteforcing a login for our Domain Controller. We have a packet capture of the intrustion. Can you figure out which account they logged in to and what the password is?
 Flag format is swampCTF{username:password}








