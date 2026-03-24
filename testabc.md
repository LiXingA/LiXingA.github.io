<!--{"pinCode":true,"dname":"b300b81e-8603-457f-b651-8075fbd2c8bb","codeMode":"markdown"}-->
```md
123
```

<!--{"pinCode":false,"dname":"30a7d08f-150c-4c3a-8d99-a68da0ae52d6","codeMode":"markdown"}-->
```md
<p align="center">
  <a href="https://editorjs.io/">
    <picture>
      <source media="(prefers-color-scheme: dark)"  srcset="./assets/logo_night.png">
      <source media="(prefers-color-scheme: light)" srcset="./assets/logo_day.png">
      <img alt="Editor.js Logo" src="./assets/logo_day.png">
    </picture>    
  </a>
</p>

<p align="center">
 <a href="https://editorjs.io/">editorjs.io</a> |
  <a href="https://editorjs.io/base-concepts/">documentation</a> |
  <a href="https://github.com/codex-team/editor.js/blob/next/docs/CHANGELOG.md">changelog</a>

</p>

<p align="center">
  <a href="https://www.npmjs.com/package/@editorjs/editorjs">
    <img src="https://flat.badgen.net/npm/v/@editorjs/editorjs?icon=npm" alt="npm"/>
  </a>
  <a href="https://www.npmjs.com/package/@editorjs/editorjs">
    <img src="https://flat.badgen.net/bundlephobia/minzip/@editorjs/editorjs?color=green" alt="Minzipped size"/>
  </a>
  <a href="https://github.com/codex-team/editor.js#backers">
    <img src="https://opencollective.com/editorjs/backers/badge.svg" alt="Backers on Open Collective"/>
  </a>
  <a href="https://github.com/codex-team/editor.js#sponsors">
    <img src="https://opencollective.com/editorjs/sponsors/badge.svg" alt="Sponsors on Open Collective"/>
  </a>
</p>
```

<!--{"pinCode":false,"dname":"48c98cbf-922c-4989-af2c-188683d2c2d5","codeMode":"markdown"}-->
```md
## About
```

<!--{"pinCode":false,"dname":"781aabda-5c74-4873-8667-8eb4ffa5775d","codeMode":"markdown"}-->
```md
Editor.js is an open-source text editor offering a variety of features to help users create and format content efficiently. It has a modern, block-style interface that allows users to easily add and arrange different types of content, such as text, images, lists, quotes, etc. Each Block is provided via a separate plugin making Editor.js extremely flexible.
```

<!--{"pinCode":false,"dname":"83c5628b-12c4-4f20-add9-a1f90e2f3bc9","codeMode":"markdown"}-->
```md
Editor.js outputs a clean JSON data instead of heavy HTML markup. Use it in Web, iOS, Android, AMP, Instant Articles, speech readers, AI chatbots — everywhere. Easy to sanitize, extend and integrate with your logic.
```

<!--{"pinCode":false,"dname":"a02fd9e2-350d-4fef-bc67-3b2854a4bb56","codeMode":"markdown"}-->
```md
* 😍  Modern UI out of the box
* 💎  Clean JSON output
* ⚙️  Well-designed API
* 🛍  Various Tools available
* 💌  Free and open source
```

<!--{"pinCode":false,"dname":"f6c6b87b-d61a-48a5-b547-67dd4f26fa96","codeMode":"markdown"}-->
```md
<picture>
  <img alt="Editor.js Overview" src="./assets/overview.png">
</picture>
```

<!--{"pinCode":false,"dname":"a9561043-092b-4307-a84d-4b85ef6c1caf","codeMode":"markdown"}-->
```md
## Installation
```

<!--{"pinCode":false,"dname":"ca687b6a-9c23-4ed2-bcaf-aa3009dde718","codeMode":"markdown"}-->
```md
It's quite simple:
```

<!--{"pinCode":false,"dname":"ecaa96cb-80a9-4467-9376-2a8aa20c414f","codeMode":"markdown"}-->
```md
1. Install Editor.js
2. Install tools you need
3. Initialize Editor's instance
```

<!--{"pinCode":false,"dname":"37c16d0e-7a02-40a3-8fc8-704fa57f8829","codeMode":"markdown"}-->
```md
Install using NPM, Yarn, or [CDN](https://www.jsdelivr.com/package/npm/@editorjs/editorjs):
```

```
npm i @editorjs/editorjs
```

<!--{"pinCode":false,"dname":"94b30f01-30c2-4924-a3e0-073cfe1d662c","codeMode":"markdown"}-->
```md
Choose and install tools:
```

