# RendersApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**downloadRender**](RendersApi.md#downloadRender) | **GET** /api/v1/renders/{render_id}/download | Download Render |
| [**getRender**](RendersApi.md#getRender) | **GET** /api/v1/renders/{render_id} | Get Render |


<a id="downloadRender"></a>
# **downloadRender**
> File downloadRender(renderId, token)

Download Render

Fetch the PDF, by signature or by API key.  Two ways in, and the signature is checked *first* — before the row is looked up — so a forged token cannot be used to tell a real render id from an invented one. It also means the token path costs no auth work at all, which matters because this is the one endpoint a browser hits directly.

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
    String token = "token_example"; // String | The signature from this render's `download_url`. Present it and no API key is needed — that is what makes the URL a link. Omit it and the request authenticates normally.
    try {
      File result = apiInstance.downloadRender(renderId, token);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RendersApi#downloadRender");
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
| **token** | **String**| The signature from this render&#39;s &#x60;download_url&#x60;. Present it and no API key is needed — that is what makes the URL a link. Omit it and the request authenticates normally. | [optional] |

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

<a id="getRender"></a>
# **getRender**
> RenderResponse getRender(renderId)

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
      RenderResponse result = apiInstance.getRender(renderId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RendersApi#getRender");
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

[**RenderResponse**](RenderResponse.md)

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

