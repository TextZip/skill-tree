# Arc Diagram

https://observablehq.com/d/8f264c3b1ce87374@277

View this notebook in your browser by running a web server in this folder. For
example:

~~~sh
npx http-server -c-1 -p 8010
~~~

Or, use the [Observable Runtime](https://github.com/observablehq/runtime) to
import this module directly into your application. To npm install:

~~~sh
npm install @observablehq/runtime@4
npm install https://api.observablehq.com/d/8f264c3b1ce87374@277.tgz?v=3
~~~

Then, import your notebook and the runtime as:

~~~js
import {Runtime, Inspector} from "@observablehq/runtime";
import define from "8f264c3b1ce87374";
~~~

To log the value of the cell named “foo”:

~~~js
const runtime = new Runtime();
const main = runtime.module(define);
main.value("foo").then(value => console.log(value));
~~~
