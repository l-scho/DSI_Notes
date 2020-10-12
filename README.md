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

### make a bash function

```bash
function gitadder() {
    git pull
    git add .
    dt=$(date '+%d/%m/%Y %H:%M:%S');
    git commit - m "Auto Updated: $(date '+%a %M:%H %h %d %Y')"
    git push
}
```

------------------------------------------------
## Python

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