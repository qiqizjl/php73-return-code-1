# php verison
php7.3beta0+
php7.3
php7.4

# steps
## install php-ext
~~~ shell
cd php-ext
phpize
./configure
make
make install
~~~
## allow extensions in php.ini
~~~ ini
extension="test.so"
~~~

## recurrent
~~~ shell
php test.php
echo $?
~~~


# result
## Expected
~~~ shell
/work/git # php test.php
/work/git # echo $?
0
~~~

## Actual
~~~ shell
/work/git # php test.php
/work/git # echo $?
1
~~~

