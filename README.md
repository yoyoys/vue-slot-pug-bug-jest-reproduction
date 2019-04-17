# reproduction a bug for named slot in jest+pug

If you use pug for template, 
and use jest to test a component which used any name slot,
you will receive this message below:

```
> vue-cli-service test:unit

 FAIL  tests/unit/example.spec.ts
  ● Test suite failed to run

    SyntaxError: Unexpected character '#' (1:150)

      at Parser.pp$4.raise (node_modules/vue-template-es2015-compiler/buble.js:2757:13)
      at Parser.pp$8.getTokenFromCode (node_modules/vue-template-es2015-compiler/buble.js:4906:8)
      at Parser.pp$8.readToken (node_modules/vue-template-es2015-compiler/buble.js:4628:15)
      at Parser.readToken (node_modules/vue-template-es2015-compiler/buble.js:6029:22)
      at Parser.pp$8.nextToken (node_modules/vue-template-es2015-compiler/buble.js:4619:15)
      at Parser.pp$8.next (node_modules/vue-template-es2015-compiler/buble.js:4576:8)
      at Parser.pp.eat (node_modules/vue-template-es2015-compiler/buble.js:577:10)
      at Parser.pp.expect (node_modules/vue-template-es2015-compiler/buble.js:641:8)
      at Parser.pp$1.parseFunctionParams (node_modules/vue-template-es2015-compiler/buble.js:1230:8)
      at Parser.pp$1.parseFunction (node_modules/vue-template-es2015-compiler/buble.js:1218:8)

Test Suites: 1 failed, 1 total
```