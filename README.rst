A modified fork of Lasagne
=======
[ 1-11-2017] Add `axis` param to Pool1DLayer, now you can specify along which axis the 1D pooling should be done, which is seldom the trailing dimension.

[ 1-16-2017] Add `consume_less` param to LSTMLayer. Set `consume_less = 'cpu'` combined with `precompute_input=True` equals to Keras LSTM implementation of 'cpu'; `consume_less = 'cpu'` combined with `precompute_input=False` equals to Keras LSTM implementation of 'mem'; `consume_less = 'gpu'` combined with `precompute_input=True` equals to Keras LSTM implementation of 'gpu'.  

[ 1-17-2017] Modify BatchNormLayer: add `mode` param, by which the GPU memory usage can be controlled; change the updating logic of mean and inv_std, replace dimshuffle() with reshape(), which is more GPU memory efficient

[ 1-19-2017] Add `mask` param to TransformerLayer; change all 'int64' type cast to 'int32'
