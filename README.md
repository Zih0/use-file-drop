# use-file-drop

A simple hook for drag and drop file in react.

[![NPM](https://img.shields.io/npm/v/@zih0/use-file-drop.svg)](https://www.npmjs.com/package/@zih0/use-file-drop) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## Installation

```sh
$ yarn add @zih0/use-file-drop
```

or, with npm:

```sh
npm install @zih0/use-file-drop
```

## Usage

```jsx
import React, { useEffect } from 'react';
import useFileDrop from '@zih0/use-file-drop';

const App () => {
  const { inputRef, labelRef, files, isDragActive } = useFileDrop();

  return (
    <div>
      <input ref={inputRef} id="upload" />
      <label ref={labelRef} htmlFor="upload">
        {isDragActive ? <span>Drop the file!</span> : <span>Drag and drop the file.</span>}
      </label>
    </div>
  )
};
```

## Options

You can set input file attributes by `options`:

```jsx
const { inputRef, files } = useFileDrop({ multiple: true, accept: 'image/*' });
```

## License

MIT © [Zih0](https://github.com/zih0/)
