# Auto-GPT Prompt Engineering:

Auto-GPT prompt engineering refers to the process of formulating effective prompts or instructions to interact with language models like GPT (Generative Pre-trained Transformer). These prompts help guide the model's output and improve the relevance, coherence, and accuracy of the generated text. Prompt engineering is crucial for fine-tuning models and achieving desired outcomes in various natural language processing (NLP) tasks.

Effective Prompt Engineering Strategies:

Clear and Specific Instructions: It is essential to provide explicit and unambiguous instructions to guide the model's behavior. Clearly define the task, desired output format, and any constraints. This helps the model understand the expectations and produce relevant responses.

Conditioning on Context: Incorporating relevant context into prompts can help the model generate more context-aware and coherent responses. By providing preceding sentences or context paragraphs, the model can better understand the context and generate more accurate and coherent outputs.

Control Tokens: Control tokens are special tokens that allow fine-grained control over the model's behavior. By incorporating control tokens within the prompt, specific attributes such as sentiment, style, or content can be influenced. This enables precise control over the generated text and helps tailor the output to desired characteristics.

Systematic Comparison: A useful strategy in prompt engineering involves systematically comparing different approaches or options. By explicitly instructing the model to compare and contrast various aspects, it can generate informative and structured responses, aiding decision-making processes or analysis.

Iterative Refinement: Prompt engineering often involves an iterative process of experimentation and refinement. It is common to start with simple prompts and gradually add complexity or adjust instructions based on the model's performance. Fine-tuning the prompts based on generated outputs and user feedback can help optimize the model's behavior.

Human-in-the-loop Evaluation: Human evaluation and feedback play a crucial role in prompt engineering. Collecting feedback on the quality of model-generated outputs and iteratively refining prompts based on this feedback can improve the overall performance and relevance of the model.

Auto-GPT prompt engineering is an essential aspect of working with language models like GPT. By carefully designing prompts and instructions, we can guide the model's output, improve relevance, coherence, and accuracy, and achieve desired results in various NLP tasks.


## Lessons learned from model development

There are scripts that are developed that will need to be debugged manually so that the models execution can continue. 

Ideally when these errors occur the developer is notified quickly. 

These models should be able to run without being constantly supervised. All logs should be saved so that decisions made by the model can be audited if required.

- Ensure that the model has been prompted with the requirement for robust software repositories (unit tested, behavioural tests).

## Auto-GPT Plugins

https://autoplugins.vercel.app/ - Community Maintained AutoGPT Plugins.

> For interactionless use, set `ALLOWLISTED_PLUGINS=example-plugin1,example-plugin2,example-plugin3` in your `.env`

