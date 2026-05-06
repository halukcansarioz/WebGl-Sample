
# 🧊 WebGL Sample Projects
### (Computer Graphics Course – WebGL Exercises & Assignments)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)](#)
[![WebGL](https://img.shields.io/badge/WebGL-990000?style=flat&logo=webgl&logoColor=white)](#)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)](#)

This repository contains my **Computer Graphics** course projects and experiments using **WebGL**. It covers shader management, model transformations, interaction, and well‑known fractal structures, all rendered directly in the browser.

## 📚 Table of Contents
- [About the Project](#about-the-project)
- [Features](#features)
- [Technologies & Resources](#technologies--resources)
- [Installation & Usage](#installation--usage)
- [Project Structure](#project-structure)
- [Development Process](#development-process)
- [Contributing](#contributing)
- [Contact](#contact)
- [License](#license)

---

## About the Project
This work was created to learn the fundamentals of computer graphics (model‑view transformations, lighting models, buffer objects) through hands‑on WebGL applications. Each folder is an independent, runnable WebGL scene.

- **Developer:** Haluk Can SARIÖZ
- **Course:** Computer Graphics
- **Goal:** Understand GPU‑based programming and OpenGL ES shader structures

---

## Features
- **Real‑Time Rendering:** GPU‑accelerated graphics directly in the browser.
- **Multiple Examples:** From basic primitive drawing to shaded objects and interactive applications.
- **Phong Lighting Model:** Practical implementation of Phong reflection in `Shaded Teapot` and related assignments.
- **User Interaction:** Mouse and keyboard control of 3D objects (especially the Utah teapot).
- **Helper Libraries:** Effective use of `initShaders` and `MV.js` provided during the course.

---

## Technologies & Resources
- **WebGL (OpenGL ES 2.0)** – Core graphics API.
- **JavaScript (ES6)** – Application logic and shader management.
- **HTML5 Canvas** – Rendering surface.
- **Educational Sources:** The projects heavily rely on Prof. Edward Angel’s resources:
  - [WebGL Examples (UNM)](https://www.cs.unm.edu/~angel/WebGL/)
- **Theory:**
  - [Phong Reflection Model (Wikipedia)](https://en.wikipedia.org/wiki/Phong_reflection_model)

---

## Installation & Usage

These projects contain no server‑side code, so no package installation is required. **However**, because WebGL shaders are loaded from external files, you **must** run them via a local server (opening the HTML files directly may be blocked by browser security policies).

### 1. Clone the Repository
```bash
git clone https://github.com/halukcansarioz/WebGl-Sample.git
```

### 2. Navigate to the Folder
```bash
cd WebGl-Sample
```

### 3. Start a Local Server

Choose one of the methods below:

- **VS Code Live Server (recommended):** Right‑click any `.html` file → “Open with Live Server”.
- **Node.js `http-server`:**
    ```bash
    npx http-server .
    ```
    Then open the address shown (usually `http://127.0.0.1:8080`).
- **Python:**
    ```bash
    python -m http.server
    ```

### 4. Navigate & Enjoy
Browse to the desired folder (e.g., `Base/`, `Shaded Teapot/`) and open the corresponding `.html` file.

> ⚠️ **Note:** Your browser must support WebGL (all modern browsers do).

---

## Project Structure
Each folder represents an independent WebGL application, typically containing an `.html` interface file, a `.js` logic/shader file, and common libraries in `src`.

```text
WebGl-Sample/
├── Base/                 # Basic polygon (cube) drawing and coloring
├── Rotation/             # Rotation transforms
├── Teapot/               # Classic Utah Teapot rendering
├── Shaded Teapot/        # Teapot with Phong lighting model
├── View/                 # Camera and view angle settings
├── Interaction/          # Mouse/keyboard interactive teapot
├── Sierpinski/           # 2D Sierpinski Triangle fractal
├── Sierpinski-2/         # Advanced Sierpinski implementation
├── İlk/                  # First WebGL attempt (beginner level)
├── Ödev/                 # Submitted assignment(s)
├── Ödev Örnek/           # Reference example for the assignment
├── Ödev-2/               # Second assignment
└── README.md             # This file
```

---

## Development Process

### 1. Fork the Repository
You can fork the project to add your own graphics experiments.

### 2. Create a New Branch
```bash
git checkout -b feature/new-shader-demo
```

### 3. Push Your Code
```bash
git push origin feature/new-shader-demo
```

---

## Contributing
1. **Fork** this repository.
2. Create a **Branch** (`git checkout -b feature/NewScene`).
3. Add your `.html` and `.js` files in a new folder.
4. **Commit** your changes (`git commit -m 'Add: New lighting example'`).
5. **Push** your branch (`git push origin feature/NewScene`).
6. Open a **Pull Request**.

> 💡 **Tip:** When adding a new example, reuse the `src` folder for helper functions like `initShaders` and `MV.js`.

---

<a name="contact"></a>
## Contact
**Haluk Can Sarıöz**
- GitHub: [@halukcansarioz](https://github.com/halukcansarioz)
- Email: [halukcansarioz19@gmail.com](mailto:halukcansarioz19@gmail.com)
- LinkedIn: [Haluk Can Sarıöz](https://www.linkedin.com/in/halukcansarioz)

**Project Link:** [https://github.com/halukcansarioz/WebGl-Sample](https://github.com/halukcansarioz/WebGl-Sample)

---

*Found this helpful? Please ⭐ the repository!*

---

## License
This project is licensed under the [MIT License](LICENSE).
