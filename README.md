# hemi

windows安装步骤

    - 打开命令提示符 (CMD):
        - 按 `Win + R` 打开“运行”窗口，输入 `cmd` 并按回车。
    - 输入以下命令，切换到 X 盘：
        
        ```
        X:
        ```
        
    
    - 使用 `cd` 命令导航到指定路径：
        
        ```
        cd PATH
        ```
        
        输入 `dir` 查看文件夹内文件
        
    
    - 验证配置是否成功:
        
        ```
        popmd.exe --help
        ```
        
    - 生成public key
        
        ```
        keygen.exe -secp256k1 -json 
        -net="testnet" > 
        ```
        
    - 查看public key
        
        ```
        %HOMEDRIVE%%HOMEPATH%\popm-address.json
        ```
        
        该命令打开 `popm-address.json` ，对密钥进行编辑
        
    - 跑挖矿小程序
    
    ```
    set POPM_STATIC_FEE=300
    set POPM_BFG_URL=wss://testnet.rpc.hemi.network/v1/ws/public
    popmd.exe
    ```
