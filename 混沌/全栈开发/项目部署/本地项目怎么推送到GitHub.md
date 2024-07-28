[toc]

## 一、本地初始化链接GitHub仓库



> 按照以下步骤进行操作。这些步骤包括创建一个新的GitHub仓库、在本地配置Git、初始化Git仓库、添加远程仓库地址并推送代码。

### 步骤一：在GitHub上创建一个新的仓库

1. 登录到你的GitHub账户。
2. 点击右上角的“+”按钮，然后选择“New repository”。
3. 输入仓库名称（例如：`my-new-repo`），填写描述（可选）。
4. 选择“Public”或“Private”。
5. 点击“Create repository”按钮。

### 步骤二：在本地初始化Git仓库

1. 打开终端，导航到你的项目目录。
    ```bash
    cd /path/to/your/project
    ```

2. 初始化Git仓库：
    ```bash
    git init
    ```

3. 添加所有文件到暂存区：
    ```bash
    git add .
    ```

4. 提交文件：
    ```bash
    git commit -m "Initial commit"
    ```

### 步骤三：将本地仓库连接到GitHub仓库

1. 在GitHub仓库创建页面上，你会看到类似以下的提示信息：
    ```bash
    git remote add origin https://github.com/your-username/my-new-repo.git
    git branch -M main
    git push -u origin main
    ```

2. 在本地终端中，执行以下命令来添加远程仓库地址（将URL替换为你的仓库URL）：
    ```bash
    git remote add origin https://github.com/your-username/my-new-repo.git
    ```

3. 设置主分支名称为 `main`：
    ```bash
    git branch -M main
    ```

4. 推送代码到远程仓库：
    ```bash
    git push -u origin main
    ```

### 步骤四：验证推送结果

1. 打开你的GitHub仓库页面，刷新页面。
2. 你应该可以看到刚刚推送的代码文件。

### 完整示例

假设你的项目目录为 `/Users/username/my-project`，GitHub用户名为 `your-username`，仓库名为 `my-new-repo`。

1. 在GitHub上创建一个名为 `my-new-repo` 的仓库。

2. 在终端中运行以下命令：

    ```bash
    cd /Users/username/my-project
    git init
    git add .
    git commit -m "Initial commit"
    git remote add origin https://github.com/your-username/my-new-repo.git
    git branch -M main
    git push -u origin main
    ```

完成以上步骤后，你的本地项目就成功推送到GitHub仓库了。如果在任何一步遇到问题，请告诉我，我会进一步帮助你。



## 二、GitHub创建仓库

> 常规的GitHub创建流程，操作一遍即可。

![image-20240603170728481](https://typora-xubang.oss-cn-hangzhou.aliyuncs.com/2024_xubang/image-20240603170728481.png?AI_make_money=VX_AI19858122061)

> 本地使用常规命令，进行上传。

![image-20240603170840736](https://typora-xubang.oss-cn-hangzhou.aliyuncs.com/2024_xubang/image-20240603170840736.png?AI_make_money=VX_AI19858122061)

> 权限问题解决。

![image-20240603170924922](https://typora-xubang.oss-cn-hangzhou.aliyuncs.com/2024_xubang/image-20240603170924922.png?AI_make_money=VX_AI19858122061)

> 这个问题和403都属于权限问题，都可以直接通过下方的流程来解决权限问题。

### 步骤一：确认仓库权限

1. 确认你是否拥有该仓库的写权限。你可以在GitHub上打开仓库主页，检查你的权限。

### 步骤二：检查和生成Token

1. 确保你的Token具有足够的权限。你需要的权限至少包括 `repo`。
2. 登录到GitHub，进入 `Settings` -> `Developer settings` -> `Personal access tokens`。
3. 检查你之前生成的Token是否具有足够的权限，如果没有，请生成一个新的Token，确保勾选 `repo` 相关权限。

### 步骤三：重新配置Git凭证

1. 清除已有的Git凭证缓存（如果有）：
    ```bash
    git credential-cache exit
    ```

2. 删除当前的凭证（可以在 macOS 中通过访问“钥匙串访问”应用来删除相关条目）：
    ```bash
    git credential-osxkeychain erase
    ```

### 步骤四：重新尝试Push操作

1. 在终端中执行以下命令以确保你使用正确的凭证：
    ```bash
    git push
    ```

2. 当提示输入用户名和密码时，使用你的GitHub用户名 `zxxxxffsxxo7148` 和新生成的Token。

### 示例详细步骤

1. 清除现有凭证：
    ```bash
    git credential-cache exit
    git credential-osxkeychain erase
    ```

2. 重新生成GitHub Token，并确保包含 `repo` 权限。

3. 重新尝试Push操作：
    ```bash
    git push
    ```

    输入用户名 `zxxxxffsxxo7148` 和新生成的Token作为密码。

