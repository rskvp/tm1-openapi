# Convert IBM TM1 OData to OpenAPI 3.1.0

This script converts an IBM Planing Analytics (aka IBM TM1) OData document ($Metadata) into OpenApi 3.0.1 JSON document.

It's a pure JavaScript implementation, depending only on [`odata-csdl`](https://github.com/oasis-tcs/odata-csdl-schemas/tree/master/lib), which in turn depends on [`sax js`](https://www.npmjs.com/package/sax).

## Installation

```sh
npm install
```

## Usage

Assuming you installed the script globally, and your TM1 metadata file is `TM1.xml`, then

```sh
node lib/cli.js ./tm1-meta/tm1.xml
```

will create `TM1.openapi3.json` next to it.

Just type

```sh
node lib/cli.js -h
```

to get usage hints

```
Usage: odata-openapi3 <options> <source files>
Options:
 --basePath              base path (default: /service-root)
 -d, --diagram           include YUML diagram
 -h, --help              show this info
 --host                  host (default: localhost)
 -o, --openapi-version   3.0.0 to 3.0.3 or 3.1.0 (default: 3.0.2)
 -p, --pretty            pretty-print JSON result
 --scheme                scheme (default: http)
 -t, --target            target file (default: source file basename + .openapi3.json)
 --skipBatchPath         skips the generation of the $batch path, (default: false)
 --title                 default title if none is annotated
 --description           default description if none is annotated
```
