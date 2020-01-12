# Guide to Install TensorFlow

This is a installation guide for Windows (tested only on Windows 10) using pip

1. Get Python 3.4-3.7 **64-bit** only

2. Add to PATH

3. Get pip (comes with Python installation)

4. (Optional)

   ```shell
   pip install virtualenv
   ```

   

5. ```shell
   pip install --upgrade tensorflow
   ```

6. Test with

   ```shell
   python -c "import tensorflow as tf;print(tf.reduce_sum(tf.random.normal([1000, 1000])))"
   ```

   If you get a lot of not located warnings but get

   ```python
   tf.Tensor(-1565.4648, shape=(), dtype=float32)
   ```

   Then it is a success

7. (Optional for Nvidia Graphics cards GT 430 or GTX 465 or 410M or higher;

   See full list @ [link](https://developer.nvidia.com/cuda-gpus))

   - The latest [NVIDIA® GPU drivers](https://www.nvidia.com/drivers)

   - The [CUDA® Toolkit](https://developer.nvidia.com/cuda-toolkit-archive)

   - The [cuDNN SDK](https://developer.nvidia.com/cudnn) (Requires a Nvidia Account)

     

   - Add to PATH the following (**Note**, must be v10.1 as of 1/12/20, otherwise check the documentation in the link [here](https://www.tensorflow.org/install/gpu#windows_setup))

     - C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.1\bin

     - C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.1\extras\CUPTI\libx64

     - C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.1\include

     - Where ever you unziped the cuDNN SDK's **bin directory**. i.e.

       ​	C:\tools\cuda\bin

8. Repeat step 6 but you should see a bunch of successes and 

   ```python
   tf.Tensor(-1565.4648, shape=(), dtype=float32)
   ```

## Issues

Post an Issue to the Issues tab in GitHub

## Other Guides

- unspecific documentation: [TensorFlow](https://www.tensorflow.org/install/pip?lang=python3)