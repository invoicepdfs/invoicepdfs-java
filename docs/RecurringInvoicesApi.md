# RecurringInvoicesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**cancelRecurringInvoice**](RecurringInvoicesApi.md#cancelRecurringInvoice) | **DELETE** /api/v1/recurring-invoices/{recurring_id} | Cancel Recurring Invoice |
| [**createRecurringInvoice**](RecurringInvoicesApi.md#createRecurringInvoice) | **POST** /api/v1/recurring-invoices | Create Recurring Invoice |
| [**getRecurringInvoice**](RecurringInvoicesApi.md#getRecurringInvoice) | **GET** /api/v1/recurring-invoices/{recurring_id} | Get Recurring Invoice |
| [**listGeneratedInvoices**](RecurringInvoicesApi.md#listGeneratedInvoices) | **GET** /api/v1/recurring-invoices/{recurring_id}/invoices | List Generated Invoices |
| [**listRecurringInvoices**](RecurringInvoicesApi.md#listRecurringInvoices) | **GET** /api/v1/recurring-invoices | List Recurring Invoices |
| [**pauseRecurringInvoice**](RecurringInvoicesApi.md#pauseRecurringInvoice) | **POST** /api/v1/recurring-invoices/{recurring_id}/pause | Pause Recurring Invoice |
| [**resumeRecurringInvoice**](RecurringInvoicesApi.md#resumeRecurringInvoice) | **POST** /api/v1/recurring-invoices/{recurring_id}/resume | Resume Recurring Invoice |
| [**updateRecurringInvoice**](RecurringInvoicesApi.md#updateRecurringInvoice) | **PATCH** /api/v1/recurring-invoices/{recurring_id} | Update Recurring Invoice |


<a id="cancelRecurringInvoice"></a>
# **cancelRecurringInvoice**
> RecurringInvoiceResponse cancelRecurringInvoice(recurringId)

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
      RecurringInvoiceResponse result = apiInstance.cancelRecurringInvoice(recurringId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RecurringInvoicesApi#cancelRecurringInvoice");
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

<a id="createRecurringInvoice"></a>
# **createRecurringInvoice**
> RecurringInvoiceResponse createRecurringInvoice(recurringInvoiceCreateRequest)

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
      RecurringInvoiceResponse result = apiInstance.createRecurringInvoice(recurringInvoiceCreateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RecurringInvoicesApi#createRecurringInvoice");
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

<a id="getRecurringInvoice"></a>
# **getRecurringInvoice**
> RecurringInvoiceResponse getRecurringInvoice(recurringId)

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
      RecurringInvoiceResponse result = apiInstance.getRecurringInvoice(recurringId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RecurringInvoicesApi#getRecurringInvoice");
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

<a id="listGeneratedInvoices"></a>
# **listGeneratedInvoices**
> InvoicesListResponse listGeneratedInvoices(recurringId, limit, cursor)

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
      InvoicesListResponse result = apiInstance.listGeneratedInvoices(recurringId, limit, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RecurringInvoicesApi#listGeneratedInvoices");
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

<a id="listRecurringInvoices"></a>
# **listRecurringInvoices**
> RecurringInvoicesListResponse listRecurringInvoices(limit, cursor, status)

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
      RecurringInvoicesListResponse result = apiInstance.listRecurringInvoices(limit, cursor, status);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RecurringInvoicesApi#listRecurringInvoices");
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

<a id="pauseRecurringInvoice"></a>
# **pauseRecurringInvoice**
> RecurringInvoiceResponse pauseRecurringInvoice(recurringId)

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
      RecurringInvoiceResponse result = apiInstance.pauseRecurringInvoice(recurringId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RecurringInvoicesApi#pauseRecurringInvoice");
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

<a id="resumeRecurringInvoice"></a>
# **resumeRecurringInvoice**
> RecurringInvoiceResponse resumeRecurringInvoice(recurringId)

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
      RecurringInvoiceResponse result = apiInstance.resumeRecurringInvoice(recurringId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RecurringInvoicesApi#resumeRecurringInvoice");
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

<a id="updateRecurringInvoice"></a>
# **updateRecurringInvoice**
> RecurringInvoiceResponse updateRecurringInvoice(recurringId, recurringInvoicePatchRequest)

Update Recurring Invoice

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
      RecurringInvoiceResponse result = apiInstance.updateRecurringInvoice(recurringId, recurringInvoicePatchRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RecurringInvoicesApi#updateRecurringInvoice");
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

