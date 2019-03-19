# machine-learning
Content for Udacity's Machine Learning curriculum, which includes projects and their descriptions.

<a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-nd/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License</a>. Please refer to [Udacity Terms of Service](https://www.udacity.com/legal) for further information.


# steps to create a Python3 virtual environment to work with Jupyter Notebook

1. `git clone <repository url>`
2. `cd machine-learning` -- folder created by git clone

3. `python3 -m venv .`   -- create a virtual environment in the current directory.
    // note: there will be additional files/folders created by venv. need to add those to .gitignore later. 

4. `source ./bin/activate`   -- activate the virtual environment.
5. `pip3 install <necessary packages>` for the whichever project you are working on. 
    i did this manually by scanning through .py files and checking and installing each imported modules. you can also create a requirements.txt file with all the dependencies, and do a one time install.
    
    as an example, for boston_housing project, here are the dependencies i installed:
    * sklearn
    * numpy
    * pandas
    * ipython
    * matplotlib
    * jupyter // it's important you install this in the virtual environment, even if you have jupyter in the global environment. 

6. in the virtual environment, run `./bin/jupyter notebook `
    
     NOTE: this is important! DO NOT use the global jupyter command. You will most likely run into module not found errors when running the project notebook (unless you have the dependencies installed globally. But we are trying to avoid referring to global dependencies here). Using the jupyter installed in our virtual environment ensures the jupyter instance looks for dependencies installed in the virtual environment. 

7. update .gitignore. in my case, these are the additional files/folders that got created by either venv or jupyter
<pre>
    # python3 venv
    bin/
    include/
    share/
    etc/
    pyvenv.cfg
    pip-selfcheck.json
</pre>