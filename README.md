# Advanced Thermodynamics Simulator

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
<!-- Remove or update the build status badge if you don't have CI set up -->

## Overview

This project is an interactive, web-based thermodynamics simulator created by a Chemical Engineering student.  It's designed as an educational tool to visualize and explore fundamental thermodynamic concepts, particularly phase diagrams and thermodynamic processes. The simulator is built with React, [react-konva](https://konvajs.org/docs/react/Intro.html) (for efficient canvas rendering), and [lodash](https://lodash.com/).  The primary goal is to provide a clear, interactive learning experience, and I warmly welcome contributions from fellow students, educators, and developers to improve its accuracy, expand its features, and make it a valuable resource for the thermodynamics community.

## Features

*   **Interactive Particle Animation:** Visualize the behavior of particles in different phases (solid, liquid, gas, supercritical fluid) as temperature and pressure change.  This provides an intuitive understanding of phase transitions.
*   **Phase Diagram:** Explore the relationship between temperature, pressure, and phase transitions on an interactive phase diagram (currently a simplified model for a water-like substance).
*   **Thermodynamic Processes:** Simulate and visualize key thermodynamic processes:
    *   Isochoric (constant volume)
    *   Isothermal (constant temperature)
    *   Isobaric (constant pressure)
    *   Adiabatic (no heat transfer)
*   **PV and T-P Diagrams:** Observe the state changes during these processes on dynamic PV and Temperature-Pressure diagrams.
*   **Adjustable Parameters:** Control temperature, pressure, volume, and animation speed using interactive sliders.
*   **State Trace:** Visualize the system's state history on the diagrams.
*   **Educational Content:** Brief explanations of the Ideal Gas Law, thermodynamic processes, and phase transitions are included.
*   **Responsive Design:** The simulator adapts to different screen sizes (desktop, tablet, mobile).
*   **Open Source (MIT License):** The code is freely available for use, modification, and distribution.

## Live Demo

