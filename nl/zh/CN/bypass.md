---

copyright:
  years: 2017
lastupdated: "2017-10-30"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# 绕过防火墙规则

要绕过防火墙规则，请执行以下过程：

1. 从浏览器，打开[客户门户网站![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/){: new_window}，并登录到帐户。
2. 在“客户门户网站”导航中，转至**网络 > IP 管理> VLAN**，单击要绕过的防火墙设备。
3. 在**设备详细信息**页面中的**配置**选项卡上，可使用**操作**下拉菜单以选择**设置路由旁路**或在**状态：**部分中，可单击**绕过规则**按钮。 

	另一个选项是，路由时绕过防火墙，可通过单击**路由时绕过**按钮执行此操作。不管是哪种方式，都应该会显示确认对话框。单击**是**以确认操作。绕过规则大约需要两分钟时间。在旁路方式中，“状态”应该为“路由绕过防火墙”。

## 再次启用规则

要再次启用规则，请遵循以上指示信息，以到达设备的**配置**选项卡，并单击**操作**下拉菜单，选择**设置路由旁路**。将显示确认对话框。单击**是**以确认操作。“状态”将在两分钟内重新变为“路由通过防火墙”。
