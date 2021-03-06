### WARNING: This is not an API. If you want to do something with the Python libraries installed in the docker image, you need to code it yourself.

```
# Main Libraries

pytesseract (english and portuguese pre-installed)
pdf2image

Pillow
opencv-contrib-python
imutils

matplotlib
numpy
pandas
pyarrow

dvc
```

# How to install the docker image
1. First, make sure that you've installed docker.
2. Then, pull the image from DockerHub.
```
docker pull leommiranda/doc-extraction
```
3. Never trusting people on the internet is a good practice. You can check the image here: https://hub.docker.com/r/leommiranda/doc-extraction

# How to run the sample Jupyter Notebooks

1. Open a terminal and clone the repository.
```
git clone https://github.com/leommiranda/doc-extraction
```
2. Download the dataset from: <https://storage.cloud.google.com/doc-extraction/exploration_data.zip>
3. Open the terminal and type this command. It'll run the docker image as a container on your current directory, which should contain the doc-extraction directory.
```
cd doc-extraction
docker run --rm -p 8888:8888 -e JUPYTER_ENABLE_LAB=yes -v ${PWD}:/current_directory -w /current_directory leommiranda/doc-extraction
```
5. Open one of the 3 server links that will appear in the terminal. I recommend the last one.
6. (☞ﾟヮﾟ)☞

# How to run a Python script

```
docker run --rm -v ${PWD}:/current_dir -w /current_dir leommiranda/doc-extraction python [SCRIPT_NAME].py
```

# How to run multiple Python scripts

```
docker run -it --rm -v ${PWD}:/current_dir -w /current_dir leommiranda/doc-extraction /bin/bash
python [SCRIPT_NAME_1].py
python [SCRIPT_NAME_2].py
(...)
```
