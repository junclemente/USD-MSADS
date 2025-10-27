# Install Windows Subsystem for Linux (WSL2)


_WSL2 (Windows Subsystem for Linux 2) is the second iteration of Microsoft's compatibility layer that allows Windows users to run a Linux environment directly within Windows, without the need for a separate virtual machine or dual-boot setup. It provides a lightweight and seamless integration of Linux with Windows._


If you do not already have WSL2 installed on your Windows machine, follow the directions on this page to install WSL2 and Ubuntu.

Open powershell and type the following:

```powershell
wsl --install
```

This will install WSL2 and Ubuntu by default.

**Source:** [How to install Linux on Windows WSL](https://learn.microsoft.com/en-us/windows/wsl/install)

# Install miniconda in Ubuntu (WSL2)


_Miniconda is a minimal installer for Conda, a package and environment manager for Python. It provides a lightweight alternative to Anaconda, allowing users to create and manage Python environments without pre-installing a large set of libraries._

Next, open Ubuntu and install miniconda.

Enter the following lines:

```bash
mkdir -p ~/miniconda3
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm -rf ~/miniconda3/miniconda.sh
```

After installing miniconda, initialize the bash and zsh shells:

```bash
~/miniconda3/bin/conda init bash
~/miniconda3/bin/conda init zsh
```

**Source:** [Miniconda: Quick command line install](https://docs.anaconda.com/miniconda/)