<!--{"pinCode":false,"dname":"3a3ba5da-41fa-45ea-ba42-6a2e6beb470f","codeMode":"markdown"}-->
```md
* [Heading](https://github.com/editor-js/header)
* [Quote](https://github.com/editor-js/quote)
* [Image](https://github.com/editor-js/image)
* [Simple Image](https://github.com/editor-js/simple-image) (without backend requirement)
* [Nested List](https://github.com/editor-js/nested-list)
* [Checklist](https://github.com/editor-js/checklist)
* [Link embed](https://github.com/editor-js/link)
* [Embeds](https://github.com/editor-js/embed) (YouTube, Twitch, Vimeo, Gfycat, Instagram, Twitter, etc)
* [Table](https://github.com/editor-js/table)
* [Delimiter](https://github.com/editor-js/delimiter)
* [Warning](https://github.com/editor-js/warning)
* [Code](https://github.com/editor-js/code)
* [Raw HTML](https://github.com/editor-js/raw)
* [Attaches](https://github.com/editor-js/attaches)
* [Marker](https://github.com/editor-js/marker)
* [Inline Code](https://github.com/editor-js/inline-code)
```

<!--{"pinCode":false,"dname":"cdcceb65-09e4-463e-a52b-1ef446508964","codeMode":"markdown"}-->
```md
See the [😎 Awesome Editor.js](https://github.com/editor-js/awesome-editorjs) list for more tools.
```

<!--{"pinCode":false,"dname":"81738c69-6cca-419f-9f5c-da8ff3acf5fd","codeMode":"markdown"}-->
```md
Initialize the Editor:
```

<!--{"pinCode":false,"dname":"47102ae4-bf49-44f8-b2c9-fa07852292cf","codeMode":"htmlmixed"}-->
```html
<div id="editorjs"></div>
```

<!--{"pinCode":true,"dname":"a6ce8fc2-69bc-4c84-95f0-357dd484ad07","codeMode":"javascript"}-->
```javascript
import EditorJS from '@editorjs/editorjs'

const editor = new EditorJS({
  tools: {
   // ... your tools
  }
})
```

<!--{"pinCode":false,"dname":"7178cf28-126e-4682-85c1-8c2bb1dfefb9","codeMode":"markdown"}-->
```md
See details about [Installation](https://editorjs.io/getting-started/) and [Configuration](https://editorjs.io/configuration/) at the documentation.
```

<!--{"pinCode":false,"dname":"ffd4d8c1-a01d-412b-ae08-b83057196df8","codeMode":"markdown"}-->
```md
### Saving Data
```

<!--{"pinCode":false,"dname":"6b4749f4-1bad-4bd7-ad34-04cc80ea0faf","codeMode":"markdown"}-->
```md
Call `editor.save()` and handle returned Promise with saved data.
```

<!--{"pinCode":true,"dname":"ab5a9875-bd0d-46c0-ad3b-16182ccd649f","codeMode":"javascript"}-->
```javascript
const data = await editor.save()
```

<!--{"pinCode":false,"dname":"f4b8f4d1-301c-4811-9545-237612d2148f","codeMode":"markdown"}-->
```md
### Example
```

<!--{"pinCode":false,"dname":"02019584-2e0e-4c4e-8399-0580aeb2e4fe","codeMode":"markdown"}-->
```md
Take a look at the [example.html](example/example.html) to view more detailed examples.
```

<!--{"pinCode":false,"dname":"0b3b05b3-f8b2-431d-8009-b2848fea910c","codeMode":"markdown"}-->
```md
## Roadmap
```

<!--{"pinCode":false,"dname":"2fa43bb0-b7f1-47b6-a027-24f17217b44d","codeMode":"markdown"}-->
```md
<img align="right" width="342" src="./assets/roadmap.png" style="margin-left: 30px">
```

<!--{"pinCode":false,"dname":"91e2a748-9768-4664-ae38-04062d3c12ee","codeMode":"markdown"}-->
```md
* Unified Toolbars
  * \[x] Block Tunes moved left
  * \[x] Toolbox becomes vertical
  * \[x] Ability to display several Toolbox buttons by the single Tool
  * \[x] Block Tunes become vertical
  * \[x] Block Tunes support nested menus
  * \[x] Block Tunes support separators
  * \[x] Conversion Menu added to the Block Tunes
  * \[x] Unified Toolbar supports hints
  * \[x] Conversion Toolbar uses Unified Toolbar
  * \[x] Inline Toolbar uses Unified Toolbar
* Collaborative editing
  * \[ ] Implement Inline Tools JSON format
  * \[ ] Operations Observer, Executor, Manager, Transformer
  * \[ ] Implement Undo/Redo Manager
  * \[ ] Implement Tools API changes
  * \[ ] Implement Server and communication
  * \[ ] Update basic tools to fit the new API
* Other features
  * \[ ] Blocks drag'n'drop
  * \[ ] New cross-block selection
  * \[ ] New cross-block caret moving
* Ecosystem improvements
  * \[x] CodeX Icons — the way to unify all tools and core icons
  * \[x] New Homepage and Docs
  * \[x] @editorjs/create-tool for Tools bootstrapping
  * \[ ] Editor.js DevTools — stand for core and tools development
  * \[ ] Editor.js Design System
  * \[ ] Editor.js Preset Env
  * \[ ] Editor.js ToolKit
  * \[ ] New core bundle system
  * \[ ] New documentation and guides
```

