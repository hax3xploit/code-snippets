# code-snippets
A Github repo containing python code snippets which I use approximately daily and to save time searching for them locally/via google.

---

### Script disable after time (stop_date).
```python3
import time
import datetime
import pytz
import undetected_chromedriver as uc
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC


stop_date = datetime.datetime(2023, 4, 15)
stop_time = datetime.time(4, 50)


pk_tz = pytz.timezone('Asia/Karachi')


current_time = datetime.datetime.now(pk_tz).time()

options = webdriver.ChromeOptions()
locations = ["Miami","tampa","Orlando","Gainesville","Miramar","Tallahassee","Hialeah"]
options = webdriver.ChromeOptions()
options.add_argument("start-maximized")
options.add_argument('--disable-blink-features=AutomationControlled')
driver = uc.Chrome(options=options)


if datetime.datetime.now(pk_tz).date() >= stop_date.date() and current_time >= stop_time:
    print("Script is disabled after the stop time.")
else:
```
