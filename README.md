# dwshare
dwshare is a simple, no-nonsense utility designed for Linux users (optimized for Debian) who need to move files from their computer to a mobile device over a local network without relying on cloud services or USB cables.

It bridges the gap between the power of the terminal and the convenience of a GUI. By utilizing Python’s built-in HTTP server, it turns any directory into a temporary local website accessible by any device with a browser.

Key Features:

  - One-Click Sharing: Instantly spins up a local server and displays a large, easy-to-read URL/IP address for your mobile device.

  - Integrated Firewall Handling: Includes logic to automatically disable/enable the ufw firewall (via [dwexec](https://github.com/DiogenesN/dwexec).) to ensure the connection isn't blocked by system security settings.

  - Zero-Footprint: Uses standard system tools. No heavy background services or proprietary protocols are required.

  - Privacy-Focused: Transfers occur entirely over your local Wi-Fi network. Your data never touches the internet.

  - Safety First: Features a "Close connection" trigger that kills the Python process immediately, ensuring your files aren't left exposed on the network when you're finished.

# Installation/Usage
  1. Install the following libs:

	     yad
	     grep
	     python3
	     coreutils
  optional but recommended: [dwexec](https://github.com/DiogenesN/dwexec).

  2. Open a terminal and run:

		 chmod +x ./dwshare
		
  3. Copy the script to /usr/local/bin:
  
		 sudo cp ./dwshare /usr/local/bin/

  4. Launch the app:

         dwshare

  5. Click 'Connect' and you'll get the dialog with an IP address as on the second screenshot. Now open your phone (should be connected to the same network), open a web browser on your phone, type in the IP address you see in the dialogue and (if firewall is disabled) you'll get all the files from your PC shown in your browser on your phone. You can download them into your phone. Note it downloads files only, if you want to download a folder then you should archive it first. 

# NOTE:
  1) All your devices should be connected to the same network.
  2) If you have any firewall installed then either first disable it or if you install [dwexec](https://github.com/DiogenesN/dwexec). and your firewall is ufw, then simply click on 'Disable firewall' and it will disable ufw automatically.

# Screenshots
 On the first app launch:
![Alt text](https://raw.githubusercontent.com/DiogenesN/dwshare/main/1.png)
 
 Successfully connected:
![Alt text](https://raw.githubusercontent.com/DiogenesN/dwshare/main/2.png)

This is what it looks like when browsing your PC files from your phone:
![Alt text](https://raw.githubusercontent.com/DiogenesN/dwshare/main/3.jpg)

That's it!

# Support

   My Libera IRC support channel: #linuxfriends
   
   Email: nicolas.dio@protonmail.com
