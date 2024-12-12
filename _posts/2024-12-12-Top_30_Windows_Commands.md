---
layout: post
title: 30 Windows Command Line Cheat Sheet
date: 07-12-2024
categories: [Windows]
tag: [Windows Commands, Windows Basics, Windows Guide, Windows Tips]
---

# 30 Windows Command Line Cheat Sheet

Welcome to your essential guide for mastering the Windows Command Line. Whether you're a beginner or an advanced user, these commands will help you manage files, folders, networks, and more. Let's dive into the core commands and their uses.

## A. Opening and Managing Files/Folders

1. Always open Command Prompt in Administrator Mode:
   ```
   runas /user:Administrator cmd
   ```
2. Hide zip or rar files inside an image:
   ```
   copy /b image.extension+folder.zip image.extension
   ```
3. Show all Wi-Fi passwords:
   ```
   netsh wlan show profile
   netsh wlan show profile wifinetwork key=clear | findstr "Key Content"
   ```
   ```
   for /f "skip=9 tokens=1,2 delims=:" %i in ('netsh wlan show profiles') do @if "%j" NEQ "" (echo SSID: %j & netsh wlan show profiles %j key=clear | findstr "Key Content") & echo.
   ```
4. Encrypt files in a folder:
   ```
   cipher /E
   ```
5. Save output of a command to a file:
   ```
   command >> output.txt
   ```
6. Hide a folder from everyone:
   ```
   attrib +h +s +r foldername
   attrib -h -s -r foldername
   ```

## B. System Information

7. Display detailed system information:
   ```
   systeminfo
   ```
8. Remove a mounted drive:
   ```
   subst /d q:
   ```
9. Securely copy files between remote hosts:
   ```
   scp file.txt root@serverip:~/file.txt
   ```
10. Change the background and text color in Command Prompt:

```
color 07 [background:text]
```

11. Change the prompt text:

```
prompt {text}$G
```

12. Map a regular folder as a mounted drive:

```
subst q: c://filelocation
```

13. Change the title of Command Prompt window:

```
title {stuff}
```

## C. Network

14. Curl the weather:

```
curl wttr.in/location
```

15. Check your public IP address:

```
curl checkip.amazonaws.com
```

16. Curl shortened links to figure out the destination:

```
curl --head --location "https://samurai1337x.github.io/"
```

17. Generate a QR code:

```
curl qrenco.de/https://samurai1337x.github.io
```

18. Check the status of a website:

```
curl -IsL http://samurai1337x.github.io/ | findstr ^Location
```

## D. Social Media and ChatGPT

19. Check latest social media posts:

```
curl -s https://decapi.me/youtube/latest_video?user=samurai1337x
curl -s https://decapi.me/twitter/latest?name=samurai1337x
```

20. Define a word:

```
curl dict.org/d:contretemps
```

21. Use ChatGPT in CMD with Curl:

```
curl https://api.openai.com/v1/chat/completions -H "Authorization: Bearer sk-xxx" -H "Content-Type: application/json" -d "{\"model\": \"gpt-3.5-turbo\", \"messages\": [{\"role\": \"user\", \"content\": \"Who is NetworkChuck?\"}]}"
```

## E. File and Folder Management

22. Visit a website:

```
start www.samurai1337x.github.io
```

23. Telnet to a server:

```
telnet telehack.com
```

24. Delete temporary files to clear space:

```
del /q /f /s %temp%\\*
del /s /q C:\Windows\temp\*
```

25. View the history of commands:

```
doskey /history
```

## F. Windows Terminal

26. Use Windows Terminal instead of Command Prompt:

- Download and install Windows Terminal from the Microsoft Store or GitHub.
- Set your preferred terminal as the default in "Settings."

```
Open Windows Terminal, press Ctrl+Shift+T for a new tab.
```

27. Open Terminal from any folder:

```
Shift-right-click on the folder and select Terminal.
```

28. Drag and drop files into Terminal for the file path:

- Open Windows Terminal.
- Drag and drop the file into the terminal to paste its path.

29. Use PowerShell for advanced tasks beyond Command Prompt.
30. Get help in the terminal:

```
help
```

This cheat sheet is your go-to resource for Windows Command Line. With these commands, you can efficiently manage files, folders, systems, and networks. Bookmark this post for quick reference!
