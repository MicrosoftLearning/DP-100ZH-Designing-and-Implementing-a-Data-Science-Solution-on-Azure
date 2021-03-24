---
title: 在线托管说明
permalink: index.html
layout: home
---

# Azure 机器学习练习

此存储库包含针对 Microsoft 课程 [DP-100 *在 Azure 上设计和实现数据科学解决方案*](https://docs.microsoft.com/learn/certifications/courses/dp-100t01)的动手实验室练习以及等效的 [Microsoft Learn 上的自定进度模块](https://docs.microsoft.com/learn/paths/build-ai-solutions-with-azure-ml-service/)。这些练习配合教材提供，你可以使用其描述的方法进行练习。

若要完成这些练习，需要一个 Microsoft Azure 订阅。如果导师没有为你提供订阅，可以在 [https://azure.microsoft.com](https://azure.microsoft.com) 注册以获取免费试用版。

{% assign labs = site.pages | where_exp:"page", "page.url contains '/Instructions'" %}
| 练习 |
| ------- | 
{% for activity in labs  %}| [{{ activity.lab.title }}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}
