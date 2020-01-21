# How to run doc-extraction
1. First, make sure that you've installed docker.
2. Open the terminal and type this command. It'll pull the image from the DockerHub repository and, then, run it as a container. 
```
docker run --rm -p 8888:8888 -e JUPYTER_ENABLE_LAB=yes leommiranda/doc-extraction
```
3. Open one of the 3 server links that will appear in the terminal
4. Then, open a Jupyter Lab terminal and type
```
git clone https://github.com/leommiranda/doc-extraction

gcloud beta auth application-default login
cd doc-extraction
dvc pull
```
5. Or, you may create a new Jupyter Notebook and run
```
!git clone https://github.com/leommiranda/doc-extraction

!gcloud beta auth application-default login
!cd doc-extraction
!dvc pull
```
6. (☞ﾟヮﾟ)☞
