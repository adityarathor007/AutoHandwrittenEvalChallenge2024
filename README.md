
# AutoEval Summer Challenge

The aim of this project is to streamline the evaluation process of True/False answer sheets by OCR and automated image processing.






## Run Locally

Clone the project

```bash
git clone https://github.com/adityarathor007/AutoHandwrittenEvalChallenge2024.git
```

Go to **code_notebook.py** and follow these steps to start the setup and install the necessary libraries:


    
  **For DOCTR:** 

- in this repo their is a folder named <doctr> in which all neccessary files are there for this project

-  Make sure you have installed Tensorflow and PyTorch >= 1.12.0 . in your environment

- You can refer the following repo for more info: [Doctr](https://github.com/mindee/doctr)



**For PaddleOCR:**

```bash
pip install Cmake ta-lib wheel setuptools --upgrade
```

```bash
pip install paddleocr paddlepaddle 
```
Refer to the following repo for more info: [PaddlePaddle](https://github.com/PaddlePaddle/PaddleOCR/blob/main/doc/doc_ch/quickstart.md)


Install the **libraries** required by doctr:

```bash
pip install defusedxml tqdm anyascii shapely Pillow pypdfium2 tf2onnx pyclipper rapidfuzz langdetect huggingface_hub scipy opencv-python opencv-contrib-python opencv-python-headless 
```

Once the setup is done in the **specify directories** section:
-  add the parent folder and the image folder


```bash
# Define the path to the folder containing images(eg: parent_folder='mytest_V2')

parent_folder=<folder name>


# Image folder name (# eg: image_folder = f'{parent_folder}/Sample_Data')

image_folder = f'{parent_folder}/<folder name>'

```

- Add the name of the csv file in which the marks along image name will be written

```bash
# path of csv where the output will be written(eg: {parent_folder}/csvs/pred.csv')

pred_csv_path=f'{parent_folder}/<csv_file>'
```

- Specify the Path of the Answer Key(csv) where answer to each question will be provided

``` bash
#Answer Key for the question paper(eg: f'{parent_folder}/ModelAnswer.csv')

actual_ans_csv_path=f'{parent_folder}/<csv_file>'

```


- For Evalution to calculate MAE(in the evaluation section):

``` bash
#specify the path where actual marks to image files are given
actual_df=pd.read_csv(f'{parent_folder}/<csv_file>')
```

