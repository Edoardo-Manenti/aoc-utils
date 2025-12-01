##########################
Advent Of Code Utils
##########################

Collection of utils based on the [aoc-to-markdown](https://github.com/antonio-ramadas)
project by antonio-ramadas.

***************
🐍 Installation
***************

If you want to install directly from this repository, then install the dependencies and you are good to go:

.. code:: bash

  pip install -r requirements.txt

  python -m aoc-utils -h

or 

.. code:: bash

  pip install -r requirements.txt

  pip install .

  aoc-utils -h


****************
📋 Pre-requisite
****************

To download the personalized input file for the problem the script needs your account's session id. 
One you have logged into the adventofcode webiste you can retrieve you session id value from the Application -> Cookies section of the developer tools.
By default the scripts expects a system variable called SESSION_ID containing the session id value.
For Unix-like systems you can simply create the variable by running this command in the a shell:

.. code:: bash

  export SESSION_ID = "your_session_id_value"


************
📖 Arguments
************

::

  Usage: aoc-utils [-h] [-y <year>] [-d <day>] [-o <output_dir>] [-b <boilerplate_dir>] [-s] [-i]
   -h, --help          Optional parameter to print this message
   -y, --year          Optional parameter to indicate the year of the problem
   -d, --day           Optional parameter to indicate the day of the problem
   -o, --output        Optional parameter to indicate the path of the output (default = ".")
   -b, --boilerplate   Optional parameter to copy a directory/file to the output
   -s, --save          Optional argument to indicate that the markdown should not be printed to stdout, but to a file
   -i, --input         Optional argument to indicate that the input is to be downloaded and saved to a file
  
  Extended description:
  --year, if not given, defaults to the current year if in december; otherwise is the current year
  --day, if not given, defaults to the first day which has not been retrieved (checks for directories named "day-<day>"); if all days have been retrieved, then go drink some hot chocolate and enjoy the rest of the day
  --output is the prefix path where the folder (syntax: "day-<day>") will be created
  --boilerplate is an argument useful to copy the solution boilerplate to help you get started
  --save is only necessary if you want to save directly to a file and --output is not given
  
  Example:
  aoc-utils -y 2018 -d 1 -o my-solution-directory -b my-boilerplate -i

