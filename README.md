**text2vec** is an R package which provides an efficient framework with a concise API for text analysis and natural language processing (NLP). 

Goals which we aimed to achieve as a result of development of `text2vec`:

* **Concise** - expose as few functions as possible
* **Consistent** - expose unified interfaces, no need to explore new interface for each task
* **Flexible** - allow to easily solve complex tasks
* **Fast** - maximize efficiency per single thread, transparently scale to multiple threads on multicore machines
* **Memory efficient** - use streams and iterators, not keep data in RAM if possible

See [API](http://text2vec.org/api.html) section for details.

# Performance

![htop](http://text2vec.org/images/htop.png)

This package is efficient because it is carefully written in C++, which also means that text2vec is memory friendly. Some parts are fully parallelized using OpenMP. 

Other emrassingly parallel tasks (such as vectorization) can use any fork-based parallel backend on UNIX-like machines. They can achieve near-linear scalability with the number of available cores. 

Finally, a streaming API means that  users do not have to load all the data into RAM. 