<!--{"pinCode":false,"dname":"449308ce-1334-4bdb-a7cc-a33ba4182d06","codeMode":"markdown"}-->
```md
<a href="https://opencollective.com/editorjs/donate" target="_blank">
  <picture>
    <source width="162px" media="(prefers-color-scheme: dark)"  srcset="./assets/support_night.png">
    <source width="162px" media="(prefers-color-scheme: light)" srcset="./assets/support_day.png">
    <img width="162px" alt="Support Editor.js" src="./assets/support_day.png">
  </picture>
</a>

<br>
```

<!--{"pinCode":false,"dname":"eccb2c65-e840-42f6-a175-3717b511bcdf","codeMode":"markdown"}-->
```md
## Like Editor.js?
```

<!--{"pinCode":false,"dname":"c39eee26-d739-445f-81d4-f19e1a566c85","codeMode":"markdown"}-->
```md
You can support project improvement and development of new features with a donation to our team.
```

<!--{"pinCode":false,"dname":"35437f15-b5b7-489b-b458-8cf6c90c8c5b","codeMode":"markdown"}-->
```md
[Donate via OpenCollective](https://opencollective.com/editorjs)
\
[Donate via Crypto](https://codex.so/donate)
\
[Donate via Patreon](https://www.patreon.com/editorjs)
```

<!--{"pinCode":false,"dname":"2fa549ab-f293-49a2-ae42-199af789d166","codeMode":"markdown"}-->
```md
### Why donate
```

<!--{"pinCode":false,"dname":"770b2c41-016c-4ed4-bd08-e0760bde6ea3","codeMode":"markdown"}-->
```md
Donations to open-source products have several advantages for your business:
```

<!--{"pinCode":false,"dname":"e292efd1-94a1-43f6-8bef-de1a6e91bf97","codeMode":"markdown"}-->
```md
* If your business relies on Editor.js, you'll probably want it to be maintained
* It helps Editor.js to evolve and get the new features
* We can support contributors and the community around the project. You'll receive well organized docs, guides, etc.
* We need to pay for our infrastructure and maintain public resources (domain names, homepages, docs, etc). Supporting it guarantees you to access any resources at the time you need them.
* You can advertise by adding your brand assets and mentions on our public resources
```

<!--{"pinCode":false,"dname":"5abd4228-009d-4cac-a10a-e8ce20e26451","codeMode":"markdown"}-->
```md
### Sponsors
```

<!--{"pinCode":false,"dname":"a0732382-0596-4209-a05c-6ca4c37763c1","codeMode":"markdown"}-->
```md
Support us by becoming a sponsor. Your logo will show up here with a link to your website.
```

<!--{"pinCode":false,"dname":"765206f3-b8d6-4723-b828-35ddc3e8bc44","codeMode":"markdown"}-->
```md
<p>
  <a href="https://www.mister-auto.com/" target="_blank">
    <img src="https://opencollective-production.s3.us-west-1.amazonaws.com/5131a030-5672-11ec-be79-1d003d12ec5f.png" width="50" alt="Mister Auto">
  </a>
  <a href="https://www.uplucid.com/" target="_blank">
    <img src="https://logo.clearbit.com/uplucid.com" width="50" alt="UPLUCID, K.K.">
  </a>
  <a href="https://www.contentharmony.com/" target="_blank">
    <img src="https://opencollective-production.s3.us-west-1.amazonaws.com/89edb1b0-7d82-11ed-b99e-ab6e6f9cb69f.png" width="50" alt="Kane Jamison">
  </a>
  <a href="https://www.contentharmony.com/product/" target="_blank">
    <img src="https://logo.clearbit.com/contentharmony.com" width="50" alt="Content Harmony">
  </a>
</p>
```

<!--{"pinCode":false,"dname":"a1bb799e-a1c4-496f-9253-dd1da0b376e2","codeMode":"markdown"}-->
```md
[Become a Sponsor](https://opencollective.com/editorjs/contribute/sir-8679/checkout)
```

