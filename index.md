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
As a Reddit user, I often found it annoying reading code from other users as it was rarely good formatting to read code snippets posted in discussions. To solve this, I created a Chrome extension that adds syntax highlighting, improving readability for code on Reddit.

How it works:
- I setup a [content script](https://developer.chrome.com/docs/extensions/develop/concepts/content-scripts) to fire whenever the active tab domain matches this pattern "https://www.reddit.com/r/*"
- Reddit is a SPA, so this makes injecting harder than traditional websites. As SPA's can rerender multiple times erasing whatever you injected
- The solution is too use a MutationObserver to observe the elements and apply a callback on element/document change
- Reddit marks any pasted code with `<pre>` tag so we loop through the document on element changes to check for this tag
- If it's found we used a minified version of highlight.js with pre-selected languages and grab the current theme from chrome.storage.local and have it apply it
- A major optimization that I made was adding a highlighted attribute to the `<pre>` as I could then check for this on the `pre` to reduce highlighting the element multple times and this made it roughly ~2x faster and gave a seamless user experience


Key Features:
- Automatic Detection and Highlighting: Automatically detects code blocks and applies syntax highlighting without any manual intervention.
- Wide Range of Languages Supported: Supports a diverse array of programming languages, ensuring that whether you're looking at Python, JavaScript, TypeScript, Java, CPP, and many more! 
- Customizable Themes: Choose from multiple highlighting themes to customize the appearance of code blocks according to your preference and comfort.

## Uplink

Description of the Uplink project...

## Calentics

Description of the Calentics project...

## Live Streaming

Description of the Live Streaming project...

## Snake Game

Description of the Snake Game project...

