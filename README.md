# Osmosis :: selfie score prediction 

## dataset used : 

-> We use the Selfie dataset hosted by the University of Central Florida for this project. 

-> dataset contains 46,836 selfie images annotated with 36 different attributes divided into several categories

-> Some of the categories are age ,race , Accessories 

![image.png](attachment:image.png)

download link : https://www.crcv.ucf.edu/data/Selfie/Selfie-dataset.tar.gz

ucf page : https://www.crcv.ucf.edu/data/Selfie/

## output 
score/ratitng for the selfie 

## for excel 

from openpyxl import load_workbook

def write_to_sheet(df,sheet):
    file_name = "Keyword_Extractor_Result_Life_20190512140420.xlsx"
    with pd.ExcelWriter(file_name, engine='openpyxl') as writer:
        writer.book = load_workbook(file_name)
        df.to_excel(writer, sheet)
