# Quick Benchmark for Macbook Pro M1 Max 64GB for Tensorflow and PyTorch

## Important notes
1. This is just to give a an idea of performance if you're considering buying the new Mac. I did this primarily due to the lack of such benchmarks at the moment. I hope this helps.
2. Running on TensorFlow Metal (GPU Edition - supporting Mac GPU) and PyTorch (CPU Edition - No Mac GPU support yet). Not a fair comparison, but wanted to see how PyTorch performs in general on the new M1 Max chip.
3. Mac GPU support is still at its very early days. I expect more imporvements in the coming months.

## Summary 
1. Did 2 tests using MNIST dataset and a basic CNN network as you can see from the Jupyter notebooks: 
    * Test1: Running a typical MNIST with regular batch size (i.e., 32)
    * Test2: Running a typical MNIST with much larger batch size (i.e., 4096). This is to simulate training on larger images that need much more memory.
2. As you can see from the table below, TensorFlow is performing very well on the new chip.
3. I really hope PyTorch catch up pretty quick (but [with this in mind](https://github.com/pytorch/pytorch/issues/47702), it doesn't seem to happen soon).. For the time being, I'm switching to TensorFlow ;).

| DL framework | Smaller batch size | Larger batch size |
| :---         |     :---:      |          ---: |
| TensorFlow (Metal)  | 1min 35s     | 22.1 s   |
| PyTorch  (CPU)  | 5min 35s       | 3min 57s      |