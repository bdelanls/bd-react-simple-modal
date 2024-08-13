# bd-react-simple-modal

`bd-react-simple-modal` is a simple and customizable modal component for React, designed to be lightweight and easy to integrate into any project. Includes essential features like backdrop opacity, adjustable size, and accessibility support.

[![NPM](https://img.shields.io/npm/v/bd-react-simple-modal.svg)](https://www.npmjs.com/package/bd-react-simple-modal)

![HTML](https://img.shields.io/badge/-HTML-E34F26?style=flat&logo=html5&logoColor=white) ![CSS](https://img.shields.io/badge/-CSS-1572B6?style=flat&logo=css3&logoColor=white) ![React](https://img.shields.io/badge/-React-61DAFB?style=flat&logo=react&logoColor=black) ![TypeScript](https://img.shields.io/badge/-Typescript-3178C6?style=flat&logo=typescript&logoColor=white) ![npm](https://img.shields.io/badge/-npm-CB3837?style=flat&logo=npm&logoColor=white)

## Install

You can install the package via npm:

```bash
npm install bd-react-simple-modal
```

## Usage

Here is an example of how to use the Modal component:
```
import React, { useState } from 'react';
import { Modal } from 'bd-react-simple-modal';

const App = () => {
  const [isModalOpen, setIsModalOpen] = useState(false);

  const handleOpenModal = () => setIsModalOpen(true);
  const handleCloseModal = () => setIsModalOpen(false);

  return (
    <div>
      <button onClick={handleOpenModal}>Open Modal</button>
      <Modal
        isOpen={isModalOpen}
        onClose={handleCloseModal}
        title="Example Modal"
        size="medium"
        backdropOpacity={0.5}
      >
        <p>This is the content of the modal.</p>
      </Modal>
    </div>
  );
};

export default App;
```

## Props

* **isOpen (boolean)**: Controls whether the modal is visible or not.
* **onClose (() => void)**: Function to call when the modal should be closed.
* **title (string)**: Optional title to display at the top of the modal.
* **size ('small' | 'medium' | 'large')**: Size of the modal. Default is '**medium**'.
* **backdropOpacity (number)**: Opacity of the backdrop. Default is **0.5**.
* **children (React.ReactNode)**: The content to display inside the modal.
* **showCloseButton (boolean)**: Whether to show a close button. Default is **true**.
* **onBackdropClick (() => void)**: Function to call when the backdrop is clicked.
* **aria-labelledby (string)**: ID of the element that labels the modal.
* **aria-describedby (string)**: ID of the element that describes the modal.


## Built with TSDX

This project was bootstrapped with [TSDX](https://github.com/jaredpalmer/tsdx).

## License

MIT © [bdelanls](https://github.com/bdelanls)

