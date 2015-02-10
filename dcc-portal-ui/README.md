ICGC DCC - Portal UI
===

Requiments
---

- Install [node.js](http://nodejs.org/download/ )
- Install ruby
- Install rubygems
- Install global modules:

	`npm install -g grunt-cli@0.1.13`

Setup
---

- Install local modules

	```
	cd src/main/js
	npm install
	```
	
- Install client-side dependencies	
	```
	cd src/main/js
	npm install -g bower
	bower install
	```
	
- Install ruby gems

	```
	cd src/main/js	
	sudo gem install bundler -v 1.5.3
	bundle install
	```

Run
---

- Start node development server: `grunt server`

- Open another console and start the proxy: `cake proxy`

- Start the [Portal API](../dcc-portal-api/README.md)
- View the site: [localhost:9001](http://localhost:9001/)

Style Guide
---

- Max line length: 120
- Spaces NOT Tabs
- 2 Spaces per indent
- Strings in 'single quotes'
- camelCase for variable names
- Use === instead of ==
- Fields generated by the UI should be prefixed with 'ui'
- No 1-line 'if' statements
- jQuery not $

Before Pull Request
---

Must pass JSHint: `grunt jshint`

Tips
---

If a production build fails to produce the expected output when deployed, try `rm -rf src/main/js/node_modules` and rebuilding.

