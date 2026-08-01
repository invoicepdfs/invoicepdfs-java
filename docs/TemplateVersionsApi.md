# TemplateVersionsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createTemplateVersionApiV1TemplatesTemplateIdVersionsPost**](TemplateVersionsApi.md#createTemplateVersionApiV1TemplatesTemplateIdVersionsPost) | **POST** /api/v1/templates/{template_id}/versions | Create Template Version |
| [**getTemplateVersionApiV1TemplatesTemplateIdVersionsVersionGet**](TemplateVersionsApi.md#getTemplateVersionApiV1TemplatesTemplateIdVersionsVersionGet) | **GET** /api/v1/templates/{template_id}/versions/{version} | Get Template Version |
| [**listTemplateVersionsApiV1TemplatesTemplateIdVersionsGet**](TemplateVersionsApi.md#listTemplateVersionsApiV1TemplatesTemplateIdVersionsGet) | **GET** /api/v1/templates/{template_id}/versions | List Template Versions |


<a id="createTemplateVersionApiV1TemplatesTemplateIdVersionsPost"></a>
# **createTemplateVersionApiV1TemplatesTemplateIdVersionsPost**
> TemplateVersionResponse createTemplateVersionApiV1TemplatesTemplateIdVersionsPost(templateId, templateVersionCreateRequest)

Create Template Version

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.TemplateVersionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    TemplateVersionsApi apiInstance = new TemplateVersionsApi(defaultClient);
    String templateId = "templateId_example"; // String | 
    TemplateVersionCreateRequest templateVersionCreateRequest = new TemplateVersionCreateRequest(); // TemplateVersionCreateRequest | 
    try {
      TemplateVersionResponse result = apiInstance.createTemplateVersionApiV1TemplatesTemplateIdVersionsPost(templateId, templateVersionCreateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplateVersionsApi#createTemplateVersionApiV1TemplatesTemplateIdVersionsPost");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **templateId** | **String**|  | |
| **templateVersionCreateRequest** | [**TemplateVersionCreateRequest**](TemplateVersionCreateRequest.md)|  | |

### Return type

[**TemplateVersionResponse**](TemplateVersionResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="getTemplateVersionApiV1TemplatesTemplateIdVersionsVersionGet"></a>
# **getTemplateVersionApiV1TemplatesTemplateIdVersionsVersionGet**
> TemplateVersionResponse getTemplateVersionApiV1TemplatesTemplateIdVersionsVersionGet(templateId, version)

Get Template Version

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.TemplateVersionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    TemplateVersionsApi apiInstance = new TemplateVersionsApi(defaultClient);
    String templateId = "templateId_example"; // String | 
    Integer version = 56; // Integer | 
    try {
      TemplateVersionResponse result = apiInstance.getTemplateVersionApiV1TemplatesTemplateIdVersionsVersionGet(templateId, version);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplateVersionsApi#getTemplateVersionApiV1TemplatesTemplateIdVersionsVersionGet");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **templateId** | **String**|  | |
| **version** | **Integer**|  | |

### Return type

[**TemplateVersionResponse**](TemplateVersionResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="listTemplateVersionsApiV1TemplatesTemplateIdVersionsGet"></a>
# **listTemplateVersionsApiV1TemplatesTemplateIdVersionsGet**
> TemplateVersionsListResponse listTemplateVersionsApiV1TemplatesTemplateIdVersionsGet(templateId)

List Template Versions

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.TemplateVersionsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    TemplateVersionsApi apiInstance = new TemplateVersionsApi(defaultClient);
    String templateId = "templateId_example"; // String | 
    try {
      TemplateVersionsListResponse result = apiInstance.listTemplateVersionsApiV1TemplatesTemplateIdVersionsGet(templateId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplateVersionsApi#listTemplateVersionsApiV1TemplatesTemplateIdVersionsGet");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **templateId** | **String**|  | |

### Return type

[**TemplateVersionsListResponse**](TemplateVersionsListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

