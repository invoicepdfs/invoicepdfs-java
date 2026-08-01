# ImportsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**cancelImportApiV1ImportsImportIdCancelPost**](ImportsApi.md#cancelImportApiV1ImportsImportIdCancelPost) | **POST** /api/v1/imports/{import_id}/cancel | Cancel Import |
| [**confirmImportApiV1ImportsImportIdConfirmPost**](ImportsApi.md#confirmImportApiV1ImportsImportIdConfirmPost) | **POST** /api/v1/imports/{import_id}/confirm | Confirm Import |
| [**createImportApiV1ImportsPost**](ImportsApi.md#createImportApiV1ImportsPost) | **POST** /api/v1/imports | Create Import |
| [**getImportApiV1ImportsImportIdGet**](ImportsApi.md#getImportApiV1ImportsImportIdGet) | **GET** /api/v1/imports/{import_id} | Get Import |


<a id="cancelImportApiV1ImportsImportIdCancelPost"></a>
# **cancelImportApiV1ImportsImportIdCancelPost**
> ImportResponse cancelImportApiV1ImportsImportIdCancelPost(importId)

Cancel Import

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.ImportsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    ImportsApi apiInstance = new ImportsApi(defaultClient);
    String importId = "importId_example"; // String | 
    try {
      ImportResponse result = apiInstance.cancelImportApiV1ImportsImportIdCancelPost(importId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ImportsApi#cancelImportApiV1ImportsImportIdCancelPost");
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
| **importId** | **String**|  | |

### Return type

[**ImportResponse**](ImportResponse.md)

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

<a id="confirmImportApiV1ImportsImportIdConfirmPost"></a>
# **confirmImportApiV1ImportsImportIdConfirmPost**
> ImportResponse confirmImportApiV1ImportsImportIdConfirmPost(importId)

Confirm Import

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.ImportsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    ImportsApi apiInstance = new ImportsApi(defaultClient);
    String importId = "importId_example"; // String | 
    try {
      ImportResponse result = apiInstance.confirmImportApiV1ImportsImportIdConfirmPost(importId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ImportsApi#confirmImportApiV1ImportsImportIdConfirmPost");
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
| **importId** | **String**|  | |

### Return type

[**ImportResponse**](ImportResponse.md)

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

<a id="createImportApiV1ImportsPost"></a>
# **createImportApiV1ImportsPost**
> ImportResponse createImportApiV1ImportsPost(importCreateRequest)

Create Import

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.ImportsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    ImportsApi apiInstance = new ImportsApi(defaultClient);
    ImportCreateRequest importCreateRequest = new ImportCreateRequest(); // ImportCreateRequest | 
    try {
      ImportResponse result = apiInstance.createImportApiV1ImportsPost(importCreateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ImportsApi#createImportApiV1ImportsPost");
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
| **importCreateRequest** | [**ImportCreateRequest**](ImportCreateRequest.md)|  | |

### Return type

[**ImportResponse**](ImportResponse.md)

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

<a id="getImportApiV1ImportsImportIdGet"></a>
# **getImportApiV1ImportsImportIdGet**
> ImportResponse getImportApiV1ImportsImportIdGet(importId)

Get Import

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.ImportsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    ImportsApi apiInstance = new ImportsApi(defaultClient);
    String importId = "importId_example"; // String | 
    try {
      ImportResponse result = apiInstance.getImportApiV1ImportsImportIdGet(importId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ImportsApi#getImportApiV1ImportsImportIdGet");
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
| **importId** | **String**|  | |

### Return type

[**ImportResponse**](ImportResponse.md)

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

