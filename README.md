# Python package template project

This is a template project for a Python package. It is intended to be used as a starting point for creating a new Python package.

# Usage and installation

To install all the packages included on the template, run the following commands (on the root of the project):

```bash
    source venv/bin/activate
    pip install -r requirements.txt
```

# Development

An example of how package imports works can be found on the `src/my_project/` folder. The `hello_world.py` file contains an import of the `util_function.py` function. To run the example, run the following command (on the root of the project):

```bash
    python src/my_project/hello_world.py
```

As you can see, the `util_function.py` file is imported and the function `util_function` is called. The function prints a message to the console.

The way to import modules from within the package is by using the following syntax:

```python
    from my_project.<module_name> import <function_name>|<class_name>|<variable_name>
```

# Testing

To run the tests, run the following command (on the root of the project):

```bash
    pytest
```

Files on `tests/` folder shall be named as `test_<module_name>.py` to be recognized by pytest.

Tests are configured to analyze the coverage of the package, in this case `my_project` package (contained on `src/my_project/` folder).

# Customization

To change package name and other metadata, edit the `setup.cfg` file which contains the metadata of the package. Also you can do some changes on `pyproject.toml` which contains the configuration for the package and pytest configuration.

For example if you want to change the package name, edit the `setup.cfg` file and chage the following fields to the desired name:

-   `name` under `[metadata]`
-   `packages` under `[options]`

Also you should change `pyproject.toml` file and change the `addopts` field under `[tool:pytest]` to the new package name, so the tests can be run correctly and coverage on the package can be calculated.

And then you should change the name of the package folder from `my_project` to the new name.
