
# FAQs

### Uninstall stand-alone Anonconda

If you have an installed Anaconda from the official website, you need to hide it before setting up PyTorch.

#### login to Palmetto Cluster.

#### Make a copy of your `.bashrc` and `.conda/environments.txt` files in case something goes wrong. 

```
cp ~/.bashrc ~/bashrc.bak
cp ~/.conda/environments.txt ~/.conda/environments.bak
```

### Open `.bashrc` and delete conda statements

Move down until you locate the following lines:

```
# >>> conda initialize >>>
<some scripting here>
# <<< conda initialize <<<
```

Erase all the lines between ```>>>conda initialize >>>``` and ```<<<conda initialize <<<```. 

### Delete `.conda/environments.txt` 

~~~
rm -rf .conda/environments.txt
~~~

### Log out of Palmetto and login again. 


## Reset modulized Anaconda

All environments installed by modulized Anaconda are stored in `.conda/envs`.
The environment index is stored in `./conda/environments.txt`.
If you no longer need them, simply delete `.conda`.