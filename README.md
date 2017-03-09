# v8-profiler-trigger-electron

> Trigger CPU profile recording or heap snapshots for node apps using keyboard
shortcuts.

[![NPM Badge](https://nodei.co/npm/v8-profiler-trigger-electron.png?downloads=true)](https://www.npmjs.com/package/v8-profiler-trigger-electron)

**Taking a heap snapshot**

![Demo](docs/demo.gif)

1. Start v8-profiler-trigger-electron once in your app

  ```js
  const v8ProfilerTrigger = require('v8-profiler-trigger-electron');
  v8ProfilerTrigger();
  ```

2. Press `h` followed by enter
3. Thats it, you can now load the saved *.heapsnapshot* to Chrome debugger

  In debugger, open `Profiles` tab. Click Load and
  open the <timestamp>.heapsnapshot.


## Install

```bash
npm install v8-profiler-trigger-electron --save-dev
```

## API

### v8ProfilerTrigger([opts])

Starts the V8 profiler trigger listeners.


#### `opts`

```js
{
  // Trigger snapshots or recording via stdin events.
  // The only method supported currently is 'stdin'.
  listenMethod: 'stdin',

  // Changes default CPU profiler sampling interval to the specified
  // number of microseconds. Default interval is 1000us.
  samplingInterval: 1000
}
```

## Usage

Examples how to use the v8-profiler.

### CPU Profiling

You can use Chrome debugger to interactively inspect results:

![Flamegraph](docs/flame.gif)


## License

MIT