<!--{"pinCode":false,"dname":"57fc15b0-cbfb-44a0-9ca9-af5d9c3fd4aa","codeMode":"markdown"}-->
```md
### Backers
```

<!--{"pinCode":false,"dname":"072f95c6-158c-46b7-a046-7a03118b9806","codeMode":"markdown"}-->
```md
Thank you to all our backers
```

<!--{"pinCode":false,"dname":"a1503501-9456-4aaa-b60b-19070a159ad5","codeMode":"markdown"}-->
```md
<a href="https://opencollective.com/editorjs#backers" target="_blank"><img src="https://opencollective.com/editorjs/backers.svg?width=890&avatarHeight=34"></a>
```

<!--{"pinCode":false,"dname":"fc027f1a-aa5b-4ec6-8697-0c21f1b0f7d0","codeMode":"markdown"}-->
```md
[Become a Backer](https://opencollective.com/editorjs/contribute/backer-8632/checkout)
```

<!--{"pinCode":false,"dname":"4c9c9685-20f3-4a0a-ab42-a74ea5a7cd44","codeMode":"markdown"}-->
```md
### Contributors
```

<!--{"pinCode":false,"dname":"faf284de-f016-4225-a606-da99f5363dcf","codeMode":"markdown"}-->
```md
This project exists thanks to all the people who contribute.
```

<!--{"pinCode":false,"dname":"08bafa8b-507f-4f70-b6a6-c6b3708a4f88","codeMode":"markdown"}-->
```md
<p><img src="https://opencollective.com/editorjs/contributors.svg?width=890&button=false&avatarHeight=34" /></p>
```

<!--{"pinCode":false,"dname":"c82e9640-754b-454c-9772-10d6c7d1cdfc","codeMode":"markdown"}-->
```md
### Need something special?
```

<!--{"pinCode":false,"dname":"f5944b8d-7051-43a7-860d-4726053fd241","codeMode":"markdown"}-->
```md
Hire CodeX experts to resolve technical challenges and match your product requirements.
```

<!--{"pinCode":false,"dname":"ab344c51-589c-45ab-a35c-1dac8f6ccb72","codeMode":"markdown"}-->
```md
* Resolve a problem that has high value for you
* Implement a new feature required by your business
* Help with integration or tool development
* Provide any consultation
```

<!--{"pinCode":false,"dname":"5349cfe2-b983-4ba7-9159-a30d99c5ad58","codeMode":"markdown"}-->
```md
Contact us via team@codex.so and share your details
```

<!--{"pinCode":false,"dname":"780145d9-4b16-4cbc-a614-2f0a510301b0","codeMode":"markdown"}-->
```md
## Community
```

<!--{"pinCode":false,"dname":"c6971273-a2cf-4979-b184-0cb8fd57427d","codeMode":"markdown"}-->
```md
* [Official Tools](https://github.com/editor-js)
* [Awesome Editor.js](https://github.com/editor-js/awesome-editorjs)
* [Good First Tasks](https://github.com/codex-team/editor.js/issues?q=is%3Aopen+is%3Aissue+label%3A%22good+first+task%22)
* [Contributing](https://editorjs.io/contributing/)
* [Telegram Chat](https://t.me/codex_editor)
```

<!--{"pinCode":false,"dname":"b189b834-1c3c-42e8-9336-8ea146c18ef3","codeMode":"markdown"}-->
```md
# About CodeX
```

<!--{"pinCode":false,"dname":"ca2f2962-6f4e-41d8-9e37-ad8cfca3463c","codeMode":"markdown"}-->
```md
<img align="right" width="120" height="120" src="https://codex.so/public/app/img/codex-logo.svg" hspace="50">
```

<!--{"pinCode":false,"dname":"f7f4537a-54e6-4ddc-bb78-f6eda058ab88","codeMode":"markdown"}-->
```md
CodeX is a team of digital specialists around the world interested in building high-quality open source products on a global market. We are [open](https://codex.so/join) for young people who want to constantly improve their skills and grow professionally with experiments in cutting-edge technologies.
```

<!--{"pinCode":false,"dname":"275e3c5d-4171-411d-b812-229edc9e4e3b","codeMode":"markdown"}-->
```md
| 🌐 | Join  👋  | Twitter | Instagram |
| -- | -- | -- | -- |
| [codex.so](https://codex.so) | [codex.so/join](https://codex.so/join) |[@codex\_team](http://twitter.com/codex_team) | [@codex\_team](http://instagram.com/codex_team/) |
```
