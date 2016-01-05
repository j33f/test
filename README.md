# test version + tag version

## usage

```bash
npm version minor -m 'tag version %s'
```

In ```package.json```

```js
{
	...
	"scripts": {
		...
	    "preversion": "npm test", // do whatever before to change the version
	    "version": "echo \"grunt build or other thing to do\"", // do whatever when the version has just changed, like build something
	    "postversion": "git push && git push --tags" // git push and tag the version
    }
...
}
```