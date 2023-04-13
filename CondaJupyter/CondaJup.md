# Conda Notes

## How to use different `Conda Environments` per Jupyter Notebook
I've found that there is a lot of partial info around this. However, I found a really good guide in this [post](https://towardsdatascience.com/get-your-conda-environment-to-show-in-jupyter-notebooks-the-easy-way-17010b76e874). The point of this post it to keep the essential and hopefully survive if that link dies. 

### Steps:

1. Install `conda` in whatever way works for you. 
3. Intall whatever packages you will use in your base environment
4. In you **base** environment:
    ```
    (base)$ conda install nb_conda_kernels
    ```
    This will allow to pick the kernel you want out of a list inside Jupyter.
3. **[OPTIONAL]** Create your new environment (Example with `sklearn`):
     
    ```
    (base)$ conda create -n sklearn-env -c conda-forge scikit-learn
    (base)$ conda activate sklearn-env
    ```
    or, create an empty one by

    ```
    (base)$ conda create --name new-env
    (base)$ conda activate new-env
    ```

4. Install whatever packages you need in the new environment
5. Install `ipykernel` to the **new** environment
    If you created a new environment:
    ```
    (new-env)$ conda install ipykernel
    ```
    If using the `sklearn-env` environment
    ```
    (sklearn-env)$ conda install ipykernel
    ```
6. Start `Jupyter` as usual and switch the Kernel inside the notebook you want by going:
    ```
    Kernel->Change Kernel->Python[conda sklearn-env]
    ```


<!-- ## Next solution -->


