# ImportsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**cancelImport**](ImportsApi.md#cancelImport) | **POST** /api/v1/imports/{import_id}/cancel | Cancel Import |
| [**confirmImport**](ImportsApi.md#confirmImport) | **POST** /api/v1/imports/{import_id}/confirm | Confirm Import |
| [**createImport**](ImportsApi.md#createImport) | **POST** /api/v1/imports | Create Import |
| [**getImport**](ImportsApi.md#getImport) | **GET** /api/v1/imports/{import_id} | Get Import |


<a id="cancelImport"></a>
# **cancelImport**
> ImportResponse cancelImport(importId)

Cancel Import

Discard an import without creating anything. Only while it is &#x60;pending&#x60; or &#x60;processing&#x60;.

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
      ImportResponse result = apiInstance.cancelImport(importId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ImportsApi#cancelImport");
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

<a id="confirmImport"></a>
# **confirmImport**
> ImportResponse confirmImport(importId)

Confirm Import

Commit a reviewed import, creating its documents.  Only from &#x60;pending&#x60; — an import already confirmed or cancelled returns &#x60;409&#x60;.

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
      ImportResponse result = apiInstance.confirmImport(importId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ImportsApi#confirmImport");
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

<a id="createImport"></a>
# **createImport**
> ImportResponse createImport(importCreateRequest)

Create Import

Upload rows to be turned into documents, for review first.  Nothing is created yet: the rows are parsed and held so you can check them. &#x60;confirm_import&#x60; commits them, &#x60;cancel_import&#x60; discards them.

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
      ImportResponse result = apiInstance.createImport(importCreateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ImportsApi#createImport");
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

<a id="getImport"></a>
# **getImport**
> ImportResponse getImport(importId)

Get Import

An import&#39;s status and how many rows it holds.

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
      ImportResponse result = apiInstance.getImport(importId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ImportsApi#getImport");
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

