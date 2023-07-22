Modal Component

Description
-----------
A simple React component that displays a modal with a title, description, and a close button.

Installation
------------
To use this component in your React project, follow these steps:

1. Install the required dependencies:
npm install react

2. Copy and paste the `Modal` component code into your project.

Usage
-----
To use the `Modal` component, import it into your React file:

```jsx
import React, { useState } from 'react';
import Modal from '@gwendish/modal-react';

const App = () => {
// Define state and functions for handling the modal's open/close state
const [isModalOpen, setIsModalOpen] = useState(false);

const handleModalOpen = () => {
 setIsModalOpen(true);
};

const handleModalClose = () => {
 setIsModalOpen(false);
};

return (
 <div>
   {/* Button to open the modal */}
   <button onClick={handleModalOpen}>Open Modal</button>

   {/* Render the modal component */}
   <Modal
     title="Modal Title"
     description="This is the content of the modal. You can put any text or JSX here."
     onClose={handleModalClose}
   />
 </div>
);
};

export default App;

```
Props
-----
The `Modal` component accepts the following props:

- `title` (string, required): The title to display at the top of the modal.
- `description` (string, required): The description or content to display inside the modal.
- `onClose` (function, optional): A callback function to be executed when the modal is closed. You can perform any necessary cleanup or actions in this function.
- `modalBackground` (string, optional): The background color of the modal. Default is 'rgba(0, 0, 0, 0.5)' (semi-transparent black).
- `containerBackground` (string, optional): The background color of the modal container. Default is '#fff' (white).

Styling
-------
You can customize the appearance of the modal and button using the following inline styles:

- `modalStyles`: To set the background color of the modal. Default is 'rgba(0, 0, 0, 0.5)'.
- `containerStyles`: To set the background color of the modal container. Default is '#fff'.
- `buttonStyles`: To customize the appearance of the close button.

Feel free to adjust the styles and use this `Modal` component in your project!

License
-------
This project is licensed under the MIT License - see the LICENSE file for details.

Contributing
------------
Contributions are welcome! If you find any issues or have suggestions for improvement, feel free to open an issue or submit a pull request.

Author
------
Gwendish