# ActGPT - chatbot that controls browser

blog post: https://yihui.dev/actgpt

demo: https://twitter.com/he_yi_hui/status/1617328366876786688

config api key, chromedriver path and user data path in `conf/config.yaml`.

- API key is from OpenAI. You can get it from https://beta.openai.com/
- chromedriver path is where you have chromedriver installed. You can download it from https://chromedriver.chromium.org/downloads
- User data path is where your browser stores cookies, history, etc. You can use a new folder to avoid logging in to websites.

```
OPENAI_API_KEY: api_key
executable_path: /path/to/chromedriver
user_data_dir: /path/to/user_data
```

install `requirements.txt` then run `python3 demo.py` to start the chatbot.

### examples

search for "ChatGPT" on wikipedia. summarize and tweet on Tiwtter.

```
write code:
1. go to www.wikipedia.org
2. find all textboxes. find one from them that is visible
3. click on the textbox
4. type in "ChatGPT" + Keys.ENTER
5. sleep 3 seconds
6. find all elements that contains text longer than 50 characters
7. combine their text in a string `text` and print it
8. go to url 'www.twitter.com'
9. ask AI about "write a tagline tweet given:" + `text` and store it in variable `response`
10. find an element whose text is Tweet
11. find a textbox near the element
12. click the textbox
13. type in existing variable `response` + Keys.ENTER
14. click the element whose text is Tweet.
15. wait 3 seconds
16. find an element that has text longer than 50 characters
17. click on the nearest like button
```

Google search, write joke about search and tweet it

```
write code: 1. go to google. 2. find all textboxes. find one from them that is visible 3. click on the textbox 4. type in Andrej Karpathy and ENTER key
write code: 1. find all elements that contains text longer than 50 characters 2. store their text in `text` and print it
write code: 1. find all elements contain text 2. initialize an empty string 3. for each element, split the text into lines 4. for each line, if it's longer than 20 words, append it to the string
ask AI about "write a joke given:" + `text` and store it in variable `response`
write code: 1. go to twitter 2. find an element whose text is Tweet 3. find a textbox near the element 4. click the textbox 5. type in existing variable `response` 6. click the element
```

Amazon search

```
go to amazon
find all textboxes. find one from them that is visible
click on the textbox
type in "ChatGPT" and enter
```
