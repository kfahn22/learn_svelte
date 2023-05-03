# learn_svelte
Trying to figure out how to use Svelte

[Getting Started](https://svelte.dev/docs#getting-started)

From Quick Start

`npm create svelte@latest myapp`  
`cd myapp`  
`npm install`  
`npm run dev`  


npm create svelte@latest learn_svelte
cd learn_svelte
npm install
npm run dev


https://vitejs.dev/guide/api-javascript.html
npm init vite
select svelte
select javascript
Give a name: p5sketch
cd p5sketch
npm install
npm run dev


Svelte head
<svelte:head>
	<link rel="stylesheet" href="/tutorial/dark-theme.css">
</svelte:head>

custom tags
<svelte:options option={value}/>

<svelte:options tag="my-custom-element"/>

get
value: any = get(store)

register
require('svelte/register');

const App = require('./App.svelte').default;

...

const { html, css, head } = App.render({ answer: 42 });


Once a custom element has been defined, it can be used as a regular DOM element:
document.body.innerHTML = `
	<my-element>
		<p>This is some slotted content</p>
	</my-element>
`;

svelte.compile
result: {
	js,
	css,
	ast,
	warnings,
	vars,
	stats
} = svelte.compile(source: string, options?: {...})