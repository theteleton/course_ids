# Python programming language

## Basic characteristics

Python is an interpreted, dynamically typed, object-oriented programming language.

Advantages:

* Simple.
* Easy to learn.
* Extensive packages.
* Cross-platform.
* Free and open source.
* Large user base.

Disadvantages:

* Being interpreted results in slower execution.
* Dynamic typing can lead to errors that only show up at runtime.
* Less suitable for mobile development and mobile computing.
* Higher memory consumption, less suitable for memory-intensive tasks.
* Underdeveloped database access layers.

## Why Python?

The Python language is one of the two most popular languages for data science (the other being R). The two main reasons are:

* The advantages of Python fit the typical data science workflow and its disadvantages are not that deterimental to the data science workflow.
* Python has a large ecosystem of packages, libraries and tools for data science, some of which are discussed later in this chapter.

The typical data science workflow consists of acquiring and manipulating data and applying standard machine learning or statistical methods. In essence, the data flows through different methods. The emphasis is on obtaining results - extracting meaningful information from data.

The advantages of Python are extremely beneficial to such a workflow: Being simple, easy to learn and free, it is accessible to a larger user base, including users with little or no prior programming experience. Being an interpreted language (and straightforward piecewise execution through read-eval-print loop shells or REPL) makes Python very flexible - multiple alternatives can be explored and quick decisions made on how to procede, depending on intermediary results.

The disadvantages of Python are of minor consequence: The data science workflow is not time-critical - even an order-of-magnitude slowdown typically makes little difference. Code maintainability is less important - data science scripts are often short and discarded after use. Mobile development, mobile computing or enterprise-level database work are also not part of the typical data science workflow.


## Setting up

Before using Python, we need first to select and install a desired distribution. One can choose to install pure Python distribution or Anaconda Python distribution. Some advantages of using Anaconda are:

* Anaconda gives the User ability to make an easy install of the version of python he/she wants. But generally, it depends on a user preference which distribution to use. Anaconda will also resolve all the problems with admin privileges if a user does not have admin rights for his system.
* [Anaconda Accelerate](https://docs.continuum.io/accelerate/index.html) can provide a user with high performance computing and several other components.
* Anaconda removes bottlenecks involved in installing the right packages while taking into considerations their compatibility with various other packages as might be encountered while using the traditional pip.
* There is no risk of messing up required system libraries. There are also many open source packages available for Anaconda, which are not within the pip repo.

We encourage you to use Anaconda Python distribution but the final choice is yours.

### Anaconda installation

Install the desired Anaconda Python distribution from [https://www.anaconda.com/distribution/](https://www.anaconda.com/distribution/). A useful way of managing multiple Python project is by using Conda environments. An environment enables you to use a specific Python version along with specific dependencies completely separately. To create and use an environment with a name *itds*, issue the following command:


```bash
conda create -n itds
conda activate itds
```

While in the environment, you can run environment-specific Python and install packages only to the environment (the example below will install additiona Anaconda features to Jupyter notebook):


```bash
conda install nb_conda
```

To exit the environment, use `conda deactivate`. To show existing environments and their locations, issue `conda info --envs`. 

### Pure Python installation

You can also install pure Python directly to your system from [https://www.python.org/downloads/](https://www.python.org/downloads/).

To run Python, issue `python` command in the console (there may be more interpreters installed on your machine and Python 3.5 might be run also using `python3.5`). After running the command, you should see something similar to the following:


```bash
quaternion:~ slavkoz$ python3.5
Python 3.5.2 (v3.5.2:4def2a2901a5, Jun 26 2016, 10:47:25)
[GCC 4.2.1 (Apple Inc. build 5666) (dot 3)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

Packages can be installed using `pip` command: 


```bash
pip install nltk
```

It can happen that in some cases, packages will be prebuilt or istallation of its dependencies can be tedious. In such cases, *wheel packages* can be provided and installed using the following command:


```bash
pip install YOUR_DOWNLOADED_PACKAGE.whl
```

## Python in 15 minutes

### Hello world! {-}


```python
print("Hello World!")
```

```
## Hello World!
```

### Variables and types {-}

#### Numbers and basic operators {-}


```python
a = 3  
b = 2.5  
c = a + b 
c = a * b
c = a / b
```

#### Strings and concatenation {-}


```python
a = "data" 
b = 'science' # we can use double and single quotes
c = a + " " + b
print(c)
```

```
## data science
```

#### Boolean {-}


```python
a = True
b = False
```

#### Iterables: Lists, Tuples, Sets {-}


```python
a = [1, 2, 3]          # List  
a = (1, 2, 3)          # Tuple (immutable)
a = {"a", "b", "c"}    # Set
```

#### Dictionaries {-}


```python
dict = {
  "title": "Introduction to Data Science",
  "year": 1,
  "semester": "fall",
  "classroom": "P02"
}
dict["classroom"] = "P03" 
```

### String formatting {-}

???

### More operators {-}


```python
a = "a"
print((a in {"a", "b"} and True) or False)
```

```
## True
```

```python
print(not True)
```

```
## False
```

### Control flow {-}

#### If-then-else {-}


```python
a = 2  
if a > 1:  
    print('a is greater than 1')
elif a == 1:  
    print('a is equal to 1')
else:  
    print('a is less than 1')
```

```
## a is greater than 1
```


#### Loops {-}


```python
for i in range(4, 6):
    print(i)
```

```
## 4
## 5
```

```python
people_list = ['Ann', 'Bob', 'Charles']  
for person in people_list:
    print(person)
```

```
## Ann
## Bob
## Charles
```

```python
i = 1
while i <= 3:
  print(i)
  i = i + 1
```

```
## 1
## 2
## 3
```

### Functions

???

### Classes and objects

???

### Python IDE's {-}

IDLE, PyCharm, Jupyter Notebook, VS Code and similar (brief descriptions with advantages/disadvantages)


### Python ecosystem for Data Science {-}

The Python ecosystem of libraries, frameworks, and tools is large and ever-growing. Python can be used for web scraping, machine learning, general scientific computing, and many other computing and scripting uses.

Some of the most popular packages:

* **scikit-learn**
* **Scipy**
* **Matplotlib**
* **Numpy** 
* **Pandas**

Some of the most popular tools:

* **TensorFlow, Keras** - Deep learning.

## Further reading and references

good books? references? online tutorials? quick reference sheets? anything that would help the students on the path to achieveing goals from previous section

* Python Tutorials: https://docs.python.org/3/tutorial/index.html

## Learning outcomes

Data science students should work towards obtaining the knowledge and the skills that enable them to:

* Use the Python programming language for common programming tasks, data manipulation, file I/0, etc.
* Identify the Python IDE(s) that best fit their requirements.
* Find suitable Python packages for the task at hand and use them.
* Recognize when Python is and when it is not a suitable language to use.


## Practice problems

* Install Anaconda Python, run the [provided Jupyter notebook](data/01 - Python introduction.ipynb) within a new conda environment and then export all the installed dependencies into an *environment.yml* file (see [reference](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)). Check the file, remove not needed data (location, library versions, libraries in lower dependency trees), create a new environment based on the exported file and run the notebook again (it should work without the need to install additiona packages manually).
* Check some Python IDEs to have a subjective opinion for some of them.
* Download, explore and run some scripts from [the Keras examples repository](https://github.com/keras-team/keras/tree/master/examples).