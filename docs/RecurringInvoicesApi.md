# RecurringInvoicesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**cancelRecurringInvoiceApiV1RecurringInvoicesRecurringIdDelete**](RecurringInvoicesApi.md#cancelRecurringInvoiceApiV1RecurringInvoicesRecurringIdDelete) | **DELETE** /api/v1/recurring-invoices/{recurring_id} | Cancel Recurring Invoice |
| [**createRecurringInvoiceApiV1RecurringInvoicesPost**](RecurringInvoicesApi.md#createRecurringInvoiceApiV1RecurringInvoicesPost) | **POST** /api/v1/recurring-invoices | Create Recurring Invoice |
| [**getRecurringInvoiceApiV1RecurringInvoicesRecurringIdGet**](RecurringInvoicesApi.md#getRecurringInvoiceApiV1RecurringInvoicesRecurringIdGet) | **GET** /api/v1/recurring-invoices/{recurring_id} | Get Recurring Invoice |
| [**listGeneratedInvoicesApiV1RecurringInvoicesRecurringIdInvoicesGet**](RecurringInvoicesApi.md#listGeneratedInvoicesApiV1RecurringInvoicesRecurringIdInvoicesGet) | **GET** /api/v1/recurring-invoices/{recurring_id}/invoices | List Generated Invoices |
| [**listRecurringInvoicesApiV1RecurringInvoicesGet**](RecurringInvoicesApi.md#listRecurringInvoicesApiV1RecurringInvoicesGet) | **GET** /api/v1/recurring-invoices | List Recurring Invoices |
| [**patchRecurringInvoiceApiV1RecurringInvoicesRecurringIdPatch**](RecurringInvoicesApi.md#patchRecurringInvoiceApiV1RecurringInvoicesRecurringIdPatch) | **PATCH** /api/v1/recurring-invoices/{recurring_id} | Patch Recurring Invoice |
| [**pauseRecurringInvoiceApiV1RecurringInvoicesRecurringIdPausePost**](RecurringInvoicesApi.md#pauseRecurringInvoiceApiV1RecurringInvoicesRecurringIdPausePost) | **POST** /api/v1/recurring-invoices/{recurring_id}/pause | Pause Recurring Invoice |
| [**resumeRecurringInvoiceApiV1RecurringInvoicesRecurringIdResumePost**](RecurringInvoicesApi.md#resumeRecurringInvoiceApiV1RecurringInvoicesRecurringIdResumePost) | **POST** /api/v1/recurring-invoices/{recurring_id}/resume | Resume Recurring Invoice |


<a id="cancelRecurringInvoiceApiV1RecurringInvoicesRecurringIdDelete"></a>
# **cancelRecurringInvoiceApiV1RecurringInvoicesRecurringIdDelete**
> RecurringInvoiceResponse cancelRecurringInvoiceApiV1RecurringInvoicesRecurringIdDelete(recurringId)

Cancel Recurring Invoice

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.RecurringInvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    RecurringInvoicesApi apiInstance = new RecurringInvoicesApi(defaultClient);
    String recurringId = "recurringId_example"; // String | 
    try {
      RecurringInvoiceResponse result = apiInstance.cancelRecurringInvoiceApiV1RecurringInvoicesRecurringIdDelete(recurringId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RecurringInvoicesApi#cancelRecurringInvoiceApiV1RecurringInvoicesRecurringIdDelete");
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
| **recurringId** | **String**|  | |

### Return type

[**RecurringInvoiceResponse**](RecurringInvoiceResponse.md)

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

<a id="createRecurringInvoiceApiV1RecurringInvoicesPost"></a>
# **createRecurringInvoiceApiV1RecurringInvoicesPost**
> RecurringInvoiceResponse createRecurringInvoiceApiV1RecurringInvoicesPost(recurringInvoiceCreateRequest)

Create Recurring Invoice

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.RecurringInvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    RecurringInvoicesApi apiInstance = new RecurringInvoicesApi(defaultClient);
    RecurringInvoiceCreateRequest recurringInvoiceCreateRequest = new RecurringInvoiceCreateRequest(); // RecurringInvoiceCreateRequest | 
    try {
      RecurringInvoiceResponse result = apiInstance.createRecurringInvoiceApiV1RecurringInvoicesPost(recurringInvoiceCreateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RecurringInvoicesApi#createRecurringInvoiceApiV1RecurringInvoicesPost");
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
| **recurringInvoiceCreateRequest** | [**RecurringInvoiceCreateRequest**](RecurringInvoiceCreateRequest.md)|  | |

### Return type

[**RecurringInvoiceResponse**](RecurringInvoiceResponse.md)

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

<a id="getRecurringInvoiceApiV1RecurringInvoicesRecurringIdGet"></a>
# **getRecurringInvoiceApiV1RecurringInvoicesRecurringIdGet**
> RecurringInvoiceResponse getRecurringInvoiceApiV1RecurringInvoicesRecurringIdGet(recurringId)

Get Recurring Invoice

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.RecurringInvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    RecurringInvoicesApi apiInstance = new RecurringInvoicesApi(defaultClient);
    String recurringId = "recurringId_example"; // String | 
    try {
      RecurringInvoiceResponse result = apiInstance.getRecurringInvoiceApiV1RecurringInvoicesRecurringIdGet(recurringId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RecurringInvoicesApi#getRecurringInvoiceApiV1RecurringInvoicesRecurringIdGet");
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
| **recurringId** | **String**|  | |

### Return type

[**RecurringInvoiceResponse**](RecurringInvoiceResponse.md)

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

<a id="listGeneratedInvoicesApiV1RecurringInvoicesRecurringIdInvoicesGet"></a>
# **listGeneratedInvoicesApiV1RecurringInvoicesRecurringIdInvoicesGet**
> InvoicesListResponse listGeneratedInvoicesApiV1RecurringInvoicesRecurringIdInvoicesGet(recurringId, limit, cursor)

List Generated Invoices

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.RecurringInvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    RecurringInvoicesApi apiInstance = new RecurringInvoicesApi(defaultClient);
    String recurringId = "recurringId_example"; // String | 
    Integer limit = 50; // Integer | 
    String cursor = "cursor_example"; // String | 
    try {
      InvoicesListResponse result = apiInstance.listGeneratedInvoicesApiV1RecurringInvoicesRecurringIdInvoicesGet(recurringId, limit, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RecurringInvoicesApi#listGeneratedInvoicesApiV1RecurringInvoicesRecurringIdInvoicesGet");
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
| **recurringId** | **String**|  | |
| **limit** | **Integer**|  | [optional] [default to 50] |
| **cursor** | **String**|  | [optional] |

### Return type

[**InvoicesListResponse**](InvoicesListResponse.md)

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

<a id="listRecurringInvoicesApiV1RecurringInvoicesGet"></a>
# **listRecurringInvoicesApiV1RecurringInvoicesGet**
> RecurringInvoicesListResponse listRecurringInvoicesApiV1RecurringInvoicesGet(limit, cursor, status)

List Recurring Invoices

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.RecurringInvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    RecurringInvoicesApi apiInstance = new RecurringInvoicesApi(defaultClient);
    Integer limit = 50; // Integer | 
    String cursor = "cursor_example"; // String | 
    String status = "status_example"; // String | 
    try {
      RecurringInvoicesListResponse result = apiInstance.listRecurringInvoicesApiV1RecurringInvoicesGet(limit, cursor, status);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RecurringInvoicesApi#listRecurringInvoicesApiV1RecurringInvoicesGet");
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
| **status** | **String**|  | [optional] |

### Return type

[**RecurringInvoicesListResponse**](RecurringInvoicesListResponse.md)

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

<a id="patchRecurringInvoiceApiV1RecurringInvoicesRecurringIdPatch"></a>
# **patchRecurringInvoiceApiV1RecurringInvoicesRecurringIdPatch**
> RecurringInvoiceResponse patchRecurringInvoiceApiV1RecurringInvoicesRecurringIdPatch(recurringId, recurringInvoicePatchRequest)

Patch Recurring Invoice

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.RecurringInvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    RecurringInvoicesApi apiInstance = new RecurringInvoicesApi(defaultClient);
    String recurringId = "recurringId_example"; // String | 
    RecurringInvoicePatchRequest recurringInvoicePatchRequest = new RecurringInvoicePatchRequest(); // RecurringInvoicePatchRequest | 
    try {
      RecurringInvoiceResponse result = apiInstance.patchRecurringInvoiceApiV1RecurringInvoicesRecurringIdPatch(recurringId, recurringInvoicePatchRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RecurringInvoicesApi#patchRecurringInvoiceApiV1RecurringInvoicesRecurringIdPatch");
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
| **recurringId** | **String**|  | |
| **recurringInvoicePatchRequest** | [**RecurringInvoicePatchRequest**](RecurringInvoicePatchRequest.md)|  | |

### Return type

[**RecurringInvoiceResponse**](RecurringInvoiceResponse.md)

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

<a id="pauseRecurringInvoiceApiV1RecurringInvoicesRecurringIdPausePost"></a>
# **pauseRecurringInvoiceApiV1RecurringInvoicesRecurringIdPausePost**
> RecurringInvoiceResponse pauseRecurringInvoiceApiV1RecurringInvoicesRecurringIdPausePost(recurringId)

Pause Recurring Invoice

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.RecurringInvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    RecurringInvoicesApi apiInstance = new RecurringInvoicesApi(defaultClient);
    String recurringId = "recurringId_example"; // String | 
    try {
      RecurringInvoiceResponse result = apiInstance.pauseRecurringInvoiceApiV1RecurringInvoicesRecurringIdPausePost(recurringId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RecurringInvoicesApi#pauseRecurringInvoiceApiV1RecurringInvoicesRecurringIdPausePost");
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
| **recurringId** | **String**|  | |

### Return type

[**RecurringInvoiceResponse**](RecurringInvoiceResponse.md)

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

<a id="resumeRecurringInvoiceApiV1RecurringInvoicesRecurringIdResumePost"></a>
# **resumeRecurringInvoiceApiV1RecurringInvoicesRecurringIdResumePost**
> RecurringInvoiceResponse resumeRecurringInvoiceApiV1RecurringInvoicesRecurringIdResumePost(recurringId)

Resume Recurring Invoice

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.RecurringInvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    RecurringInvoicesApi apiInstance = new RecurringInvoicesApi(defaultClient);
    String recurringId = "recurringId_example"; // String | 
    try {
      RecurringInvoiceResponse result = apiInstance.resumeRecurringInvoiceApiV1RecurringInvoicesRecurringIdResumePost(recurringId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RecurringInvoicesApi#resumeRecurringInvoiceApiV1RecurringInvoicesRecurringIdResumePost");
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
| **recurringId** | **String**|  | |

### Return type

[**RecurringInvoiceResponse**](RecurringInvoiceResponse.md)

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

