# RendersApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**downloadRenderApiV1RendersRenderIdDownloadGet**](RendersApi.md#downloadRenderApiV1RendersRenderIdDownloadGet) | **GET** /api/v1/renders/{render_id}/download | Download Render |
| [**getRenderApiV1RendersRenderIdGet**](RendersApi.md#getRenderApiV1RendersRenderIdGet) | **GET** /api/v1/renders/{render_id} | Get Render |


<a id="downloadRenderApiV1RendersRenderIdDownloadGet"></a>
# **downloadRenderApiV1RendersRenderIdDownloadGet**
> File downloadRenderApiV1RendersRenderIdDownloadGet(renderId)

Download Render

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.RendersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    RendersApi apiInstance = new RendersApi(defaultClient);
    String renderId = "renderId_example"; // String | 
    try {
      File result = apiInstance.downloadRenderApiV1RendersRenderIdDownloadGet(renderId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RendersApi#downloadRenderApiV1RendersRenderIdDownloadGet");
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
| **renderId** | **String**|  | |

### Return type

[**File**](File.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf, application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | PDF file |  -  |
| **422** | Validation Error |  -  |

<a id="getRenderApiV1RendersRenderIdGet"></a>
# **getRenderApiV1RendersRenderIdGet**
> Map&lt;String, Object&gt; getRenderApiV1RendersRenderIdGet(renderId)

Get Render

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.RendersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    RendersApi apiInstance = new RendersApi(defaultClient);
    String renderId = "renderId_example"; // String | 
    try {
      Map<String, Object> result = apiInstance.getRenderApiV1RendersRenderIdGet(renderId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RendersApi#getRenderApiV1RendersRenderIdGet");
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
| **renderId** | **String**|  | |

### Return type

**Map&lt;String, Object&gt;**

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

