# EzOcrServer
[![LeTian Space](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://lloydztw.github.io/mysite/)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=c-sharp&logoColor=white)
[![LeTian FB](https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white)](https://www.facebook.com/letian.chang)
[![](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:lloydz.tw@gmail.com)

OCR server written in pytorch

------------------------------------------------------------------

## History
- 25 June 2022 - Version 2.2.1
    - 增加 回報每一個字元參考位置 之功能
    - Revised by [@letian Chang](https://lloydztw.github.io/mysite/).

- 19 June 2022 - Version 1.0.1
    - Created by [@letian Chang](https://lloydztw.github.io/mysite/).

## Install dependencies
### Requirements
- python 3.8
- easyocr
    - torch
    - torchvision>=0.5
    - opencv-python-headless<=4.5.4.60
    - scipy
    - numpy
    - Pillow
    - scikit-image
    - python-bidi
    - PyYAML

- grpcio
- grpcio-tools
- pandas

<br/><br/>

# 如何 【全部重新】 安裝 EzOcrServer
(0) 下載 http://download.jeteazy.com/LeTian/EzOcrAI/install 所有檔案, 至暫存資料夾, <br/>
開啟 windows command line 視窗 (anaconda 專用的) 
依序 鍵入 以下指令:

------------------------------------------------------------------
(1) 移除舊的 anaconda python 3.9 環境,用 command line 執行: <br/>
    (如果是新機安裝, 或目前已經有 python 3.8 名稱為 ocr 的虛擬環境, 可跳過此步驟.)
```
conda deactivate
conda env remove -n ocr
```
------------------------------------------------------------------
(2) 安裝 python 3.8 虛擬環境,<br/> 
    用 command line 執行:
```
"0) create_conda_env_with_python_38.cmd" ocr
```
成功後,手動鍵入:
```    
conda activate ocr
```
------------------------------------------------------------------
(3) 安裝 pytorch,<br/>
    用 command line 執行:
```
"1) pip install pytorch.cmd"
```
------------------------------------------------------------------
(4) 安裝其他必要套件,<br/>
    用 command line 執行:
```
"2) pip install misc.cmd"
```
------------------------------------------------------------------
(5) 安裝 Apple 模型套件,<br/>
    用 command line 執行:
```
pip install EzOcrServer-2.2.1-py3-none-any.whl --force-reinstall
```
或是舊版 (ver 1.0.1)
```
pip install EzOcrServer-1.0.1-py3-none-any.whl --force-reinstall
```
------------------------------------------------------------------
(6) 更新 Apple 訓練後參數檔,<br/>
    複製 model_files 裡面兩個資料夾, 

    model
    user_network

覆蓋到 
    
    C:\users\<使用者名稱>\.EasyOCR

<br/><br/>
# 如何 【更新】 從 1.0.1 升級至 2.2.1
(0) 下載以下檔案至暫存資料夾, <br/>

http://download.jeteazy.com/LeTian/EzOcrAI/upgrade_ver_2.2.1/EzOcrServer-2.2.1-py3-none-any.whl.7z

http://download.jeteazy.com/LeTian/EzOcrAI/upgrade_ver_2.2.1/EzOcrClientDemo_C#.7z

<br/>

------------------------------------------------------------------
(1) 開啟 windows command line 視窗 (anaconda 專用的), 
    鍵入 以下指令:
```
conda activate ocr

pip install EzOcrServer-2.2.1-py3-none-any.whl --force-reinstall
```

(2) 更新 C# dll,
    解開 EzOcrClientDemo_C#.7z 後, 
    請參考以下源碼:

        EzOcrDemoCtrl.cs 
	        DecodeOneImage

<br/><br/>

------------------------------------------------------------------
# Author
**[LeTian Chang](mailto:lloydz.tw@gmail.com)**
<br/>

![](https://scontent.fkhh1-2.fna.fbcdn.net/v/t1.6435-9/94496580_3289259774417998_6021738680945737728_n.jpg?_nc_cat=108&ccb=1-7&_nc_sid=174925&_nc_ohc=58aiZPHed7gAX_6vKw5&_nc_ht=scontent.fkhh1-2.fna&oh=00_AT8By9vZ7G_MIRGxsr_sPpJdVepuxVMk8szf0ts3L1U7Ig&oe=62FD3DAD)    
