# parallelized-stemmer
`parallelized-stemmer` aims to show report from the use of thread to improve time performance of stemmer algorithm.
This repository using python version `3.6.4` and `flask` framework in order to try out the service by using exposed api. 
Another dependencies that are used for this project listed on `/requirements.txt`

### stemmer library
based on sastrawi `pip install PySastrawi`

### threading library
- package multiprocessing https://docs.python.org/3.4/library/multiprocessing.html?highlight=process
- dask https://towardsdatascience.com/why-every-data-scientist-should-use-dask-81b2b850e15b

## usage
1. always use virtualenv so this project wont bother your machine
- on mac run `source /bin/activate`
- on windows `\Scripts\activate`

to exit virtualenv just exit the terminal or run `deactivate`

2. `pip install -r requirements.txt` (for first time only)
3. run python `setup.py`

(additional)
update `requirements.txt` using `pip freeze > requirements.txt`

## how it works
![thread-flow](https://user-images.githubusercontent.com/4990180/46242844-a3f6d080-c3f7-11e8-8293-936bf563d0e9.jpeg)

## performance test using `time`
- serial_stemmer#1 processed 87440 words, elapsed time in seconds 172.53443098068237
- serial_stemmer#2 processed 87440 words, elapsed time in seconds 181.88903880119324
- serial_stemmer#3 processed 87440 words, elapsed time in seconds 181.69096302986145

- dask_stemmer#1 processed 87440 words, elapsed time in seconds 
- dask_stemmer#2 processed 87440 words, elapsed time in seconds 
- dask_stemmer#3 processed 87440 words, elapsed time in seconds 

