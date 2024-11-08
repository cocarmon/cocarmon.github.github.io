[Home](index.md) | [About](about.md) | [Contact](contact.md)

### Welcome to my portfolio
I am a full-stack developer, primarily operating in the javascript and python ecoystem. I have an interest peaking behind the curtain and working with lower level
optimizations, sometimes outsourcing to c when needed. I am most motivated by impact and curisoity these two traits lead to me spending a lot of time building personal projects.

[Personal Projects](#)
- [Reddit Syntax Highlighting](#reddit-syntax-highlighting)
- [Uplink](#uplink)
- [Calentics](#calentics)
- [Live Streaming](#live-streaming)
- [Snake Game](#snake-game)

---


[Open Source Contributions](#)
- [Vitess](#)

[Articles](#)
- [Vitess](#)

## Reddit Syntax Highlighting
Peak Users: 11
Date: May 8, 2024
url: [Chrome Webstore](https://chromewebstore.google.com/detail/reddit-syntax-highlightin/pifeljijalbijipppemldffoinofnelf?hl=en-US)
### Description
As a Reddit user, I often found it frustrating to read code snippets shared by other users due to inconsistent formatting. To address this, I created a Chrome extension that adds syntax highlighting based on the programming language, making code snippets on Reddit more readable.

How it works:
- I setup a [content script](https://developer.chrome.com/docs/extensions/develop/concepts/content-scripts) to fire whenever the active tab domain matches this pattern "https://www.reddit.com/r/*"
- Reddit is a single-page application (SPA), which makes injecting code more challenging than on traditional websites. Since SPAs rerender dynamically, injected code can be erased multiple times.
- To handle this, I used a MutationObserver to monitor changes in the DOM and apply a callback whenever the document updates.
- Reddit marks any pasted code with `<pre>` tags, so my script loops through the document on each DOM change to check for this tag.
- When a `<pre>` tag is found, I apply syntax highlighting using a minified version of highlight.js with pre-selected languages and retrieve the current theme from chrome.storage.local.
- An optimization I implemented was adding a highlighted attribute to `<pre>` tags after applying highlighting. This allowed the script to quickly check for the attribute before reapplying, improving efficiency. Since the MutationObserver monitors the entire document, this optimization roughly doubled performance, providing a seamless user experience.


Key Features:
- Automatic Detection and Highlighting: Automatically detects code blocks and applies syntax highlighting without any manual intervention.
- Wide Range of Languages Supported: Supports a diverse array of programming languages, ensuring that whether you're looking at Python, JavaScript, TypeScript, Java, CPP, and many more! 
- Customizable Themes: Choose from multiple highlighting themes to customize the appearance of code blocks according to your preference and comfort.

## Uplink
Peak Users: 48
Date: September 30, 2022
url: [Chrome Webstore](https://chromewebstore.google.com/detail/uplink/nododegcpoanlijiclligefbpmnhdham)
### Description
I had this idea during my internship at Playlister. As Playlister was a startup so we all wore multiple hats and I had some customer facing roles like support and some demos. At the time we kept a live document full of links that we could switch too, but this was kind of a pain. As I would have to find the active tab in a sea of tabs switch to it, find the link, and then switch back to my other tab. So I built a chrome extension to handle this for me, I could hit a key command it would open automatically

How it works:
- I setup a [content script](https://developer.chrome.com/docs/extensions/develop/concepts/content-scripts) to fire whenever the active tab domain matches this pattern "https://www.reddit.com/r/*"
- Reddit is a single-page application (SPA), which makes injecting code more challenging than on traditional websites. Since SPAs rerender dynamically, injected code can be erased multiple times.
- To handle this, I used a MutationObserver to monitor changes in the DOM and apply a callback whenever the document updates.
- Reddit marks any pasted code with `<pre>` tags, so my script loops through the document on each DOM change to check for this tag.
- When a `<pre>` tag is found, I apply syntax highlighting using a minified version of highlight.js with pre-selected languages and retrieve the current theme from chrome.storage.local.
- An optimization I implemented was adding a highlighted attribute to `<pre>` tags after applying highlighting. This allowed the script to quickly check for the attribute before reapplying, improving efficiency. Since the MutationObserver monitors the entire document, this optimization roughly doubled performance, providing a seamless user experience.


Key Features:
- Automatic Detection and Highlighting: Automatically detects code blocks and applies syntax highlighting without any manual intervention.
- Wide Range of Languages Supported: Supports a diverse array of programming languages, ensuring that whether you're looking at Python, JavaScript, TypeScript, Java, CPP, and many more! 
- Customizable Themes: Choose from multiple highlighting themes to customize the appearance of code blocks according to your preference and comfort.
  
## Calentics

Description of the Calentics project...

## Live Streaming

Description of the Live Streaming project...

## Snake Game

Description of the Snake Game project...

