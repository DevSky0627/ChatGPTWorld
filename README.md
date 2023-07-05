# ChatGPT-web
[![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/Niek/chatgpt-web/pages.yml?style=flat-square)](https://github.com/Niek/chatgpt-web/actions/workflows/pages.yml)
[![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg?style=flat-square)](https://standardjs.com)
[![GitHub](https://img.shields.io/github/license/Niek/chatgpt-web)](/LICENSE)
[![All Contributors](https://img.shields.io/github/all-contributors/Niek/chatgpt-web?color=ee8449&style=flat-square)](#contributors)

## **URL**: https://niek.github.io/chatgpt-web/

![Screenshot of ChatGPT-web](.github/screenshot.png)


ChatGPT-web is a simple one-page web interface to the OpenAI ChatGPT API. To use it, you need to register for [an OpenAI API key](https://platform.openai.com/account/api-keys) first. All messages are stored in your browser's local storage, so everything is **private**. You can also close the browser tab and come back later to continue the conversation.

## Features
* **Open source**: ChatGPT-web is open source ([GPL-3.0](/LICENSE)), so you can host it yourself and make changes as you want.
* **Private**: All chats and messages are stored in your browser's local storage, so everything is private.
* **Customizable**: You can customize the prompt, the temperature, and other model settings. Multiple models (including GPT-4) are supported.
* **Cheaper**: ChatGPT-web uses the commercial OpenAI API, so it's much cheaper than a ChatGPT Plus subscription.
* **Fast**: ChatGPT-web is a single-page web app, so it's [fast and responsive](https://pagespeed.web.dev/analysis/https-niek-github-io-chatgpt-web/8xv5uwrnes).
* **Mobile-friendly**: ChatGPT-web is mobile-friendly, so you can use it on your phone.
* **Voice input**: ChatGPT-web supports voice input, so you can talk to ChatGPT. It will also talk back to you.
* **Pre-selected prompts**: ChatGPT-web comes with a list of [pre-selected prompts](https://github.com/f/awesome-chatgpt-prompts), so you can get started quickly.
* **Export**: ChatGPT-web can export chats as a Markdown file, so you can share them with others.
* **Code**: ChatGPT-web recognizes and highlights code blocks and allows you to copy them with one click.
* **Desktop app**: ChatGPT-web can be bundled as a desktop app, so you can use it outside of the browser.

## Development

To run the development server, run

```bash
npm ci
npm run dev # or: npm run build
```

To update the [`awesome-chatgpt-prompts`](/src/awesome-chatgpt-prompts/) subtree, run :
```bash
git subtree pull --prefix src/awesome-chatgpt-prompts https://github.com/f/awesome-chatgpt-prompts.git main --squash
```

## Use with Docker compose

```bash
docker compose up -d
```

## Mocked api
If you don't want to wait for the API to respond, you can use the mocked API instead. To use the mocked API, edit the `.env` file at root of the project ans set the key `VITE_API_BASE=http://localhost:5174` in it. Then, run the `docker compose up -d` command above.

You can customize the mocked API response by sending a message that consists of `d` followed by a number, it will delay the response the the specified number of seconds. You can customize the length of the response by including `l` followed by a number, it will return a response with the specified number of sentences.
For example, sending the message `d2 l10` will result in a 2 seconds delay and 10 sentences response.

## Desktop app

You can also use ChatGPT-web as a desktop app. To do so, [install Rust first](https://www.rust-lang.org/tools/install). Then, simply run `npm run tauri dev` for the development version or `npm run tauri build` for the production version of the desktop app. The desktop app will be built in the `src-tauri/target` folder.

</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->
