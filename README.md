![tabu](http://github.com/posixpascal/tabu/blob/master/p.png)
===

A noscript tab library written with only CSS.
On top of it, it offers a nice JavaScript API for non-noscript users.
The JavaScript API isn't finished yet.

### Maintainer

[Pascal Raszyk](https://github.com/posixpascal)

### Get Started

Install dependencies

`sudo npm install && bower install`

Build Project

`grunt`

Run Tests

Open `SpecRunner.html` in your browser and test with jasmine

### How to use


```html
	<!-- It's important to add a .noscript class to your body in order to use this script -->
	<body class="noscript">
	

		<div data-tabu="section_1">
			<a href="#tab1">
				<label for="tab1">
					Tab 1
				</label>
			<a href="#tab2">
				<label for="tab2">
					Tab 2
				</label>
			</a>
			<a href="#tab3">
				<label for="tab3">
					Tab 3
				</label>
			</a>
		</div>

		<div data-tabu-content="section_1">
			<input type="radio" checked name="section_1" id="tab1" data-tabu-tab="tab1">
			<a name="tab1">
				This is the content for the first tab.
				Also this tab is active by default.
			</a>
		</div>

		<div data-tabu-content="section_1">
			<input type="radio" name="section_1" id="tab2" data-tabu-tab="tab2">
			<a name="tab2">
				This is the content for the second tab.
			</a>
		</div>

		<div data-tabu-content="section_1">
			<input type="radio" name="section_1" id="tab3" data-tabu-tab="tab3">
			<a name="tab3">
				And this is the last tab.
			</a>
		</div>


	</body>
```

### How it works

The tab navigation is build with labels which trigger radio inputs in the content area.
I'm using the CSS sibling selector `+` to match the next `<a>` block and set it's display attribute to block.
The label tags are wrapped with an additional `<a>` tag to change the URL after selecting the tab.

Unfortunately it's not possible to select the current active link using CSS . :(. So it's not possible for users to save the tab state in the URL.

### License

The MIT License (MIT)

Copyright (c) 2015 Pascal Raszyk

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
