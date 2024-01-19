# Zukijourney API Documentation V2

>As of 12/15/2023:
>
>Request-Response pairs that are 99% similar to previous posts, such as repeating the same request multiple times, will receive the same response. This is in order to save up on usage.
>If the most recent message to the API is too short, too simple, or unnecessary,  that request, including all previous usage, will be handled by Mistral-Instruct-v0.1. This is to avoid unnecessary waste of previous GPT resources.
>The Api-Key you receive is IP-LOCKED. You can only use your key from one IP at a time. In order to change that IP, use the /resetip command. Automation of /resetip is illegal.  Also, IP-Lock is disabled for subscribers.
>Leaving this server will result in your Api-Key being suspended. Rejoining will not fix this, unless I am notified of the situation.
>Alt accounts & DDosing the API will be punished, and automatic punishment measures are in place for this. Only one account per person, and do not overuse/overstress the API.
>The Midjourney implementation works based off of the showcase, finding the most matching image. Sometimes, it may not find anything that matches.
>I reserve the right to remove access, premium, or anything related to this API for any reason whatsoever I wish for.

## Generalized Overview

- FastAPI docs: [Zukijourney API Documentation](http://zukijourney.xyzbot.net/docs)
- OpenAI docs (closest reference): [OpenAI API Reference](https://platform.openai.com/docs/api-reference)

## Code Samples

### Python - All Possible Endpoints

Install the required library:

```bash
pip install openai==0.28.1
```

```python
import openai

openai.api_key = "<your key, obtain it with /key on @zuki.api>"
openai.api_base = "https://zukijourney.xyzbot.net/v1"  # or "https://zukijourney.xyzbot.net/unf"

# Example for Embedding endpoint
response = openai.Embedding.create(input="hello world!", model="balls")
print(response)

# Example for Image endpoint
response = openai.Image.create(prompt="a circle", n=1, size="1024x1024")
print(response)

# Example for Chat Completion endpoint
chat_completion = openai.ChatCompletion.create(
    stream=False,
    model="gpt-4",
    messages=[
        {
            "role": "user",
            "content": 'There are 50 books in a library... [full message]',
        },
    ],
)
print(chat_completion.choices[0].message.content)


```

### Community-Contributed Code Samples

- JavaScript: [zukijs](https://github.com/Sabsterrexx/zukijs)
- Java: [zukiJava](https://github.com/Sabsterrexx/zukiJava)
- Python: [zukiPy](https://github.com/Launchers-1/zukiPy)
- TypeScript: [zukiTS](https://github.com/eL1fe/zukiTS)



## Notices

- All available chat models: [Chat Models](https://zukijourney.xyzbot.net/v1/models)
- All available image models: [Image Models](https://zukijourney.xyzbot.net/models/images)
- No model selection for specific endpoints.
- Current model status: [Model Status](https://zukijourney.xyzbot.net/status)
- Function calling and moderation endpoint not supported.


## Limits & Premium Information

### API Usage Limits

- @supporters: 1/sec, 3/min, 200/day
- @donators & @boosters: 1/sec, 8/min, 789/day
- @subscribers: 11/min

### How to Get Premium Role

- @boosters: Boost the server.
- @donators: Donate $5 or more via [Ko-fi](https://ko-fi.com/zukixa).
- @subscribers: Donate $5 or more (one-time) and have a recurring donation via [Ko-fi](https://ko-fi.com/zukixa).



## Premium Notices

- Enterprise benefits for significant donations.
- Benefits in the @Jake Landau (zuki.gm) bot for donors.
- Special endpoint for NSFW RP with different GPT/Claude resources.



## TL;DR - How to Use the API

- **API URL:** [Chat Completions API](https://zukijourney.xyzbot.net/v1/chat/completions) or [Unf Chat Completions API](https://zukijourney.xyzbot.net/unf/chat/completions)
- **API Key:** Obtain from the /key command on @zuki.api bot.
- **Rate Limits:** Review [here](#limits--premium-information).
- **Donations:** [Ko-fi](https://ko-fi.com/zukixa) or via crypto.

## HOW TO GET PREMIUM ROLE?

- @boosters (the rich) can be achieved by boosting [this discord server](https://discord.gg/zukijourney). Both Boosts are necessary for successful validation of premium.
- @donators (the ily'all) can be achieved by a one-time donation of $5 or more via [Ko-fi](https://ko-fi.com/zukixa) -- where the donation will grant you the required role.
- @subscribers (the o7 <333333) can be achieved by a one-time donation of $5 or more  AND a recurring donation of $5 or more via [Ko-fi](https://ko-fi.com/zukixa)

Crypto payment is also available. Make a ⁠ticket in #tickets (on the discord) to coordinate such.

## More Documentation

For detailed information, refer to the provided links and documentation.

*Note: Replace placeholders such as `<your key>` with actual values.*
