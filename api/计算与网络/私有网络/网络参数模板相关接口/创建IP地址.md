## 1. 接口描述

本接口(CreateAddress)用于创建 IP 地址。
接口请求域名：<font style="color:red">vpc.api.qcloud.com</font>


## 2. 请求参数

以下请求参数列表仅列出了接口请求参数，正式调用时需要加上公共请求参数，见 <a href="/doc/api/372/4153" title="公共请求参数">公共请求参数</a> 页面。其中，此接口的 Action 字段为 CreateAddress

| 参数名称 | 必选 | 类型 | 描述 |
|---------|---------|---------|---------|
| addressName | 是 | String | IP 地址名称 。|
| address | 是 | Array| IP 地址列表。 |
| address.n | 是 | String | IP 地址，支持多种格式，详见 [参数模板产品文档](https://cloud.tencent.com/document/product/215/20090)。|


## 3. 输出参数

| 参数名称 | 类型 | 描述 |
|---------|---------|---------|
| code | Int | 数字错误码, 0 表示成功，其他值表示失败。详见错误码页面的 <a href='https://cloud.tencent.com/document/api/215/4781' title='公共错误码'>公共错误码</a>。|
| message | String | 模块错误信息描述，与接口相关。|
| codeDesc | String | 字符串错误码。 |
| data | Object | 返回信息。 |
| data.addressId | String | IP 地址 ID。| 

## 4. 错误码表
以下错误码表仅列出了该接口的业务逻辑错误码，更多公共错误码详见 <a href="https://cloud.tencent.com/doc/api/245/4781" title="公共错误码">公共错误码</a>。


 <table class="t"><tbody><tr>
<th><b>错误码数值</b></th>
<th><b>原因</b></th>
<tr>
<td> 29257 <td> 后台错误，请求失败。
<tr>
<td> 29258 <td> 引用资源不存在。
<tr>
<td> 29259 <td> 关联对象因规则展开过大拒绝您的关联。
<tr>
<td> 29260 <td> 参数模板总数或成员数使用超限。
<tr>
<td> 29254 <td> 鉴权失败。
<tr>
<td> 9003 <td> 参数错误。
<tr>
<td> 9005 <td> 系统忙或有相关资源正在被编辑。
</tbody></table>

## 5. 示例
输入
<pre>
https://vpc.api.qcloud.com/v2/index.php?Action=CreateAddress
&<<a href="https://cloud.tencent.com/doc/api/229/6976">公共请求参数</a>>
&addressName=CreateAddressTest&address.0=10.0.0.6&address.1=10.0.0.2/16&address.2=10.0.0.1-10.0.0.20
</pre>
输出
```
{
    "code": 0,
    "message": "",
    "codeDesc": "Success",
    "data": {
        "addressId": "ipm-f5n688da"
    }
}
```



 
