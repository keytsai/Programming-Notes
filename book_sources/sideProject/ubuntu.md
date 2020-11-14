# VirtualBox 與 ubuntu 安裝建置

## ubuntu安裝

### 安裝Java

```bash
1. wget https://www.dropbox.com/s/butr4i8gfru3xzs/jdk-8u251-linux-x64.tar.gz?dl=0 -O jdk.tar.gz
2. sudo mkdir -p /usr/lib/jvm
3. sudo tar axvf jdk.tar.gz -C /usr/lib/jvm
4. sudo update-alternatives --install /usr/bin/java java /usr/lib/jvm/jdk1.8.0_251/bin/java 1
5. echo export PATH=$PATH:/usr/lib/jvm/jdk1.8.0_251/bin >> ~/.bashrc
```

| code        | 說明                   |
| ----------- | ---------------------- |
| `wget`      | 下載的指令             |
| `-o <檔名>` | 將檔案重新命名為<檔名> |
| -p          | 創建多層資料夾         |

列出在執行的程式`ps aux | grep java`
終止id為6844的程式`sudo kill -9 6844`

### 安裝Tomcat

[如何在 Ubuntu 20.04 上安装 Tomcat 9](https://www.itcoder.tech/posts/how-to-install-tomcat-9-on-ubuntu-20-04/)

- 要改version改為9.0.39
- vim的`Environment="JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64"`這行最後面改為`jdk1.8.0_251`

```bash
1. sudo useradd -m -U -d /opt/tomcat -s /bin/false tomcat
2. VERSION=9.0.39
3. echo $VERSION
4. wget https://www-eu.apache.org/dist/tomcat/tomcat-9/v${VERSION}/bin/apache-tomcat-${VERSION}.tar.gz -P /tmp
```
