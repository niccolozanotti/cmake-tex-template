# cmake-tex-template

This project is meant to be a quick start template to write a LaTeX document whose compilation is handled by Cmake through UseLATEX [module](https://gitlab.kitware.com/kmorel/UseLATEX/).

For more information check out the documentation of UseLATEX [here](https://gitlab.kitware.com/kmorel/UseLATEX/).

## Dependencies

This project has the following dependencies:
- [CMake](https://cmake.org)
- [LaTeX](https://www.latex-project.org) 

First, check if `CMake` is installed by running
```shell
cmake --version
```
If CMake is installed, you should see an output with the version number, such as:
```shell
cmake version 3.xx.x
```
If you get an error or CMake is not installed check the [instructions below](#installing-cmake).

To check if `LaTeX` is installed and available in your system’s path, run the following command:
```shell
latex --version
```
If LaTeX is installed, you should see an output with the version number, such as:
```shell
pdfTeX 3.x.x
```
If you get an error or LaTeX is not installed, check the [instructions below](#installing-latex).

## Build the files
One way to quickly compile the `.tex` files into the relative `.pdf` is by running
```shell
mkdir build
cd build
cmake ..
make target-name 
```
The `target-name.pdf` file will then be located in the `build/` directory.

## Installation instructions 

### Installing LaTeX

#### macOS (via [Homebrew](https://brew.sh))
 Open a terminal and run:
```shell
brew install --cask mactex  # or mactex-no-gui for the lighter version without the GUI
```

#### Linux (Debian/Ubuntu)
Open a terminal and run:
```shell
sudo apt-get update
sudo apt-get install texlive-full
```
On other distributions, use the equivalent package manager (e.g., dnf for Fedora, pacman for Arch).

#### Windows
Download the full MiKTeX installer from the MiKTeX website, and follow the installation instructions.

Alternatively, you can install it via Chocolatey by running:
```shell
choco install miktex
```

### Installing CMake 
#### macOS (via [Homebrew](https://brew.sh))
Open a terminal and run:
```shell
brew install cmake
```

#### Linux (Debian/Ubuntu)
Open a terminal and run:
```shell
sudo apt-get update
sudo apt-get install cmake
```
On other distributions, use the equivalent package manager (e.g., dnf for Fedora, pacman for Arch).

#### Windows
Download the latest installer from the [official CMake website](https://cmake.org/download/), and follow the installation instructions.

Alternatively, you can install CMake through a package manager like Chocolatey by running:
```shell
choco install cmake
```
---

### UseLatex module update

If any change in the upstream Cmake module [UseLatex.cmake](UseLATEX.cmake) is detected (the Github [Action](.github/workflows/update-cmake-module.yml)
runs monthly[^1]) a new Pull Request will be opened to integrate the changes.

## License

This project is licensed under the [MIT LICENSE](LICENSE).

---
[^1]: You can also manually trigger an update with a manual dispatch if you need. 
