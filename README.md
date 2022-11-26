
# 🚀 Simple Discord Webhook Spammer

Spam discord webhooks with a custom spam message


⚡ if this repo hits 10-15 stars i will make it better  by adding threading and make it faster and also add multi webhooks support
## Usage

```python
import time
import requests
from colorama import Fore
message = input("Spam Message: ")
url = input("WebHook URL: ")

def spam(message, url):
    while True:
        try:
            req = requests.post(url, json={'content': message})
            if req.status_code == 204:
                print(f"[{Fore.GREEN}+{Fore.WHITE}] Succesfully Sent {message}")
        except:
            print(f"[{Fore.RED}-{Fore.WHITE}] invalid webhook | " + url)
            print("closing in 5 seconds")
            time.sleep(5)
            exit()
loop = 1
while loop == 1:
    spam(message, url)


```

