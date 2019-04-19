# Make chocolate
BE534 HW-14-open, by Chunan Liu, chunanliu@email.arizona.edu

Write a python program called make_chocolate.py.

Given 3 positional arguments: the numbers of small bars (1 kilo each), big bars (5 kilos each), and goal kilos of chocolate, return the number of small bars to use if the goal chocolate can be done, assuming we always use big bars before small bars. Otherwise, print out "The goal chocolate cannot be done".

# Expected behabior

```
$ ./make_chocolate.py -h
usage: make_chocolate.py [-h] int int int

Make Chocolate

positional arguments:
  int         the number of small bars
  int         the number of big bars
  int         the number of goal kilos

optional arguments:
  -h, --help  show this help message and exit
```

```
$ ./make_chocolate.py 4 1 9
4
```

```
./make_chocolate.py 6 2 10
0
```

```
$ ./make_chocolate.py 4 1 10
The goal chocolate cannot be done
```

```
$ ./make_chocolate.py 1 2 7
The goal chocolate cannot be done
```

# Test Suite

A passing test suite looks like this:

```
$ make test
python3 -m pytest -v test.py
============================================================= test session starts =============================================================
platform darwin -- Python 3.7.1, pytest-4.0.2, py-1.7.0, pluggy-0.8.0 -- /anaconda3/bin/python3
cachedir: .pytest_cache
rootdir: /Users/chunanliu/Desktop/BE 534/work/biosys-analytics/assignments/14-open, inifile:
plugins: remotedata-0.3.1, openfiles-0.3.1, doctestplus-0.2.0, arraydiff-0.3
collected 2 items                                                                                                                             

test.py::test_usage PASSED                                                                                                              [ 50%]
test.py::test_runs PASSED                                                                                                               [100%]

========================================================== 2 passed in 0.38 seconds ===========================================================
```
