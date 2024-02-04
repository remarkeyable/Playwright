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

