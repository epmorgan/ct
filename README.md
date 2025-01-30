## Tasks

We use [mise](https://mise.jdx.dev/) to manage the JVM dependency and tasks we can perform on the project.

### `mise repl`

Starts an interactive REPL with history, highlighting, completion and automatic documentation lookup as you type. Before you start working with the project you should run this in a terminal that you can keep safe in the background somewhere.

You can type code directly into this REPL but I’d recommend using a plugin for an editor of your choosing. It should connect to the REPL automatically when you open a Clojure file in this project thanks to the `.nrepl-port` file.

You may also enable a [portal](https://github.com/djblue/portal) window like so:

```bash
mise repl :portal true
```

This will open a window alongside your REPL (or in your current browser window if you don’t have a Chrome / Chromium installed) that will allow you to visually inspect any values you wrap in `(tap> ...)`. Try it out by evaluating `(tap> (range 10))` in the REPL with the portal window open.

This development REPL also enables the [mount](https://github.com/tolitius/mount) system management and [malli](https://github.com/metosin/malli) function instrumentation.

### `mise test`

Run the test suite with [kaocha](https://github.com/lambdaisland/kaocha). Append `--watch` to execute your tests as you change files.

### `mise format`

Format all of your code with [cljfmt](https://github.com/weavejester/cljfmt).

### `mise antq`

Find and update dependencies with [antq](https://github.com/liquidz/antq).

```bash
# Check for updates
mise antq

# Actually perform updates
mise antq --upgrade
```
