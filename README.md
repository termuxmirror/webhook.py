# webhook.py

```bash
wget https://raw.githubusercontent.com/termuxmirror/webhook.py/main/webhook-0.2.tar.gz
```

main.py

```python
import os
from webhook import api

def msg():
    global message
    message = input("Geben Sie die Nachricht ein: ")

def url():
    global url
    url = input("Geben Sie die URL ein: ")

def info():
    print("Nachricht:", message)
    print("URL:", url)

def send():
    api.send_message(url, message)

def main():
    print("Willkommen bei Webhook!")
    while True:
        command = input("webhook@send>> ")
        if command == "msg":
            msg()
        elif command == "url":
            url()
        elif command == "info":
            info()
        elif command == "send":
            send()
        elif command == "exit":
            break
        else:
            print("Ungültiger Befehl")

if __name__ == "__main__":
    main()
```