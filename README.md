## This Project is the prototype implementation of Uploading any file on IPFS(particularly IOT Firmwares) network and calculating IPFS Hashes (starting with Qm), 

> Completed under IIITA Internship, frontend of the project is under development...

> Just enough code to calculate the IPFS hash for some data

Calculate the IPFS hash for some data without having to install or run an IPFS node. Try it out with npx:

```
npx pure-ipfs-only-hash <path to file>
```

## Install

```sh
npm i --only=production pure-ipfs-only-hash
```

## Usage

From the command line

```sh
pure-ipfs-only-hash <file>

# or pipe in 
echo "hello world" | pure-ipfs-only-hash
```

As a library

```js
const Hash = require('pure-ipfs-only-hash')
const data = 'hello world!'
const hash = await Hash.of(data)
console.log(hash) // QmTp2hEo8eXRp6wg7jXv1BLCMh5a4F3B7buAUZNZUu772j
```

## API

```js
const Hash = require('pure-ipfs-only-hash')
```

### `Hash.of(input, options?): Promise<string>`

Calculate the hash for the provided input.

* `input` (`string|Uint8Array|AsyncIterable<Uint8Array>`): The input bytes to calculate the IPFS hash for. Note that Node.js readable streams are async iterable!
* `options` (`Object`): Optional options passed directly to the `pure-ipfs-unixfs-importer` module. See the [API docs](https://github.com/ipfs/js-ipfs-unixfs-importer#api) for possible values.


## License

[MIT](LICENSE)
