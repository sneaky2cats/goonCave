# 🧰 Toolkit
> *This will be my toolkit.*

---

### 🔍 `curl` & `grep`
```bash
curl -sL mzelo.com | grep -iEC 5 browser|vpn|ip

    curl → Visit website & fetch page content
        -s = Silent mode → hides progress / errors → clean output
        -L = Follow redirects → loads final page if URL moves
    grep → Search & filter text from the output
        -i = Ignore case → matches Browser / BROWSER / browser
        -E = Extended regex → allows | (OR) in search terms
        -C 5 = Context → shows 5 lines before + after every match
        browser|vpn|ip = Keywords → search for any of these words

    📌 Format: curl [options] [url] | grep [options] [terms]
