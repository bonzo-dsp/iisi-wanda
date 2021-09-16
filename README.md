# iisi-wanda
萬大電廠 1 &amp; 2號機組發電量、4號機組發電量、霧社水庫入流量

## 事前準備  
* Win 10 ([在 Win 10 上安裝 Ubuntu 20.04 subsystem](https://marcus116.blogspot.com/2019/07/how-to-add-linux-bash-windows-terminal.html))  
  1. 安裝 Windows Subsystem for Linux  
      * 首先使用管理者 admin 權限開啟 powershell  
        ![](https://1.bp.blogspot.com/-A1PK0psTr0U/XTTz8AZGheI/AAAAAAAAHSQ/TyDY4UeH6VcuNYrVZh2SZe6ngoASDiFEQCLcBGAs/s1600/install_WindowsSubsystemforLinux.png)  
      * 接著在 powershell 輸入下列指令  
        ```bash
        Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
        ```
      * 安裝完畢之後會詢問是否要重新啟動電腦，選擇 y 就會進行立即重啟的動作  
        ![](https://1.bp.blogspot.com/-uOVF_cwR47A/XTT0eJI_B8I/AAAAAAAAHSY/owAyRT5OZZwvOJ_wbIJoToyiCYF6_h0GwCLcBGAs/s1600/install_WindowsSubsystemforLinux_restart.png)
  2. 安裝 Ubuntu 20.04  
      * 到 Windows 商店下載 Linux 子系統，在 Microsoft Store 提供多個 Linux 子系統像是 Ubuntu、OpenSUSE、SLES 可以下載，可以在 Store 輸入 Linux 就可以輕易地找到 Ubuntu，下載完畢後可以點選啟用  
        ![](https://1.bp.blogspot.com/-K9W68vomNNY/XTT2isyEqTI/AAAAAAAAHSk/26ZWeyDwlj0UoLTfjMop-ceMbuq3lHh-ACLcBGAs/s1600/installubuntu_store.png)
      * 第一次啟用 ubuntu 會需要一點時間進行初始化設定與安裝，完畢之後會要求你輸入帳號密碼的動作  
        ![](https://1.bp.blogspot.com/-v6zvodZPGmA/XTT3TRIaY2I/AAAAAAAAHSs/v8jUsn9mkOwF7sXQx9njvx4swoB8qzCHACLcBGAs/s1600/installubuntu_store_initial.png)  
  3. 在 Win 10 內啟動 Ubuntu 20.04 的CLI   
      * 在起始目錄列點選 Ubuntu 20.04  
        ![](https://imgur.com/a/2XIY72M)  
* Ubuntu 20.04  
  1. 點選 Menu 按鈕  
     ![](https://vitux.com/wp-content/uploads/word-image-1669.png)  
  2. 點選 terminal  
     ![](https://vitux.com/wp-content/uploads/word-image-1670.png)  
* MAC
  請參照[官方說明](https://support.apple.com/zh-tw/guide/terminal/apd5265185d-f365-44cb-8b09-71a064a42125/mac)  

## API 部署  
以下皆在 linux 的 CLI 底下執行  
1. 安裝 python 3.8.10 
2. 安裝套件  
  `pip install -r requirements.txt`  
4. 啟動 api 服務，預設 port:8100  
  `python api.pyc` 或  `python api.pyc --port 8100` 或  `python api.pyc -p 8100` 
    
## `api.pyc` 可帶參數  
* -h, --help  show this help message and exit  
* -port PPPP  port number for the api service  

## API 說明 &amp; 文件    
API 啟動時會花一些時間喚醒套件，啟動成功會出現以下畫面  
![](https://i.imgur.com/Joj04tv.png)  

在瀏覽器輸入　`http://<host ip>:<host port>/docs` 將出現API說明文件  
![](https://i.imgur.com/Zj8fgXI.png)  

所有的 APIs 皆有輸出/入格式，以及範例說明，請自行參閱  
