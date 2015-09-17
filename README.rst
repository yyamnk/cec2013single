=============================================================
CEC'2013 Single Global Optimization Special Session Benchmark
=============================================================

This package wraps the official C code for the Special Session & Competition on Real-Parameter Single Objective Optimization at
the IEEE Congress on Evolutionary Computation. See http://www.ntu.edu.sg/home/EPNSugan/index_files/CEC2013/CEC2013.htm.

This package is a unofficial package using cython for calling the official implementation in C source code.


original repository is `dmolina/cec2013single <https://github.com/dmolina/cec2013single>`


--------------------------------------------------------------
Setup
--------------------------------------------------------------

::

    git clone git@github.com:yyamnk/cec2013single.git
    cd cec2013single
    python setup.py build_ext --inplace
    # cec2013single/cec2013.c, cec2013single/cec2013.so are generated

--------------------------------------------------------------
Usage
--------------------------------------------------------------

::

    # path/to/cec2013single/cec2013single
    $ ipython

    In [1]: import cec2013 as cec

    In [2]: fobj = cec.Benchmark()

    In [3]: fid = 1 # function id, [1-28]

    In [4]: f = fobj.get_function(fid)

    In [5]: pos = np.random.rand(30) # position vector to be evaluated

    In [6]: f(pos) # get fitness
    Out[6]: 70296.9232630032
