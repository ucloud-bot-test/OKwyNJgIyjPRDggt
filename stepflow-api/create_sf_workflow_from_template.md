# 导入工作流定义 - CreateSFWorkflowFromTemplate

## 简介

导入工作流定义






## 使用方法

您可以选择以下方式中的任意一种，发起 API 请求：
- 多语言 OpenSDK / [Go](https://github.com/ucloud/ucloud-sdk-go) / [Python](https://github.com/ucloud/ucloud-sdk-python3) /
- [UAPI 浏览器](https://console.ucloud.cn/uapi/detail?id=CreateSFWorkflowFromTemplate)


## 定义

### 公共参数

| 参数名 | 类型 | 描述信息 | 必填 |
|:---|:---|:---|:---|
| **Action**     | string  | 对应的 API 指令名称，当前 API 为 `CreateSFWorkflowFromTemplate`                        | **Yes** |
| **PublicKey**  | string  | 用户公钥，可从 [控制台](https://console.ucloud.cn/uapi/apikey) 获取                                             | **Yes** |
| **Signature**  | string  | 根据公钥及 API 指令生成的用户签名，参见 [签名算法](api/summary/signature.md)  | **Yes** |

### 请求参数

| 参数名 | 类型 | 描述信息 | 必填 |
|:---|:---|:---|:---|
| **Region** | string | 地域。 参见 [地域和可用区列表](api/summary/regionlist) |**Yes**|
| **ProjectId** | string | 项目ID。不填写为默认项目，子帐号必须填写。 请参考[GetProjectList接口](api/summary/get_project_list) |No|
| **Namespace** | string | 需要创建的工作流namespace |**Yes**|
| **WorkflowName** | string | 需要创建的工作流名称 |**Yes**|
| **Workflow** | string | 描述工作流定义的base64字符串 |**Yes**|

### 响应字段

| 字段名 | 类型 | 描述信息 | 必填 |
|:---|:---|:---|:---|
| **RetCode** | int | 返回状态码，为 0 则为成功返回，非 0 为失败 |**Yes**|
| **Action** | string | 操作指令名称 |**Yes**|
| **Message** | string | 返回错误消息，当 `RetCode` 非 0 时提供详细的描述信息 |No|
| **Version** | int | 	<br />创建的工作流版本号 |**Yes**|




## 示例

### 请求示例
    
```
https://api.ucloud.cn/?Action=CreateSFWorkflowFromTemplate
&Region=cn-zj
&ProjectId=pAZhEbkU
&Namespace=fdhoGtKK
&WorkflowName=hKfCxTNZ
&Workflow=bUaIPfzZ
```

### 响应示例
    
```json
{
  "Action": "CreateSFWorkflowFromTemplateResponse",
  "Message": "success",
  "RetCode": 0,
  "Version": 3
}
```





