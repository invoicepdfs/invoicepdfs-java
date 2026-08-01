# DocumentsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**calculateDocumentApiV1DocumentsCalculatePost**](DocumentsApi.md#calculateDocumentApiV1DocumentsCalculatePost) | **POST** /api/v1/documents/calculate | Calculate Document |
| [**renderDocumentApiV1DocumentsRenderPost**](DocumentsApi.md#renderDocumentApiV1DocumentsRenderPost) | **POST** /api/v1/documents/render | Render Document |
| [**validateDocumentApiV1DocumentsValidatePost**](DocumentsApi.md#validateDocumentApiV1DocumentsValidatePost) | **POST** /api/v1/documents/validate | Validate Document |


<a id="calculateDocumentApiV1DocumentsCalculatePost"></a>
# **calculateDocumentApiV1DocumentsCalculatePost**
> DocumentCalculateResponse calculateDocumentApiV1DocumentsCalculatePost(documentCalculateRequest)

Calculate Document

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.DocumentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    DocumentsApi apiInstance = new DocumentsApi(defaultClient);
    DocumentCalculateRequest documentCalculateRequest = new DocumentCalculateRequest(); // DocumentCalculateRequest | 
    try {
      DocumentCalculateResponse result = apiInstance.calculateDocumentApiV1DocumentsCalculatePost(documentCalculateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#calculateDocumentApiV1DocumentsCalculatePost");
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
| **documentCalculateRequest** | [**DocumentCalculateRequest**](DocumentCalculateRequest.md)|  | |

### Return type

[**DocumentCalculateResponse**](DocumentCalculateResponse.md)

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

<a id="renderDocumentApiV1DocumentsRenderPost"></a>
# **renderDocumentApiV1DocumentsRenderPost**
> Object renderDocumentApiV1DocumentsRenderPost(documentRenderRequest, idempotencyKey)

Render Document

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.DocumentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    DocumentsApi apiInstance = new DocumentsApi(defaultClient);
    DocumentRenderRequest documentRenderRequest = new DocumentRenderRequest(); // DocumentRenderRequest | 
    String idempotencyKey = "idempotencyKey_example"; // String | 
    try {
      Object result = apiInstance.renderDocumentApiV1DocumentsRenderPost(documentRenderRequest, idempotencyKey);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#renderDocumentApiV1DocumentsRenderPost");
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
| **documentRenderRequest** | [**DocumentRenderRequest**](DocumentRenderRequest.md)|  | |
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

<a id="validateDocumentApiV1DocumentsValidatePost"></a>
# **validateDocumentApiV1DocumentsValidatePost**
> DocumentValidateResponse validateDocumentApiV1DocumentsValidatePost(documentValidateRequest)

Validate Document

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.DocumentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    DocumentsApi apiInstance = new DocumentsApi(defaultClient);
    DocumentValidateRequest documentValidateRequest = new DocumentValidateRequest(); // DocumentValidateRequest | 
    try {
      DocumentValidateResponse result = apiInstance.validateDocumentApiV1DocumentsValidatePost(documentValidateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#validateDocumentApiV1DocumentsValidatePost");
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
| **documentValidateRequest** | [**DocumentValidateRequest**](DocumentValidateRequest.md)|  | |

### Return type

[**DocumentValidateResponse**](DocumentValidateResponse.md)

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

