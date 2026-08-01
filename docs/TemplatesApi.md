# TemplatesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createTemplateApiV1TemplatesCustomPost**](TemplatesApi.md#createTemplateApiV1TemplatesCustomPost) | **POST** /api/v1/templates/custom | Create Template |
| [**deleteTemplateApiV1TemplatesCustomTemplateIdDelete**](TemplatesApi.md#deleteTemplateApiV1TemplatesCustomTemplateIdDelete) | **DELETE** /api/v1/templates/custom/{template_id} | Delete Template |
| [**duplicateTemplateApiV1TemplatesCustomTemplateIdDuplicatePost**](TemplatesApi.md#duplicateTemplateApiV1TemplatesCustomTemplateIdDuplicatePost) | **POST** /api/v1/templates/custom/{template_id}/duplicate | Duplicate Template |
| [**getBuiltinTemplateApiV1TemplatesBuiltinTemplateIdGet**](TemplatesApi.md#getBuiltinTemplateApiV1TemplatesBuiltinTemplateIdGet) | **GET** /api/v1/templates/builtin/{template_id} | Get Builtin Template |
| [**getCustomTemplateApiV1TemplatesCustomTemplateIdGet**](TemplatesApi.md#getCustomTemplateApiV1TemplatesCustomTemplateIdGet) | **GET** /api/v1/templates/custom/{template_id} | Get Custom Template |
| [**getTemplateApiV1TemplatesTemplateIdGet**](TemplatesApi.md#getTemplateApiV1TemplatesTemplateIdGet) | **GET** /api/v1/templates/{template_id} | Get Template |
| [**listCustomTemplatesApiV1TemplatesCustomGet**](TemplatesApi.md#listCustomTemplatesApiV1TemplatesCustomGet) | **GET** /api/v1/templates/custom | List Custom Templates |
| [**patchTemplateApiV1TemplatesCustomTemplateIdPatch**](TemplatesApi.md#patchTemplateApiV1TemplatesCustomTemplateIdPatch) | **PATCH** /api/v1/templates/custom/{template_id} | Patch Template |
| [**previewTemplateApiV1TemplatesTemplateIdPreviewPost**](TemplatesApi.md#previewTemplateApiV1TemplatesTemplateIdPreviewPost) | **POST** /api/v1/templates/{template_id}/preview | Preview Template |
| [**publishTemplateApiV1TemplatesCustomTemplateIdPublishPost**](TemplatesApi.md#publishTemplateApiV1TemplatesCustomTemplateIdPublishPost) | **POST** /api/v1/templates/custom/{template_id}/publish | Publish Template |
| [**templatesApiV1TemplatesGet**](TemplatesApi.md#templatesApiV1TemplatesGet) | **GET** /api/v1/templates | Templates |


<a id="createTemplateApiV1TemplatesCustomPost"></a>
# **createTemplateApiV1TemplatesCustomPost**
> CustomTemplateResponse createTemplateApiV1TemplatesCustomPost(templateCreateRequest)

Create Template

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.TemplatesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    TemplatesApi apiInstance = new TemplatesApi(defaultClient);
    TemplateCreateRequest templateCreateRequest = new TemplateCreateRequest(); // TemplateCreateRequest | 
    try {
      CustomTemplateResponse result = apiInstance.createTemplateApiV1TemplatesCustomPost(templateCreateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplatesApi#createTemplateApiV1TemplatesCustomPost");
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
| **templateCreateRequest** | [**TemplateCreateRequest**](TemplateCreateRequest.md)|  | |

### Return type

[**CustomTemplateResponse**](CustomTemplateResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="deleteTemplateApiV1TemplatesCustomTemplateIdDelete"></a>
# **deleteTemplateApiV1TemplatesCustomTemplateIdDelete**
> deleteTemplateApiV1TemplatesCustomTemplateIdDelete(templateId)

Delete Template

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.TemplatesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    TemplatesApi apiInstance = new TemplatesApi(defaultClient);
    String templateId = "templateId_example"; // String | 
    try {
      apiInstance.deleteTemplateApiV1TemplatesCustomTemplateIdDelete(templateId);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplatesApi#deleteTemplateApiV1TemplatesCustomTemplateIdDelete");
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

null (empty response body)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="duplicateTemplateApiV1TemplatesCustomTemplateIdDuplicatePost"></a>
# **duplicateTemplateApiV1TemplatesCustomTemplateIdDuplicatePost**
> CustomTemplateResponse duplicateTemplateApiV1TemplatesCustomTemplateIdDuplicatePost(templateId)

Duplicate Template

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.TemplatesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    TemplatesApi apiInstance = new TemplatesApi(defaultClient);
    String templateId = "templateId_example"; // String | 
    try {
      CustomTemplateResponse result = apiInstance.duplicateTemplateApiV1TemplatesCustomTemplateIdDuplicatePost(templateId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplatesApi#duplicateTemplateApiV1TemplatesCustomTemplateIdDuplicatePost");
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

[**CustomTemplateResponse**](CustomTemplateResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="getBuiltinTemplateApiV1TemplatesBuiltinTemplateIdGet"></a>
# **getBuiltinTemplateApiV1TemplatesBuiltinTemplateIdGet**
> TemplateDetailResponse getBuiltinTemplateApiV1TemplatesBuiltinTemplateIdGet(templateId)

Get Builtin Template

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.TemplatesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    TemplatesApi apiInstance = new TemplatesApi(defaultClient);
    String templateId = "templateId_example"; // String | 
    try {
      TemplateDetailResponse result = apiInstance.getBuiltinTemplateApiV1TemplatesBuiltinTemplateIdGet(templateId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplatesApi#getBuiltinTemplateApiV1TemplatesBuiltinTemplateIdGet");
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

[**TemplateDetailResponse**](TemplateDetailResponse.md)

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

<a id="getCustomTemplateApiV1TemplatesCustomTemplateIdGet"></a>
# **getCustomTemplateApiV1TemplatesCustomTemplateIdGet**
> CustomTemplateResponse getCustomTemplateApiV1TemplatesCustomTemplateIdGet(templateId)

Get Custom Template

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.TemplatesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    TemplatesApi apiInstance = new TemplatesApi(defaultClient);
    String templateId = "templateId_example"; // String | 
    try {
      CustomTemplateResponse result = apiInstance.getCustomTemplateApiV1TemplatesCustomTemplateIdGet(templateId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplatesApi#getCustomTemplateApiV1TemplatesCustomTemplateIdGet");
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

[**CustomTemplateResponse**](CustomTemplateResponse.md)

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

<a id="getTemplateApiV1TemplatesTemplateIdGet"></a>
# **getTemplateApiV1TemplatesTemplateIdGet**
> TemplateDetailResponse getTemplateApiV1TemplatesTemplateIdGet(templateId)

Get Template

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.TemplatesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    TemplatesApi apiInstance = new TemplatesApi(defaultClient);
    String templateId = "templateId_example"; // String | 
    try {
      TemplateDetailResponse result = apiInstance.getTemplateApiV1TemplatesTemplateIdGet(templateId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplatesApi#getTemplateApiV1TemplatesTemplateIdGet");
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

[**TemplateDetailResponse**](TemplateDetailResponse.md)

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

<a id="listCustomTemplatesApiV1TemplatesCustomGet"></a>
# **listCustomTemplatesApiV1TemplatesCustomGet**
> CustomTemplatesListResponse listCustomTemplatesApiV1TemplatesCustomGet(limit, cursor)

List Custom Templates

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.TemplatesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    TemplatesApi apiInstance = new TemplatesApi(defaultClient);
    Integer limit = 50; // Integer | 
    String cursor = "cursor_example"; // String | 
    try {
      CustomTemplatesListResponse result = apiInstance.listCustomTemplatesApiV1TemplatesCustomGet(limit, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplatesApi#listCustomTemplatesApiV1TemplatesCustomGet");
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
| **limit** | **Integer**|  | [optional] [default to 50] |
| **cursor** | **String**|  | [optional] |

### Return type

[**CustomTemplatesListResponse**](CustomTemplatesListResponse.md)

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

<a id="patchTemplateApiV1TemplatesCustomTemplateIdPatch"></a>
# **patchTemplateApiV1TemplatesCustomTemplateIdPatch**
> CustomTemplateResponse patchTemplateApiV1TemplatesCustomTemplateIdPatch(templateId, templatePatchRequest)

Patch Template

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.TemplatesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    TemplatesApi apiInstance = new TemplatesApi(defaultClient);
    String templateId = "templateId_example"; // String | 
    TemplatePatchRequest templatePatchRequest = new TemplatePatchRequest(); // TemplatePatchRequest | 
    try {
      CustomTemplateResponse result = apiInstance.patchTemplateApiV1TemplatesCustomTemplateIdPatch(templateId, templatePatchRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplatesApi#patchTemplateApiV1TemplatesCustomTemplateIdPatch");
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
| **templatePatchRequest** | [**TemplatePatchRequest**](TemplatePatchRequest.md)|  | |

### Return type

[**CustomTemplateResponse**](CustomTemplateResponse.md)

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

<a id="previewTemplateApiV1TemplatesTemplateIdPreviewPost"></a>
# **previewTemplateApiV1TemplatesTemplateIdPreviewPost**
> Object previewTemplateApiV1TemplatesTemplateIdPreviewPost(templateId, appSchemasV1DocumentRenderRequest, idempotencyKey)

Preview Template

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.TemplatesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    TemplatesApi apiInstance = new TemplatesApi(defaultClient);
    String templateId = "templateId_example"; // String | 
    AppSchemasV1DocumentRenderRequest appSchemasV1DocumentRenderRequest = new AppSchemasV1DocumentRenderRequest(); // AppSchemasV1DocumentRenderRequest | 
    String idempotencyKey = "idempotencyKey_example"; // String | 
    try {
      Object result = apiInstance.previewTemplateApiV1TemplatesTemplateIdPreviewPost(templateId, appSchemasV1DocumentRenderRequest, idempotencyKey);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplatesApi#previewTemplateApiV1TemplatesTemplateIdPreviewPost");
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
| **appSchemasV1DocumentRenderRequest** | [**AppSchemasV1DocumentRenderRequest**](AppSchemasV1DocumentRenderRequest.md)|  | |
| **idempotencyKey** | **String**|  | [optional] |

### Return type

**Object**

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

<a id="publishTemplateApiV1TemplatesCustomTemplateIdPublishPost"></a>
# **publishTemplateApiV1TemplatesCustomTemplateIdPublishPost**
> CustomTemplateResponse publishTemplateApiV1TemplatesCustomTemplateIdPublishPost(templateId)

Publish Template

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.TemplatesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    TemplatesApi apiInstance = new TemplatesApi(defaultClient);
    String templateId = "templateId_example"; // String | 
    try {
      CustomTemplateResponse result = apiInstance.publishTemplateApiV1TemplatesCustomTemplateIdPublishPost(templateId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplatesApi#publishTemplateApiV1TemplatesCustomTemplateIdPublishPost");
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

[**CustomTemplateResponse**](CustomTemplateResponse.md)

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

<a id="templatesApiV1TemplatesGet"></a>
# **templatesApiV1TemplatesGet**
> TemplatesListResponse templatesApiV1TemplatesGet()

Templates

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.TemplatesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    TemplatesApi apiInstance = new TemplatesApi(defaultClient);
    try {
      TemplatesListResponse result = apiInstance.templatesApiV1TemplatesGet();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TemplatesApi#templatesApiV1TemplatesGet");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**TemplatesListResponse**](TemplatesListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

