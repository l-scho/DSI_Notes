# DSI_Notes
*[Markdown](#markdown)

## Relevant Links
* [Visualizing 'scipy.stats' distributions](https://stackoverflow.com/questions/37559470/what-do-all-the-distributions-available-in-scipy-stats-look-like)

* [MathJax basic tutorial and quick reference](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference)

-----------------------------------------------
## <a name="markdown">Markdown</a>

### Anchors / internal reference links
In standard Markdown, place an anchor <a name="abcd"></a> where you want to link to and refer to it on the same page by [link text](#abcd).

### Images

```
![Stir the pile](https://imgs.xkcd.com/comics/machine_learning.png)
```

![Stir the pile](https://imgs.xkcd.com/comics/machine_learning.png)

------------------------------------------------
## Bash Scirpting

* bash profile location on OSX: '~/.bash_profile'

### Basic Commands
* recursively delete a directory: 'rm -rf <directoryname>

### make a bash function

```bash
function gitadder() {
    git pull
    git add .
    #dt=$(date '+%d/%m/%Y %H:%M:%S');
    git commit - m "Auto Updated: $(date '+%a %M:%H %h %d %Y')"
    git push
}
```

------------------------------------------------
## Python

### Important Links
*[Python Cheat Sheet](https://github.com/GalvanizeDataScience/course-outline/blob/20-10-DS_SEA_SEA20/quick-reference/Python.pdf)

### Comprehensions

```python
[num for num in range(100)]
```

### functions to remember

```python
def factorial(n):
    prod = 1
    for num in range(n+1):
        prod *= num
    return prod
```

### Methods
#### Dictionary Methods
* clear() - Removes all the elements from the dictionary
* copy() - Returns a copy of the dictionary
* fromkeys() - Returns a dictionary with the specified keys and value
* get() - Returns the value of the specified key
* items() - Returns a list containing a tuple for each key value pair
* keys() - Returns a list containing the dictionary's keys
* pop() - Removes the element with the specified key
* popitem() - Removes the last inserted key-value pair
* setdefault() - Returns the value of the specified key. If the key does not exist: insert the key with the specified value
* update() - Uodates the dictionary with the specified key-value pairs
* values() - Returns a list of all the values in the dictionary

-------------------------------------------------
## Machine Learning Workflow

## Cross Validation
```python
#train/test split
```

###k-fold Cross Validation

### Bootstrap

--------------------------------------------------
## Sorting Algorithms

### Bubble Sort

```python
#hand coded algorithm
```

```python
#library-called bubble sort
```

---------------------------------------------------
## 'matplotlib.pyplot' visualizations

### Import Syntax

$$
import matplotlib.pyplot as plt
$$

### Important Links
*[Creating multiple subplot using plt.subplot](https://matplotlib.org/3.1.0/gallery/subplots_axes_and_figures/subplots_demo.html)
*[Intro to pyplot](https://matplotlib.org/tutorials/introductory/pyplot.html)
*[Intro to Matplotlib](https://github.com/GalvanizeDataScience/course-outline/blob/20-10-DS_SEA_SEA20/quick-reference/Matplotlib.pdf)

---------------------------------------------------
## Derivations
* [Link to Jupyter Notebook (http://github....)]()


---------------------------------------------------
## LaTEX
* won't render in GitHub, but will in VSCode

$$
\sum_{x=1}^{25} a_x
$$

____________________________________________________
## Linear Algebra

### Important Links
*[Essence of linear algebra - 3Blue1Brown](https://www.3blue1brown.com/essence-of-linear-algebra-page)
*[Linear Algebra & Numpy](https://github.com/GalvanizeDataScience/course-outline/blob/20-10-DS_SEA_SEA20/notes/reading_material/numpy_reading.md)

____________________________________________________
## Statistics

## Imports
```
from scipy import stats
```


## Hypothesis Testing

Null Hypothesis Significance Testing Procedure¶
* State a scientific yes/no question
* Take a skeptical stance: state a null hypothesis
* State the opposite of your null hypothesis: the alternative hypothesis
* Create a probabilistic model of the situation when the null is true
* Determine how surprised you need to be to reject the null: determine a rejection level alpha
* Collect your data
* Calculate the conditional probability of finding a result equally or more extreme than you actually observed, assuming the null is true: this is your p-value
* Compare the p-value to your stated rejection threshold, reject the null hypothesis if the p-value is smaller than your rejection level alpha

The p-value is the conditional probability of observing a result equally or more extreme than we actually observed, assuming the null hypothesis is true.

The rejection level alpha is the false positive rate under the null. If the null hypothesis is true, it is the probability we could collect data that falsely rejects the null hypothesis.
* We call this a type-1 error

### Statistical Power

Statistical power tells us how often we will falsely adopt negative beliefs.

A false negative is the failure to reject a null hypothesis when it is actually false.
* We call this a type-2 error

False negative rate - The probability of making a false negative error, given that the null hypothesis is false. (denoted by beta)

Statistical Power = 1 - beta

Effect size - the effect size is the magnitude of the effect of the experimental treatment. 

If we assume a specific effect size, then the difference in the average of the data will be normally distributed.

Statistical Power is effected by:
* The rejection level alpha
* The effect size we wish to detect.
* The size of the sample we collect.

### Bayes



____________________________________________________
## Git 

*[Learn Git Branching](https://learngitbranching.js.org/)

_____________________________________________________
## Pandas

*[Pandas & Python: Top 10](http://manishamde.github.io/blog/2013/03/07/pandas-and-python-top-10/)
*[EDA with Pandas](https://nbviewer.jupyter.org/github/cs109/content/blob/master/labs/lab3/lab3full.ipynb)
*[Data Wranging with Pandas](https://nbviewer.jupyter.org/github/cs109/content/blob/master/lec_04_wrangling.ipynb)

_____________________________________________________
## Numpy

*[Linear Algebra & Numpy](https://github.com/GalvanizeDataScience/course-outline/blob/20-10-DS_SEA_SEA20/notes/reading_material/numpy_reading.md)

_____________________________________________________
## Docker

Docker image - a read-only template that contains a set of instructions for creating a container that can run on the Docker platform.
* provides a convenient way to package up applications and preconfigured server environments

Dockerfile - a text-file that defines the environmnet inside the container.
* can pull from parent images
* can specify programs to install
* can define environment variables
* can expose ports
* can run commands

Docker container - contain running applications
* made by running a Docker image

Docker volume - way of consuming and storing data in a container.
* it does not increase the size of the container using it
* it exists outside of the lifecycle of the container
* it can be shared with other containers

Docker Command References:
* docker COMMAND --help             Gets help on COMMAND
* docker info                       View details about your Docker installation
* docker login                      Logs in to Docker Hub so you can pull your own images
* docker build                      Use to make an image from a Dockerfile
* docker run <image>                Pull (if needed) and start a container from an image
* docker image ls                   Show local images
* docker volume ls                  Show local volumes
* docker start <name | id>          Start a pre-existing container
* docker logs <id>                  Return log of container(get token for notebook after starting)
* docker stop <name | id>           Stop a container
* docker container ls               Show running containers
* docker container ls -a            Show running and stopped containers
* docker container rm <name | id>   Removes a container 
* docker exec                       Execute commands on a container that's already running