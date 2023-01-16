
## Prestudy
#### Keyword Collection + Primitive Grouping
- TensorFlow Data Structures
	- Tensor : numpy.ndarray
		- EagerTensor : Python
		- RaggedTensor
		- SparseTensor
		- `tf.constant()`
		- `tf.Variable()`
	- String
	- Set
	- Queue
	- Tensor Array
	- Graph
- Keras: High Level API
- `tf.GradientTape()`
-  `tf.function()`
- Accelerated Linear Algebra (XLA)
	-  `@tf.function`
- Autodiff: compute gradients
- AutoGraph
- Tracing
- Mixed Precision, NVIDIA GPUs
- TensorFlow Data
	- TFRecord format
	- Data API
		- shuffle -> preprocess -> prefetch
	- TF Transform
	- TFDS

-   @tf.function decorator work only when eager execution is disabled ? **no, actually tf.function is something to accelerate execution when eager mode is enabled**
-   What is the relationship between @tf.function decorator and eager mode of execution ? **@tf.function will cause tensorflow autograph working and accelerate execution for those operation inside it.**
-   How does TensorFlow switch between eager mode and non-eager mode internally ? **tf.function and AutoGraph work by generating code and tracing it into TensorFlow graphs. So when you call a @tf.function decorated function the first time, tensorflow will first convert it into a graph, then execute it, after that, when you can the function again, it will just execute the graph**

