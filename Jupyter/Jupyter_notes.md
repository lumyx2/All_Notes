# Jupyter Notes

## Jupyter not letting you same - FORBIDDEN Error 
The notebook/lab authentication has become stale. Likely from having it open for too long while not being used. When this error happens you cannot save the notebook. Solution based on this [StackOverflow Answer](https://stackoverflow.com/questions/41532441/jupyter-creating-notebook-failed-forbidden). 

To solve the problem do the following: 

## Steps: 
1. Open the Jupyter notebook/lab in another browser (copy the link). 
    - It will ask you to enter the password (if you set one) or token for the notebook. To get token follow step 2. 
2. Open a terminal in the environment that you use the notebook and type:
    ```
    (base)$ jupyter notebook list
    ```
    The output should be similar to: 
    ```
    Currently running servers:
    http://localhost:8888/?token=cbad1a6ce77ae284725a5e43a7db48f2e9bf3b6458e577bb :: <path to notebook>
    ```



<!-- <a name="head1234"></a>A Heading in this SO entry! -->

