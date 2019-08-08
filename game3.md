## game3 连接UK8S集群

### 初始化工作

1. 初始环境
    1.1 ubuntu 18.04

    1.2 设置sudo不用密码:

    ```
    sudo vi /etc/sudoers
    ```

    1.3 添加`ubuntu  ALL = NOPASSWD: ALL`


### game环节

1. 安装kubectl(已安装):

    1.1 下载对应版本的kubectl客户端
    
    ```
    curl -LO https://storage.googleapis.com/kubernetes-release/release/v1.13.5/bin/linux/amd64/kubectl
    ```
    1.2 赋予文件执行权限
    
    ```
    chmod +x ./kubectl
    ```
    1.3 移动二进制文件到指定目录中
    
    ```
    sudo mv ./kubectl /usr/local/bin/kubectl
    ```
    1.4 验证客户端安装成功
    
    ```
    kubectl version
    ```

2. 连接UK8S集群

    2.1 在console.ucloud.cn中查询创建好的集群。
    ![](images/20190808154142.png)

    2.2 查看集群凭证
    ![](images/kubeconfig.png)

    2.3 复制集群凭证