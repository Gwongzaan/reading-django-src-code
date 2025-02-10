`setup.py` is a script commonly used in Python projects for packaging and distribution. It is part of the setuptools library and serves as the configuration file for defining how a Python package should be installed, built, and distributed.

## **Purpose of `setup.py`**

1. **Package Metadata** – It provides essential details like package name, version, author, description, and dependencies.
2. **Dependency Management** – Lists external libraries required for the package.
3. **Installation Instructions** – Defines how the package should be installed using `pip` or `setuptools`.
4. **Entry Points** – Allows defining console scripts or command-line tools.
5. **Distribution** – Helps create distributable formats (`wheel` or `source tarball`).
6. **Custom Commands** – Can be extended to include custom installation behaviors.

---

## **Basic Structure of `setup.py`**

Here’s a simple example:

```python
from setuptools import setup, find_packages

setup(
    name="my_package",
    version="0.1",
    author="Your Name",
    author_email="your.email@example.com",
    description="A simple Python package",
    long_description=open("README.md").read(),
    long_description_content_type="text/markdown",
    url="https://github.com/yourusername/my_package",
    packages=find_packages(),
    install_requires=[
        "requests",  # Dependencies
        "numpy"
    ],
    entry_points={
        "console_scripts": [
            "mycommand=mypackage.module:main_function"
        ]
    },
    classifiers=[
        "Programming Language :: Python :: 3",
        "License :: OSI Approved :: MIT License",
        "Operating System :: OS Independent",
    ],
    python_requires='>=3.6',
)
```

---

## **How `setup.py` Works**

1. **Installing the Package Locally**

    ```sh
    python setup.py install
    ```

    - Installs the package and dependencies.

2. **Editable Mode (for Development)**

    ```sh
    pip install -e .
    ```

    - Allows modifying the package without reinstalling.

3. **Building a Distribution**

    ```sh
    python setup.py sdist bdist_wheel
    ```

    - Creates a `tar.gz` (source distribution) and `.whl` (binary wheel).

4. **Uploading to PyPI** (Requires `twine`)
    ```sh
    twine upload dist/*
    ```
    - Publishes the package to PyPI.

---

## **Alternatives**

-   **`pyproject.toml`**: The modern replacement for `setup.py`, used with `setuptools`, `poetry`, or `flit`.

-   [ ] develop a very simple example to see how setup and setuptools work.
-   [ ] develop a simple example to see how the modern approach using setup.cfg work.
-   [ ] compare and see the difference between using `setup.py` and `setup.cfg`, why one not the other.
