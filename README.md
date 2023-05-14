# GPU-Accelerated-Matrix-Multiplication


This code compares the performance of matrix(300x300) multiplication on a CPU and GPU. It utilizes the PyCUDA library to accelerate the computation on the GPU. The code measures the running times of both the CPU and GPU implementations and verifies the correctness of the GPU results. The goal is to assess the potential speedup achieved by leveraging GPU parallelism for matrix multiplication tasks.

How to run this code:

You will need a Nvidia GPU to run this code but incase if you dont have nvidia GPU you can use google colab.

Here are the step-by-step instructions to run the code using Google Colab with a GPU:

- Open your web browser and go to Google Colab.
- Click on "New Notebook" to create a new Colab notebook.
- Copy and paste the provided code into a code cell in the Colab notebook.
- To enable the GPU, click on "Runtime" in the menu bar at the top of the Colab interface.
- In the "Runtime" menu, select "Change runtime type."
- In the dialog box that appears, you will see a drop-down menu for "Hardware accelerator." Select "GPU" from the options.
- Click the "Save" button.
- Now you are ready to run the code. Click on the play button located on the left side of the code cell, or you can use the keyboard shortcut Ctrl + Enter.
- Google Colab will provision a virtual machine with a GPU for you to run the code. The code will execute, and you will see the output in the Colab interface.

By following these steps, you can utilize the GPU capabilities offered by Google Colab to run the code, even if you don't have an NVIDIA GPU on your local machine.

Note ! 

Some parts of the code may require additional installations. For example, if the required packages (pycuda, numpy, matplotlib) are not already installed in your pc/laptop or in the Colab environment, you may need to install them using !pip install <package_name> before running the code.Also the code is not optimized yet because In the matmul_cpu function, the matrix multiplication is implemented using nested loops, resulting in a sequential computation. The inner loop performs scalar multiplication and accumulation, which cannot be parallelized effectively. As a result, the CPU performs the calculations sequentially, leading to slower performance compared to the GPU.. In future ill try to make the optimized version of this code and will check the perfomance !

Results:

![download (4)](https://github.com/whiz-coder/GPU-Accelerated-Matrix-Multiplication/assets/73718958/2868a823-36f9-4a0e-ae87-e124e1f34a40)
