# 🐍 Robust Python Source Installer for Termux 🛠️

This shell script automates the process of downloading, configuring, compiling, and installing a specific version of Python from source code directly within the Termux environment.

It includes crucial platform-specific fixes to ensure a stable and successful build on Android.

## ✨ Key Features

* **Automated Compilation:** Handles the entire `configure`, `make`, and `make install` workflow.
* **Termux Compatibility:** Includes necessary configuration flags (`ac_cv_func_close_range=no`, etc.) to resolve common build errors specific to the Termux/Android platform.
* **Dependency Management:** Automatically installs required build packages (`build-essential`, `wget`, `tar`, etc.) using `pkg install`.
* **Robust Error Handling:** Stops the build process, dumps the comprehensive error log, and cleans up temporary files if any step fails.
* **Parallel Compilation:** Speeds up the compilation process by utilizing all available CPU cores (`make -j $(nproc)`).

## 🚀 Usage

### Prerequisites

You must have Termux installed on an Android device. Ensure you have network connectivity for downloading dependencies and the Python source code.

### 1. Download the Script

First, save the script (e.g., as `install_py.sh`) to your Termux home directory.


# Example: Download the raw script file
git clone https://github.com/omar-termux/installpy.git

chmod +x installpy/installpy.sh

