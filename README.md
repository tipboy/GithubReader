##代码仓库探索器##
使用OpenAI的GPT-3.5语言模型探索和提问GitHub代码仓库。
输入Git地址，即可分析，原理是先下载下整个项目，然后再将代码提取，生成本地数据库
问答的时候，使用检索增强的方式，先从本地检索TOP_k 相近结果，然后把结果当做参考内容放到gpt中回答用户内容。

##先决条件##
Python 3.10
OpenAI API密钥（设置在环境变量OPENAI_API_KEY中）
export OPENAI_API_KEY="sk-xxxxx"

#使用方法#
将OpenAI API密钥设置为环境变量OPENAI_API_KEY。
pip install -r requirements.txt
运行脚本：app.py
输入要探索的GitHub仓库的URL。
对仓库提出问题。输入 exit() 来退出。


#主要特点#
克隆并索引GitHub仓库的内容。
支持各种文件类型，包括代码、文本和Jupyter Notebook文件。
根据仓库内容生成详细回答用户查询的答案。
使用OpenAI的语言模型来生成回应。
支持与语言模型进行互动对话。
针对每个问题展示最相关的文档。
