# callback_tensorboard


TensorBoard basic visualizations




## Description

This callback writes a log for TensorBoard, which allows you to visualize
dynamic graphs of your training and test metrics, as well as activation
histograms for the different layers in your model.





## Usage
```r
callback_tensorboard(
  log_dir = NULL,
  histogram_freq = 0,
  batch_size = NULL,
  write_graph = TRUE,
  write_grads = FALSE,
  write_images = FALSE,
  embeddings_freq = 0,
  embeddings_layer_names = NULL,
  embeddings_metadata = NULL,
  embeddings_data = NULL,
  update_freq = "epoch",
  profile_batch = 0
)
```




## Arguments


Argument      |Description
------------- |----------------
log_dir | The path of the directory where to save the log files to be parsed by Tensorboard. The default is ``NULL``, which will use the active run directory (if available) and otherwise will use "logs".
histogram_freq | frequency (in epochs) at which to compute activation histograms for the layers of the model. If set to 0, histograms won't be computed.
batch_size | size of batch of inputs to feed to the network for histograms computation. No longer needed, ignored since TF 1.14.
write_graph | whether to visualize the graph in Tensorboard. The log file can become quite large when write_graph is set to ``TRUE``
write_grads | whether to visualize gradient histograms in TensorBoard. ``histogram_freq`` must be greater than 0.
write_images | whether to write model weights to visualize as image in Tensorboard.
embeddings_freq | frequency (in epochs) at which selected embedding layers will be saved.
embeddings_layer_names | a list of names of layers to keep eye on. If ``NULL`` or empty list all the embedding layers will be watched.
embeddings_metadata | a named list which maps layer name to a file name in which metadata for this embedding layer is saved. See the https://www.tensorflow.org/tensorboard/tensorboard_projector_plugin#saving_data_for_tensorboarddetails about the metadata file format. In case if the same metadata file is used for all embedding layers, string can be passed.
embeddings_data | Data to be embedded at layers specified in ``embeddings_layer_names``. Array (if the model has a single input) or list of arrays (if the model has multiple inputs). Learn https://www.tensorflow.org/text/guide/word_embeddingsmore about embeddings
update_freq | ``'batch'`` or ``'epoch'`` or integer. When using ``'batch'``, writes the losses and metrics to TensorBoard after each batch. The same applies for ``'epoch'``. If using an integer, let's say ``10000``, the callback will write the metrics and losses to TensorBoard every 10000 samples. Note that writing too frequently to TensorBoard can slow down your training.
profile_batch | Profile the batch to sample compute characteristics. By default, it will disbale profiling. Set profile_batch=2 profile the second batch. Must run in TensorFlow eager mode. (TF >= 1.14)




## Details

TensorBoard is a visualization tool provided with TensorFlow.

You can find more information about TensorBoard
https://www.tensorflow.org/tensorboard/get_startedhere.

When using a backend other than TensorFlow, TensorBoard will still work
(if you have TensorFlow installed), but the only feature available will
be the display of the losses and metrics plots.







## See Also

Other callbacks: 
`callback_csv_logger()`,
`callback_early_stopping()`,
`callback_lambda()`,
`callback_learning_rate_scheduler()`,
`callback_model_checkpoint()`,
`callback_progbar_logger()`,
`callback_reduce_lr_on_plateau()`,
`callback_remote_monitor()`,
`callback_terminate_on_naan()`


