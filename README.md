# Playwright

<h3>Installation Pip</h3>

```
pip install playwright
playwright install
```


```python
from playwright.sync_api import sync_playwright

with sync_playwright() as p:
    browser = p.chromium.launch(headless=False)
    page = browser.new_page()
    page.goto("https://www.google.com")

```

<h2>Selector ID</h2>

```python
from playwright.sync_api import sync_playwright

with sync_playwright() as p:
    browser = p.chromium.launch(headless=False)
    page = browser.new_page()
    page.goto("https://demo.automationtesting.in/Index.html")

    email = page.wait_for_selector('#email')
    email.type('abc123@gmail.com')
    login_button = page.wait_for_selector('#enterimg')
    login_button.click()

    page.wait_for_timeout(3000)
```


<h2>Selector Attribute</h2>

```python
from playwright.sync_api import sync_playwright


with sync_playwright() as p:
    browser = p.chromium.launch(headless=False)
    page = browser.new_page()
    page.goto("https://opensource-demo.orangehrmlive.com/web/index.php/auth/login")

    #type #tagname
    username = page.wait_for_selector('input[name="username"]')
    username.type('admin')
    password = page.wait_for_selector('input[type="password"]')
    password.type('admin123')

    login = page.wait_for_selector('button[type="submit"]')
    login.click()

    page.wait_for_timeout(3000)
```