[https://Prasanna163.github.io/my-thermodynamics-simulator/](https://Prasanna163.github.io/my-thermodynamics-simulator/)  <!-- **REPLACE THIS WITH YOUR GITHUB PAGES URL** -->

## Getting Started

To run the simulator locally (for development or experimentation):

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/YOUR_USERNAME/your-repository-name.git
    cd your-repository-name
    ```
    (Replace `YOUR_USERNAME` and `your-repository-name` with your GitHub username and repository name.)

2.  **Install dependencies:**

    ```bash
    npm install
    ```

3.  **Start the development server:**

    ```bash
    npm start
    ```

    This will open the simulator in your default web browser (typically at `http://localhost:3000`).

## Project Structure

The project follows a standard Create React App structure, with the core logic residing within the `src` directory:

-   **`public/`**:  This directory holds static assets.
    -   `index.html`:  The main HTML file.  React injects the compiled application code into this file.  You generally don't need to modify this directly.
    -   Other assets (favicon, images, etc.) can be placed here.

-   **`src/`**:  This is where the React application's source code lives.
    -   `App.js`:  The main React component.  This file contains:
        -   The `ThermodynamicsSimulator` component, which manages the entire application's state and logic.
        -   The JSX (HTML-like syntax) that defines the user interface.
        -   `useEffect` hooks for handling side effects (like animation and thermodynamic process updates).
        -   Event handlers for user interactions (slider changes, button clicks, etc.).
    -   `App.module.css`:  A CSS Module that contains the styles specifically for the `App.js` component.  Using CSS Modules ensures that styles are scoped to the component, preventing naming collisions.
    -   `index.js`: The entry point for the React application. It renders the `App` component into the `root` element in `public/index.html`.  You usually don't need to modify this.

-   **`.gitignore`**:  A crucial file that tells Git which files and directories to *ignore*.  This prevents large and unnecessary files (like the `node_modules` directory) from being tracked in your repository.

-   **`package.json`**:  This file contains important project information:
    -   **`name`, `version`, `description`**: Basic project metadata.
    -   **`dependencies`**:  A list of the project's runtime dependencies (e.g., `react`, `react-konva`, `lodash`).
    -   **`devDependencies`**:  A list of dependencies used only during development (e.g., `gh-pages` for deployment).
    -   **`scripts`**:  Defines commands that can be run with `npm` (e.g., `npm start`, `npm run build`, `npm run deploy`).
    - **`homepage`**: Specifies the URL where the application will be deployed.

-   **`README.md`**:  This file (the one you're reading!) provides a description of the project, instructions for running it, contribution guidelines, and other important information.

-   **`LICENSE`**: This file contains the license information, specifying how others can use and distribute your project.

## Contributing

As a Chemical Engineering student, I created this project to enhance my own understanding and to share it with others. I enthusiastically welcome contributions from anyone interested in thermodynamics, simulations, or React development!  Your help can significantly improve the accuracy, scope, and educational value of this simulator.

**Here are some areas where you can contribute:**

*   **Accuracy and Validation:**
    *   Improve the accuracy of the phase diagram and thermodynamic process calculations. The current model is simplified; adding more realistic equations of state (e.g., Van der Waals, Peng-Robinson) would be a major improvement.
    *   Validate the simulator's results against experimental data or established thermodynamic models.
    *   Add error handling and input validation to prevent unexpected behavior.

*   **New Features and Models:**
    *   Implement support for different substances (beyond the current water-like model).  Allow users to select substances or input their properties.
    *   Add simulations for mixtures of substances.
    *   Visualize additional thermodynamic properties (enthalpy, entropy, Gibbs free energy, chemical potential).
    *   Incorporate chemical reaction kinetics and equilibrium.
    *   Explore more advanced thermodynamic concepts (e.g., fugacity, activity coefficients).
    * Develop models for Heat transfer.
    * Include Heat Engines and refrigeration cycles.

*   **UI/UX Improvements:**
    *   Enhance the user interface to make it more intuitive and user-friendly.
    *   Improve the visual clarity of the diagrams and animations.
    *   Add interactive elements to the phase diagram (e.g., click to set temperature/pressure).
    *   Create more detailed explanations and tooltips.

*   **Code Quality:**
    *   Refactor the code to improve its organization, readability, and maintainability.
    *   Add comments and documentation.
    *   Write unit tests to ensure the code's correctness.

*   **Bug Fixes:**
    *   Identify and fix any bugs you find.

**Contribution Guidelines:**

1.  **Fork the repository** on GitHub.
2.  **Create a new branch** for your contribution: `git checkout -b feature/your-feature-name` (or `bugfix/your-bug-fix`).
3.  **Make your changes** to the code.
4.  **Commit your changes** with clear and descriptive commit messages.
5.  **Push your branch** to your forked repository: `git push origin feature/your-feature-name`.
6.  **Open a pull request** from your forked repository to the `main` branch of the original repository. Describe your changes and explain why they are beneficial.  Include any relevant screenshots or data.
7. **Code Review and Collaboration**: I, and hopefully other contributors, will review your pull request.  We may ask for clarifications, suggest changes, or discuss alternative approaches.  Be prepared to collaborate and iterate on your contribution.

**No contribution is too small!** Even fixing a typo or improving a comment is valuable.

## License

This project is licensed under the **MIT License**. This is a very permissive license that allows you to use, modify, and distribute the code for any purpose, including commercial use, *as long as you include the original copyright notice and disclaimer*.  See the [LICENSE](LICENSE) file for the full text.  This open license encourages collaboration and sharing.  By contributing, you agree that your contributions will also be licensed under the MIT License.

## Acknowledgments

*   [React](https://reactjs.org/)
*   [react-konva](https://konvajs.org/docs/react/Intro.html)
*   [lodash](https://lodash.com/)
*   [Create React App](https://create-react-app.dev/)

I hope this simulator is a helpful tool for learning and exploring thermodynamics.  I look forward to your contributions!
