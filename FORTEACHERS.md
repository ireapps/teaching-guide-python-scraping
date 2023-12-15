# Web scraping with Python conference teaching guide
Thank you for volunteering to teach this one-hour session at our conference! This teaching guide explains our setup and the material we try to cover.

The exercises live in [the "Web scraping with Python" Jupyter notebook](https://github.com/ireapps/teaching-guide-python-scraping/blob/master/Web%20scraping%20with%20Python.ipynb). [The other notebook](https://github.com/ireapps/teaching-guide-python-scraping/blob/master/Python%20syntax%20cheat%20sheet.ipynb) has a refresher on some basic Python syntax for folks who are new to Python or could use a reference.

## Take it for a spin
At the conference, this repository will be on the conference computers, the virtual environment created and the dependencies (`jupyterlab`, `requests`, `bs4`) installed and tested. You'll probably want to give it a spin before the conference, though. You'll need Python 3 installed on your computer.

1. Clone or [download/unzip](https://github.com/ireapps/teaching-guide-python-scraping/archive/master.zip) this repo onto your computer
2. In your command-line interface, cd into the folder
3. Create a virtual environment (using `venv` or your tooling of choice):
    - Macs: `python3 -m venv env`
    - PCs: `python -m venv env`
4. Activate the virtual environment:
    - Macs: `source env/bin/activate`
    - PCs: `.\env\Scripts\activate`
5. `pip install -r requirements.txt`
6. `jupyter lab`

## Session description
This session will show you how to use the Python programming language to scrape data from simple websites.

This session is good for: People with some experience working with data. Experience with Python and/or HTML is a plus but not necessary.

## Session goals
Some of the ground you want to cover:
- How to write and run Python code in a Jupyter notebook
- Browser tools for inspecting the source code of a web page
- How to use the `requests` library to fetch the HTML code for a web page
- How to use the `beautifulsoup4` library to parse the HTML
- Using `beautifulsoup4`'s `find()` and `find_all()` methods to target and extract information
- Writing the results of a scrape to a CSV (if time)
- Where to find [instructions for installing Python on their own machines](https://docs.google.com/document/d/1cYmpfZEZ8r-09Q6Go917cKVcQk_d0P61gm0q8DAdIdg/edit#) (or tell them about [JupyterLab desktop](https://github.com/jupyterlab/jupyterlab-desktop) or direct them to your install guide of choice)
- How to find help when they get stuck

## General approach
I Do, We Do, You Do. Demonstrate a concept, work through it together, then give them plenty of time to experiment on their own while you and your coach walk around and answer questions (see sections marked `✍️ Try it yourself`).

The pace will be slower than you think, and that's OK! It's not the end of the world if you don't get through everything. Many people who come to this class will have zero experience with programming.

## Class setup
We'll have the latest version of Python 3 installed. We're using the standard library's `venv` module to manage the virtual environment and project dependencies (`jupyterlab`, `bs4` and `requests`), which will already have been installed and tested prior to your session. Please refer to the Python setup sheet for the conference and let us know if you have any questions.

## Class outline

### Start up the notebook server
Begin the class by walking everyone through the process of activating their virtual environments and launching JupyterLab:
1. Open the command-line interface
2. `cd` into your class directory (or, if you're on a Mac, you could have them right-click on the class folder and select `Services > New Terminal at folder`)
3. Activate the virtual environment:
    - Macs: `source env/bin/activate`
    - PCs: `.\env\Scripts\activate`
4. `jupyter lab`

It will take everyone a few minutes to get going. You'll also probably get some questions about what you're doing at this step. Try to avoid a lengthy digression into virtual environments -- it's beyond the scope of this hourlong session, so maybe offer to talk to them after class, or send 'em our way: [training@ire.org](mailto:training@ire.org).

Once everyone is good to go, toggle back to the terminal and show them what's going on: A Jupyter server is running in the background, so don't close the terminal window.

Go over some notebook basics: Adding cells, writing code and running cells, etc. A common gotcha: Writing code that other cells depend on but forgetting to first _run_ it to make it available.

### Main course content
Start working your way through the notebook: Practice inspecting a web page, fetch a web page, parse the HTML, target and extract the data, write to CSV (if time). Pause frequently to ask if anyone has questions. There's a bunch of text at the beginning of the notebook that's mostly for them to read and reference, not necessarily a list of things to cover.

Any time you see `✍️ Try it yourself`, hit the brakes and give everyone a little time to play around with whatever concept you're discussing.

In IRE's experience, you'll want to budget more time than you'd think for showing how to parse data out of the BeautifulSoup object.

If you have Internet problems, you can pivot and work on the HTML file saved in this directory, `sd-warn.html` -- there's a cell with some commented-out code that folks can run to read in the HTML.

### Debugging
If you can, find an opportunity when someone has gotten an error and take a few minutes to walk through basic debugging strategy: Reading the traceback error from bottom to top, strategic Googling, etc.

### If you have extra time at the end
You can set them on the extra credit problems at the end of the notebook or oversee some unstructured lab time -- they can practice scraping other web pages or look up additional methods for navigating the souped HTML, etc.

### Ending the session
1. Have everyone close out of their notebook tabs
2. In terminal, `Ctrl+C` to kill the server process
3. Close the terminal window