There are two categories of plugins: **first party** and **third party**. First-party plugins are included in this repo and are installed by default when the plugin platform is installed. Third-party plugins need to be added individually. Use first-party plugins for widely-used plugins, and third-party for your specific needs. **You can view all the plugins and their contributors on this [directory](https://autoplugins.vercel.app/).**

If you've built a plugin and it's not listed in the directory, you can make a PR to this [repo](https://github.com/dylanintech/autoplugins) by adding your plugin to the `data` array in `plugins.tsx`.

You can also see the plugins here:

| Plugin       | Description     | Location |
|--------------|-----------|--------|
| Astro Info   | This gives Auto-GPT info about astronauts.                                                           | [autogpt_plugins/astro](https://github.com/Significant-Gravitas/Auto-GPT-Plugins/tree/master/src/autogpt_plugins/astro)           |
| API Tools        | This allows Auto-GPT to make API calls of various kinds.                                                           | [autogpt_plugins/api_tools](https://github.com/Significant-Gravitas/Auto-GPT-Plugins/tree/master/src/autogpt_plugins/api_tools)           |
| Baidu Search |  This search plugin integrates Baidu search engines into Auto-GPT. | [autogpt_plugins/baidu_search](https://github.com/Significant-Gravitas/Auto-GPT-Plugins/tree/master/src/autogpt_plugins/baidu_search)|
| Bing Search      | This search plugin integrates Bing search engines into Auto-GPT.                                                  | [autogpt_plugins/bing_search](https://github.com/Significant-Gravitas/Auto-GPT-Plugins/tree/master/src/autogpt_plugins/bing_search)       |
| Bluesky | Enables Auto-GPT to retrieve posts from Bluesky and create new posts. | [autogpt_plugins/bluesky](https://github.com/Significant-Gravitas/Auto-GPT-Plugins/tree/master/src/autogpt_plugins/bluesky)|
| Email            | Revolutionize email management with the Auto-GPT Email Plugin, leveraging AI to automate drafting and intelligent replies. | [autogpt_plugins/email](https://github.com/Significant-Gravitas/Auto-GPT-Plugins/tree/master/src/autogpt_plugins/email)                 |
| News Search      | This search plugin integrates News Articles searches, using the NewsAPI aggregator into Auto-GPT.                 | [autogpt_plugins/news_search](https://github.com/Significant-Gravitas/Auto-GPT-Plugins/tree/master/src/autogpt_plugins/news_search)   |
| Planner          | Simple Task Planner Module for Auto-GPT  | [autogpt_plugins/planner](https://github.com/Significant-Gravitas/Auto-GPT-Plugins/blob/master/src/autogpt_plugins/planner/) |
| Random Values    | Enable Auto-GPT to generate various random numbers and strings.                                                    | [autogpt_plugins/random_values](https://github.com/Significant-Gravitas/Auto-GPT-Plugins/tree/master/src/autogpt_plugins/random_values) |
| SceneX           | Explore image storytelling beyond pixels with the Auto-GPT SceneX Plugin.                                        | [autogpt_plugins/scenex](https://github.com/Significant-Gravitas/Auto-GPT-Plugins/tree/master/src/autogpt_plugins/scenex)               |
| Telegram |  A smoothly working Telegram bot that gives you all the messages you would normally get through the Terminal. | [autogpt_plugins/telegram](https://github.com/Significant-Gravitas/Auto-GPT-Plugins/tree/master/src/autogpt_plugins/telegram) |
| Twitter          | Auto-GPT is capable of retrieving Twitter posts and other related content by accessing the Twitter platform via the v1.1 API using Tweepy.               | [autogpt_plugins/twitter](https://github.com/Significant-Gravitas/Auto-GPT-Plugins/tree/master/src/autogpt_plugins/twitter)           |
| Wikipedia Search | This allows Auto-GPT to use Wikipedia directly.                                                                    | [autogpt_plugins/wikipedia_search](https://github.com/Significant-Gravitas/Auto-GPT-Plugins/tree/master/src/autogpt_plugins/wikipedia_search) |
| WolframAlpha Search | This allows AutoGPT to use WolframAlpha directly.                                                                                         | [autogpt_plugins/wolframalpha_search](https://github.com/Significant-Gravitas/Auto-GPT-Plugins/tree/master/src/autogpt_plugins/wolframalpha_search)|

Some third-party plugins have been created by contributors that are not included in this repository. For more information about these plugins, please visit their respective GitHub pages.

| Plugin       | Description     | Repository |
|--------------|-----------------|-------------|
| Alpaca-Trading | Trade stocks and crypto, paper or live with Auto-GPT | [danikhan632/Auto-GPT-AlpacaTrader-Plugin](https://github.com/danikhan632/Auto-GPT-AlpacaTrader-Plugin)|
| AutoGPT User Input Request | Allow Auto-GPT to specifically request user input in continous mode | [HFrovinJensen/Auto-GPT-User-Input-Plugin](https://github.com/HFrovinJensen/Auto-GPT-User-Input-Plugin)|
| BingAI | Enable Auto-GPT to fetch information via BingAI, saving time, API requests while maintaining accuracy. This does not remove the need for OpenAI API keys | [gravelBridge/AutoGPT-BingAI](https://github.com/gravelBridge/AutoGPT-BingAI)|
| Crypto | Trade crypto with Auto-GPT | [isaiahbjork/Auto-GPT-Crypto-Plugin](https://github.com/isaiahbjork/Auto-GPT-Crypto-Plugin)|
| Discord | Interact with your Auto-GPT instance through Discord | [gravelBridge/AutoGPT-Discord](https://github.com/gravelBridge/AutoGPT-Discord)|
| Dolly AutoGPT Cloner | A way to compose & run multiple Auto-GPT processes that cooperate, till core has multi-agent support | [pr-0f3t/Auto-GPT-Dolly-Plugin](https://github.com/pr-0f3t/Auto-GPT-Dolly-Plugin)|
| Google Analytics | Connect your Google Analytics Account to Auto-GPT. | [isaiahbjork/Auto-GPT-Google-Analytics-Plugin](https://github.com/isaiahbjork/Auto-GPT-Google-Analytics-Plugin)|
| IFTTT webhooks | This plugin allows you to easily integrate IFTTT connectivity using Maker | [AntonioCiolino/AutoGPT-IFTTT](https://github.com/AntonioCiolino/AutoGPT-IFTTT)|
| iMessage | Send and Get iMessages using Auto-GPT | [danikhan632/Auto-GPT-Messages-Plugin](https://github.com/danikhan632/Auto-GPT-Messages-Plugin)|
| Instagram | Instagram access | [jpetzke/AutoGPT-Instagram](https://github.com/jpetzke/AutoGPT-Instagram)|
| Mastodon  | Simple Mastodon plugin to send toots through a Mastodon account | [ppetermann/AutoGPTMastodonPlugin](https://github.com/ppetermann/AutoGPTMastodonPlugin)|
| MetaTrader | Connect your MetaTrader Account to Auto-GPT. | [isaiahbjork/Auto-GPT-MetaTrader-Plugin](https://github.com/isaiahbjork/Auto-GPT-MetaTrader-Plugin) |
| Notion      | Notion plugin for Auto-GPT.  | [doutv/Auto-GPT-Notion](https://github.com/doutv/Auto-GPT-Notion) |
| Slack | This plugin allows to receive commands and send messages to slack channels | [adithya77/Auto-GPT-slack-plugin](https://github.com/adithya77/Auto-GPT-slack-plugin)
| Spoonacular | Find recipe insiprations using Auto-GPT | [minfenglu/Auto-GPT-Spoonacular-Plugin](https://github.com/minfenglu/Auto-GPT-Spoonacular-Plugin)
| System Information      | This plugin adds an extra line to the prompt, serving as a hint for the AI to use shell commands likely supported by the current system. By incorporating this plugin, you can ensure that the AI model provides more accurate and system-specific shell commands, improving its overall performance and usefulness. | [hdkiller/Auto-GPT-SystemInfo](https://github.com/hdkiller/Auto-GPT-SystemInfo) |
| TiDB Serverless   | Connect your TiDB Serverless database to Auto-GPT, enable get query results from database | [pingcap/Auto-GPT-TiDB-Serverless-Plugin](https://github.com/pingcap/Auto-GPT-TiDB-Serverless-Plugin)
| Todoist-Plugin | Allow Auto-GPT to programatically interact with yor Todoist to create, update, and manage your Todoist | [danikhan632/Auto-GPT-Todoist-Plugin](https://github.com/danikhan632/Auto-GPT-Todoist-Plugin) |
| Weather | A simple weather plugin wrapping around python-weather | [ppetermann/Auto-GPT-WeatherPlugin](https://github.com/ppetermann/Auto-GPT-WeatherPlugin) |
| Web-Interaction | Enable Auto-GPT to fully interact with websites! Allows Auto-GPT to click elements, input text, and scroll | [gravelBridge/AutoGPT-Web-Interaction](https://github.com/gravelBridge/AutoGPT-Web-Interaction)|
| WolframAlpha | Access to WolframAlpha to do math and get accurate information | [gravelBridge/AutoGPT-WolframAlpha](https://github.com/gravelBridge/AutoGPT-WolframAlpha)|
| YouTube   | Various YouTube features including downloading and understanding | [jpetzke/AutoGPT-YouTube](https://github.com/jpetzke/AutoGPT-YouTube) |
| Zapier webhooks | This plugin allows you to easily integrate Zapier connectivity | [AntonioCiolino/AutoGPT-Zapier](https://github.com/AntonioCiolino/AutoGPT-Zapier)|
| Project Management | Streamline your Project Management with ease: Jira, Trello, and Google Calendar Made Effortless| [minfenglu/AutoGPT-PM-Plugin](https://github.com/minfenglu/AutoGPT-PM-Plugin)|

https://github.com/Significant-Gravitas/Auto-GPT-Plugins
