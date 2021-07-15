---
lab:
    title: '运行试验'
---
# 运行试验

试验是数据科学家工作的核心。在 Azure 机器学习中，*试验*用于运行脚本或管道，通常会生成输出并记录指标。在本练习中，你将使用 Azure 机器学习 SDK 以试验的形式来运行 Python 代码。

## 准备工作

如果尚未完成 *[创建 Azure 机器学习工作区](01-create-a-workspace.md)* 练习以创建 Azure 机器学习工作区和计算实例，请完成它，并克隆本练习所需的笔记本。

## 打开 Jupyter

虽然可以使用 Azure 机器学习工作室中的 **“笔记本”** 页面来运行笔记本，但使用功能齐全的笔记本开发环境（如 *Jupyter*） 通常效率更高。好在 Azure 机器学习计算实例包括 Jupyter 的安装。

> **提示**： Jupyter Notebook 是用于数据科学的常用开放源代码工具。如果不熟悉它，请参阅[本文档](https://jupyter-notebook.readthedocs.io/en/stable/notebook.html)。

1. 在 [Azure 机器学习工作室](https://ml.azure.com)中，查看工作区的 **“计算”** 页面，并在 **“计算实例”** 选项卡上启动计算实例（如果尚未运行）。
2. 当计算实例正在运行时，单击 **Jupyter** 链接以在新的浏览器选项卡中打开 Jupyter 主页。务必打开 *Jupyter* 而不是 *JupyterLab*。

## 验证是否安装了 Azure 机器学习 SDK

默认情况下，Azure 机器学习 SDK 已安装在计算实例上。请按照以下步骤来验证安装。

1. 在 Jupyter Notebook 环境中，创建一个新的 **“终端”**。这将打开一个带有命令外壳的新选项卡。
2. 输入以下命令来确认 Azure ML SDK 已安装：

    ```bash
    pip show azureml-sdk
    ```

    请注意已安装的 SDK 包的版本。

3. **azureml-sdk SDK** 包提供了与 Azure 机器学习一起使用所需的最重要的库。但是，有些其他包包含主 SDK 包中不包含的其他有用库。使用以下命令来验证是否还安装了 **azureml-widgets** 包，此包包含用于在笔记本中显示 Azure 机器学习信息的库：

    ```bash
    pip show azureml-widgets
    ```

4. 关闭 **“终端”** 选项卡，然后返回到包含 Jupyter 主页的选项卡。

> **详细信息**： 有关安装 Azure ML SDK 机器可选组件的更多详细信息，请参阅 [Azure ML SDK 文档](https://docs.microsoft.com/python/api/overview/azure/ml/install?view=azure-ml-py)。

## 在笔记本中运行试验

Azure 机器学习中的试验需要从某种*控制*层（通常是脚本或程序）启动。在本练习中，你将使用笔记本来控制试验。

1. 在 Jupyter 主页中，浏览到克隆的笔记本存储库所在的 **/users/*your-user-name*/mslearn-dp100** 文件夹，然后打开 **“运行试验”** 笔记本。
2. 然后阅读笔记本中的笔记，依次运行每个代码单元。
3. 笔记本中的代码运行完毕后，在 **“文件”** 菜单上单击 **“关闭并停止”** 以关闭它及其 Python 内核。然后关闭所有 Jupyter 浏览器选项卡。

## 清理

如果你现在完成了 Azure 机器学习的工作，请在 Azure 机器学习工作室的 **“计算”** 页上的 **“计算实例”** 选项卡上，选择你的计算实例，然后单击 **“停止”** 以将其关闭。否则，让它继续运行以便你在下一个实验室中使用。

> **备注**： 停止计算可确保你的订阅不会为计算资源付费。但是，只要订阅中存在 Azure 机器学习工作区，就需要为数据存储支付少量费用。如果已完成对 Azure 机器学习的探索，可以删除 Azure 机器学习工作区和相关资源。但是，如果计划完成本系列中的任何其他实验室，则需要先重复 *[创建 Azure 机器学习工作区](01-create-a-workspace.md)* 练习来创建工作区并准备环境。
