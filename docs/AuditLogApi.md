# AuditLogApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getAuditEventApiV1AuditEventsAuditEventIdGet**](AuditLogApi.md#getAuditEventApiV1AuditEventsAuditEventIdGet) | **GET** /api/v1/audit-events/{audit_event_id} | Get Audit Event |
| [**listAuditEventsApiV1AuditEventsGet**](AuditLogApi.md#listAuditEventsApiV1AuditEventsGet) | **GET** /api/v1/audit-events | List Audit Events |


<a id="getAuditEventApiV1AuditEventsAuditEventIdGet"></a>
# **getAuditEventApiV1AuditEventsAuditEventIdGet**
> AuditEventResponse getAuditEventApiV1AuditEventsAuditEventIdGet(auditEventId)

Get Audit Event

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.AuditLogApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    AuditLogApi apiInstance = new AuditLogApi(defaultClient);
    String auditEventId = "auditEventId_example"; // String | 
    try {
      AuditEventResponse result = apiInstance.getAuditEventApiV1AuditEventsAuditEventIdGet(auditEventId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AuditLogApi#getAuditEventApiV1AuditEventsAuditEventIdGet");
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
| **auditEventId** | **String**|  | |

### Return type

[**AuditEventResponse**](AuditEventResponse.md)

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

<a id="listAuditEventsApiV1AuditEventsGet"></a>
# **listAuditEventsApiV1AuditEventsGet**
> AuditEventsListResponse listAuditEventsApiV1AuditEventsGet(limit, cursor, action, resourceType, resourceId)

List Audit Events

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.AuditLogApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    AuditLogApi apiInstance = new AuditLogApi(defaultClient);
    Integer limit = 50; // Integer | 
    String cursor = "cursor_example"; // String | 
    String action = "action_example"; // String | 
    String resourceType = "resourceType_example"; // String | 
    String resourceId = "resourceId_example"; // String | 
    try {
      AuditEventsListResponse result = apiInstance.listAuditEventsApiV1AuditEventsGet(limit, cursor, action, resourceType, resourceId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AuditLogApi#listAuditEventsApiV1AuditEventsGet");
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
| **action** | **String**|  | [optional] |
| **resourceType** | **String**|  | [optional] |
| **resourceId** | **String**|  | [optional] |

### Return type

[**AuditEventsListResponse**](AuditEventsListResponse.md)

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

