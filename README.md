# Overview,

A simple bash 'common' helper script to source in which helps to improve the readability of scripts. I use this helper quite a bit when tidying up old code I see around the place. 
<hr>
# How it works,

Within your bash script simply source the ./bin/common_bash and then start using the log functions to add some simple colour and improve the readability of your code. 

eg,

```
bash-4.3$ source ./bin/common_bash

cat << my_test.sh >> EOF
log stage 'Starting Here'
if [ 0 == 0 ]; then 
  log failed 'my failed message here'
fi
if [ 0 == 0 ]; then 
  log passed 'my passing message here' 
fi
EOF

bash-4.3$ ./my_test.sh
### [Stage : Starting Here ] ###
[Failed] - my failed message here
[Passed] - my passing message here
```

There's a bit more to read in the common_bash itself, so have a read through in there as well. 
<hr>
# References,

Credit goes to http://www.kfirlavi.com/blog/2012/11/14/defensive-bash-programming/ which started me thinking about getting a little better and something fairly simple