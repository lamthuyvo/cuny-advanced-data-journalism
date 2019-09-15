# Your first Jupyter Notebook!

Setting up a jupyter notebook project can be A LOT. While you have the slides from your class [here](https://docs.google.com/presentation/d/1v2ef_bdJKTJhhsH5t2IU9vpKjzqkG6_9sTsCb3SEyA0/edit?usp=sharing), feel free to use this quick run-down of commands for when you're in a hurry to get your data analysis started.

![TMI!](https://media.giphy.com/media/l3q2Ph0I1osaagoQE/giphy.gif)

Below is a quick rundown of commands:

### Organize your data projects

Make a project folder, then make three folders inside of the folder:

- one for all your raw input data called `data` (this is where all the data goes in its original format)
- one for all your output data, meaning the results of your data. Call this folder `output`
- then you need a folder for all your notebooks, where you will store all of your Python-based analyses. This folder should be called `notebooks`

### Make your virtual environment

To make your virtual environment for your project, navigate to your overall project folder by using the `cd` command. Then run this command:

```
python3 -m venv venv
```
Activate your project:
```
source venv/bin/Activate
```
Your virtual environment is activated if you see the string `(venv)` at the beginning of your command line.

Then you can run the folllowing command to install `jupyter`:

```
pip3 install jupyter
```
And then `pandas`:

```
pip3 install pandas
```

### Using Jupyter Notebooks

While your environment is activated, run the command:
```
jupyter notebook
```
That should open the web app in Chrome or whatever your default browser is. Click on the notebooks folder and then use the dropdown menu `New` to select a new `Notebook: Python 3` notebook.

Now you have a Jupyter notebook and can start messing with your data!
