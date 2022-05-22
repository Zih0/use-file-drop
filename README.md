# use-file-drop

A simple hook for drag and drop file in react.

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
  const { inputRef, labelRef, files, isDragActive } = useInputFile();

  return (
    <div>
      <input ref={inputRef} />
      <label ref={labelRef}>
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
