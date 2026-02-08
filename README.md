<p align="center">

</p>

<h1></h1>
<br />


<h2>Video Demonstration</h2>

- ### [YouTube: Day 4 Lab Basic Device Security](https://www.youtube.com/watch?v=pXzjPI4rmYA)

<h2>Environments and Technologies Used</h2>

- Jeremy's IT Lab Youtube Channel
- Cisco Packet Tracer
  

  
<h2>Operating Systems Used </h2>

- Cisco IOS


<h2>Step-by-Step</h2>

<b>🟢 Part 1 — Set Hostnames</b>

- Click on the device (R1 or SW1).

- Select CLI to access the command line.

- Enter Privileged EXEC mode with enable or shortcut en.

- Enter Global Configuration mode with configure terminal or shortcut conf t.

- Set the router hostname: hostname R1.

- Set the switch hostname: hostname SW1.

<b>🟢 Part 2 — Set Enable Password</b>

- Stay in Global Configuration mode.

- Enter the command: enable password CCNA.

- This password will protect access to Privileged EXEC mode.

<b>🟢 Part 3 — Test Enable Password</b>

- Exit back to User EXEC mode using exit twice.

- Enter Privileged EXEC mode with enable.

- Type the password CCNA.

- If typed incorrectly three times, access will be denied (“bad secrets”).

- Enter correct password to access Privileged EXEC mode.

<b>🟢 Part 4 — View Password in Running Configuration</b>

- From Privileged EXEC mode, type: show running-config or shortcut sh run.

- Observe the enable password CCNA in clear text (unencrypted).

<b>🟢 Part 5 — Encrypt Passwords</b>

- Enter Global Configuration mode if not already in it: conf t.

- Enable encryption: service password-encryption.

- Check the running config from Privileged EXEC mode or using do show running-config if still in global config.

- Observe the password is now encrypted (type 7).

<b>🟢 Part 6 — Configure More Secure Enable Secret</b>

- In Global Configuration mode, enter: enable secret Cisco.

- This uses MD5 encryption (type 5), which is more secure than service password-encryption.

<b>🟢 Part 7 — Test Enable Secret</b>

- Exit back to User EXEC mode: exit twice.

- Enter Privileged EXEC mode with enable.

- Try old password CCNA — it will fail.

- Enter new enable secret password Cisco — it works.

<b>Note: If both enable password and enable secret exist, only enable secret works.</b>

<b>🟢 Part 8 — View All Passwords</b>

- From Privileged EXEC mode, type: show running-config.

- Observe:

- enable password (type 7 encryption)

- enable secret (type 5 / MD5 encryption)

<b>🟢 Part 9 — Save Running Configuration</b>

- Save current configuration to Startup Config with one of these commands:

- write

- write memory

- copy running-config startup-config

- Verify with: show startup-config.

- Confirm passwords and other configurations are saved.
