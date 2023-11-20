# Spruce is no longer maintained

![Spruce 3 - Bruce Lee](http://cbsnews1.cbsistatic.com/hub/i/2014/03/08/2653257f-848f-4e81-8db9-b9a8bfdcd00e/bruce-lee-big-boss-47.jpg)

Spruce is a command line tool that looks for objects on your Jamf Pro server which have no current usage, are out of date, or are otherwise "crufty". It can optionally remove objects from its findings.

## Requirements

This version of Spruce requires Python 3.8. To create a virtual environment for Spruce, follow these steps.

1. Use a local clone of relocatable-python to build a Python 3.8 framework.

    ```sh
    cd ~/src/Spruce
    ~/src/relocatable-python/make_relocatable_python_framework.py --python-version 3.8.10 --os-version 11
    ```

    This should result in a _Python.framework_ bundle being created in your Spruce clone directory.

1. Install virtualenv.

    ```sh
    Python.framework/Versions/Current/bin/python3.8 -m pip install virtualenv
    ```

1. Create a virtual environment and activate it.

    ```sh
    Python.framework/Versions/Current/bin/python3.8 -m virtualenv --python 3.8 venv
    source venv/bin/activate
    ```

1. Install remaining requirements.

    ```sh
    pip install -r requirements.txt
    ```

1. Verify Spruce runs by viewing its help.

    ```sh
    python3 ./spruce.py -h
    ```

## Instructions for use

**For details on how to use Spruce, please visit our [Wiki](https://github.com/jssimporter/Spruce/wiki).**

**IMPORTANT:**
Spruce 3 requires python-jss 2.1.0 and python3, with the `Foundation` module. The simplest way to achieve this is to install [AutoPkg](https://github.com/autopkg/autopkg/releases/) 2.0 and [JSSImporter](https://github.com/jssimporter/JSSImporter/releases) 1.1.0, and then run Spruce using the python that is supplied with AutoPkg:

    /usr/local/autopkg/python spruce.py -h

## Acknowledgements

Huge thanks to Shea Craig, who wrote the bulk of this work and is still providing advice, though not currently involved in Jamf administration.

The world of Mac administration evolves fast, and continued functionality of Spruce and python-jss requires active engagement from the Jamf-using Mac Admin community. If you think you can help and have ideas, please go ahead and file issues and pull requests, or contact us in the MacAdmins Slack `#jss-importer` channel.

## License

See the [LICENSE](https://github.com/grahampugh/Spruce/blob/master/LICENSE.txt) file.
