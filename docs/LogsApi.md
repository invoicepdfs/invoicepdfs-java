# LogsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**listLogsApiV1LogsGet**](LogsApi.md#listLogsApiV1LogsGet) | **GET** /api/v1/logs | List Logs |


<a id="listLogsApiV1LogsGet"></a>
# **listLogsApiV1LogsGet**
> ApiRequestLogsListResponse listLogsApiV1LogsGet(status, limit)

List Logs

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.LogsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    LogsApi apiInstance = new LogsApi(defaultClient);
    String status = ""; // String | 
    Integer limit = 100; // Integer | 
    try {
      ApiRequestLogsListResponse result = apiInstance.listLogsApiV1LogsGet(status, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LogsApi#listLogsApiV1LogsGet");
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
| **status** | **String**|  | [optional] [default to ] |
| **limit** | **Integer**|  | [optional] [default to 100] |

### Return type

[**ApiRequestLogsListResponse**](ApiRequestLogsListResponse.md)

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

