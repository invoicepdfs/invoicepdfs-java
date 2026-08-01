# InvoicesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**archiveInvoiceApiV1InvoicesInvoiceIdArchivePost**](InvoicesApi.md#archiveInvoiceApiV1InvoicesInvoiceIdArchivePost) | **POST** /api/v1/invoices/{invoice_id}/archive | Archive Invoice |
| [**calculateInvoiceApiV1InvoicesCalculatePost**](InvoicesApi.md#calculateInvoiceApiV1InvoicesCalculatePost) | **POST** /api/v1/invoices/calculate | Calculate Invoice |
| [**createInvoiceApiV1InvoicesPost**](InvoicesApi.md#createInvoiceApiV1InvoicesPost) | **POST** /api/v1/invoices | Create Invoice |
| [**deleteInvoiceApiV1InvoicesInvoiceIdDelete**](InvoicesApi.md#deleteInvoiceApiV1InvoicesInvoiceIdDelete) | **DELETE** /api/v1/invoices/{invoice_id} | Delete Invoice |
| [**duplicateInvoiceApiV1InvoicesInvoiceIdDuplicatePost**](InvoicesApi.md#duplicateInvoiceApiV1InvoicesInvoiceIdDuplicatePost) | **POST** /api/v1/invoices/{invoice_id}/duplicate | Duplicate Invoice |
| [**finalizeInvoiceApiV1InvoicesInvoiceIdFinalizePost**](InvoicesApi.md#finalizeInvoiceApiV1InvoicesInvoiceIdFinalizePost) | **POST** /api/v1/invoices/{invoice_id}/finalize | Finalize Invoice |
| [**getInvoiceApiV1InvoicesInvoiceIdGet**](InvoicesApi.md#getInvoiceApiV1InvoicesInvoiceIdGet) | **GET** /api/v1/invoices/{invoice_id} | Get Invoice |
| [**listInvoiceDeliveriesApiV1InvoicesInvoiceIdDeliveriesGet**](InvoicesApi.md#listInvoiceDeliveriesApiV1InvoicesInvoiceIdDeliveriesGet) | **GET** /api/v1/invoices/{invoice_id}/deliveries | List Invoice Deliveries |
| [**listInvoicesApiV1InvoicesGet**](InvoicesApi.md#listInvoicesApiV1InvoicesGet) | **GET** /api/v1/invoices | List Invoices |
| [**markPaidApiV1InvoicesInvoiceIdMarkPaidPost**](InvoicesApi.md#markPaidApiV1InvoicesInvoiceIdMarkPaidPost) | **POST** /api/v1/invoices/{invoice_id}/mark-paid | Mark Paid |
| [**markSentApiV1InvoicesInvoiceIdMarkSentPost**](InvoicesApi.md#markSentApiV1InvoicesInvoiceIdMarkSentPost) | **POST** /api/v1/invoices/{invoice_id}/mark-sent | Mark Sent |
| [**markUnpaidApiV1InvoicesInvoiceIdMarkUnpaidPost**](InvoicesApi.md#markUnpaidApiV1InvoicesInvoiceIdMarkUnpaidPost) | **POST** /api/v1/invoices/{invoice_id}/mark-unpaid | Mark Unpaid |
| [**patchInvoiceApiV1InvoicesInvoiceIdPatch**](InvoicesApi.md#patchInvoiceApiV1InvoicesInvoiceIdPatch) | **PATCH** /api/v1/invoices/{invoice_id} | Patch Invoice |
| [**previewInvoiceApiV1InvoicesPreviewPost**](InvoicesApi.md#previewInvoiceApiV1InvoicesPreviewPost) | **POST** /api/v1/invoices/preview | Preview Invoice |
| [**renderInvoiceApiV1InvoicesInvoiceIdRendersPost**](InvoicesApi.md#renderInvoiceApiV1InvoicesInvoiceIdRendersPost) | **POST** /api/v1/invoices/{invoice_id}/renders | Render Invoice |
| [**replaceInvoiceApiV1InvoicesInvoiceIdPut**](InvoicesApi.md#replaceInvoiceApiV1InvoicesInvoiceIdPut) | **PUT** /api/v1/invoices/{invoice_id} | Replace Invoice |
| [**restoreInvoiceApiV1InvoicesInvoiceIdRestorePost**](InvoicesApi.md#restoreInvoiceApiV1InvoicesInvoiceIdRestorePost) | **POST** /api/v1/invoices/{invoice_id}/restore | Restore Invoice |
| [**sendInvoiceApiV1InvoicesInvoiceIdSendPost**](InvoicesApi.md#sendInvoiceApiV1InvoicesInvoiceIdSendPost) | **POST** /api/v1/invoices/{invoice_id}/send | Send Invoice |
| [**validateInvoiceApiV1InvoicesValidatePost**](InvoicesApi.md#validateInvoiceApiV1InvoicesValidatePost) | **POST** /api/v1/invoices/validate | Validate Invoice |
| [**voidInvoiceApiV1InvoicesInvoiceIdVoidPost**](InvoicesApi.md#voidInvoiceApiV1InvoicesInvoiceIdVoidPost) | **POST** /api/v1/invoices/{invoice_id}/void | Void Invoice |


<a id="archiveInvoiceApiV1InvoicesInvoiceIdArchivePost"></a>
# **archiveInvoiceApiV1InvoicesInvoiceIdArchivePost**
> InvoiceResponse archiveInvoiceApiV1InvoicesInvoiceIdArchivePost(invoiceId)

Archive Invoice

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.InvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    InvoicesApi apiInstance = new InvoicesApi(defaultClient);
    String invoiceId = "invoiceId_example"; // String | 
    try {
      InvoiceResponse result = apiInstance.archiveInvoiceApiV1InvoicesInvoiceIdArchivePost(invoiceId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoicesApi#archiveInvoiceApiV1InvoicesInvoiceIdArchivePost");
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
| **invoiceId** | **String**|  | |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

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

<a id="calculateInvoiceApiV1InvoicesCalculatePost"></a>
# **calculateInvoiceApiV1InvoicesCalculatePost**
> Map&lt;String, Object&gt; calculateInvoiceApiV1InvoicesCalculatePost(invoiceDraftRequest)

Calculate Invoice

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.InvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    InvoicesApi apiInstance = new InvoicesApi(defaultClient);
    InvoiceDraftRequest invoiceDraftRequest = new InvoiceDraftRequest(); // InvoiceDraftRequest | 
    try {
      Map<String, Object> result = apiInstance.calculateInvoiceApiV1InvoicesCalculatePost(invoiceDraftRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoicesApi#calculateInvoiceApiV1InvoicesCalculatePost");
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
| **invoiceDraftRequest** | [**InvoiceDraftRequest**](InvoiceDraftRequest.md)|  | |

### Return type

**Map&lt;String, Object&gt;**

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

<a id="createInvoiceApiV1InvoicesPost"></a>
# **createInvoiceApiV1InvoicesPost**
> InvoiceResponse createInvoiceApiV1InvoicesPost(invoiceCreateRequest, idempotencyKey)

Create Invoice

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.InvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    InvoicesApi apiInstance = new InvoicesApi(defaultClient);
    InvoiceCreateRequest invoiceCreateRequest = new InvoiceCreateRequest(); // InvoiceCreateRequest | 
    String idempotencyKey = "idempotencyKey_example"; // String | 
    try {
      InvoiceResponse result = apiInstance.createInvoiceApiV1InvoicesPost(invoiceCreateRequest, idempotencyKey);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoicesApi#createInvoiceApiV1InvoicesPost");
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
| **invoiceCreateRequest** | [**InvoiceCreateRequest**](InvoiceCreateRequest.md)|  | |
| **idempotencyKey** | **String**|  | [optional] |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

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

<a id="deleteInvoiceApiV1InvoicesInvoiceIdDelete"></a>
# **deleteInvoiceApiV1InvoicesInvoiceIdDelete**
> SimpleBoolResponse deleteInvoiceApiV1InvoicesInvoiceIdDelete(invoiceId)

Delete Invoice

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.InvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    InvoicesApi apiInstance = new InvoicesApi(defaultClient);
    String invoiceId = "invoiceId_example"; // String | 
    try {
      SimpleBoolResponse result = apiInstance.deleteInvoiceApiV1InvoicesInvoiceIdDelete(invoiceId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoicesApi#deleteInvoiceApiV1InvoicesInvoiceIdDelete");
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
| **invoiceId** | **String**|  | |

### Return type

[**SimpleBoolResponse**](SimpleBoolResponse.md)

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

<a id="duplicateInvoiceApiV1InvoicesInvoiceIdDuplicatePost"></a>
# **duplicateInvoiceApiV1InvoicesInvoiceIdDuplicatePost**
> InvoiceResponse duplicateInvoiceApiV1InvoicesInvoiceIdDuplicatePost(invoiceId)

Duplicate Invoice

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.InvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    InvoicesApi apiInstance = new InvoicesApi(defaultClient);
    String invoiceId = "invoiceId_example"; // String | 
    try {
      InvoiceResponse result = apiInstance.duplicateInvoiceApiV1InvoicesInvoiceIdDuplicatePost(invoiceId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoicesApi#duplicateInvoiceApiV1InvoicesInvoiceIdDuplicatePost");
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
| **invoiceId** | **String**|  | |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

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

<a id="finalizeInvoiceApiV1InvoicesInvoiceIdFinalizePost"></a>
# **finalizeInvoiceApiV1InvoicesInvoiceIdFinalizePost**
> Map&lt;String, Object&gt; finalizeInvoiceApiV1InvoicesInvoiceIdFinalizePost(invoiceId, idempotencyKey)

Finalize Invoice

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.InvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    InvoicesApi apiInstance = new InvoicesApi(defaultClient);
    String invoiceId = "invoiceId_example"; // String | 
    String idempotencyKey = "idempotencyKey_example"; // String | 
    try {
      Map<String, Object> result = apiInstance.finalizeInvoiceApiV1InvoicesInvoiceIdFinalizePost(invoiceId, idempotencyKey);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoicesApi#finalizeInvoiceApiV1InvoicesInvoiceIdFinalizePost");
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
| **invoiceId** | **String**|  | |
| **idempotencyKey** | **String**|  | [optional] |

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

<a id="getInvoiceApiV1InvoicesInvoiceIdGet"></a>
# **getInvoiceApiV1InvoicesInvoiceIdGet**
> InvoiceResponse getInvoiceApiV1InvoicesInvoiceIdGet(invoiceId)

Get Invoice

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.InvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    InvoicesApi apiInstance = new InvoicesApi(defaultClient);
    String invoiceId = "invoiceId_example"; // String | 
    try {
      InvoiceResponse result = apiInstance.getInvoiceApiV1InvoicesInvoiceIdGet(invoiceId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoicesApi#getInvoiceApiV1InvoicesInvoiceIdGet");
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
| **invoiceId** | **String**|  | |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

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

<a id="listInvoiceDeliveriesApiV1InvoicesInvoiceIdDeliveriesGet"></a>
# **listInvoiceDeliveriesApiV1InvoicesInvoiceIdDeliveriesGet**
> DeliveriesListResponse listInvoiceDeliveriesApiV1InvoicesInvoiceIdDeliveriesGet(invoiceId, limit, cursor)

List Invoice Deliveries

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.InvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    InvoicesApi apiInstance = new InvoicesApi(defaultClient);
    String invoiceId = "invoiceId_example"; // String | 
    Integer limit = 50; // Integer | 
    String cursor = "cursor_example"; // String | 
    try {
      DeliveriesListResponse result = apiInstance.listInvoiceDeliveriesApiV1InvoicesInvoiceIdDeliveriesGet(invoiceId, limit, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoicesApi#listInvoiceDeliveriesApiV1InvoicesInvoiceIdDeliveriesGet");
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
| **invoiceId** | **String**|  | |
| **limit** | **Integer**|  | [optional] [default to 50] |
| **cursor** | **String**|  | [optional] |

### Return type

[**DeliveriesListResponse**](DeliveriesListResponse.md)

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

<a id="listInvoicesApiV1InvoicesGet"></a>
# **listInvoicesApiV1InvoicesGet**
> InvoicesListResponse listInvoicesApiV1InvoicesGet(limit, cursor, status)

List Invoices

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.InvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    InvoicesApi apiInstance = new InvoicesApi(defaultClient);
    Integer limit = 50; // Integer | 
    String cursor = "cursor_example"; // String | 
    String status = "status_example"; // String | 
    try {
      InvoicesListResponse result = apiInstance.listInvoicesApiV1InvoicesGet(limit, cursor, status);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoicesApi#listInvoicesApiV1InvoicesGet");
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

<a id="markPaidApiV1InvoicesInvoiceIdMarkPaidPost"></a>
# **markPaidApiV1InvoicesInvoiceIdMarkPaidPost**
> InvoiceResponse markPaidApiV1InvoicesInvoiceIdMarkPaidPost(invoiceId)

Mark Paid

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.InvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    InvoicesApi apiInstance = new InvoicesApi(defaultClient);
    String invoiceId = "invoiceId_example"; // String | 
    try {
      InvoiceResponse result = apiInstance.markPaidApiV1InvoicesInvoiceIdMarkPaidPost(invoiceId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoicesApi#markPaidApiV1InvoicesInvoiceIdMarkPaidPost");
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
| **invoiceId** | **String**|  | |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

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

<a id="markSentApiV1InvoicesInvoiceIdMarkSentPost"></a>
# **markSentApiV1InvoicesInvoiceIdMarkSentPost**
> InvoiceResponse markSentApiV1InvoicesInvoiceIdMarkSentPost(invoiceId)

Mark Sent

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.InvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    InvoicesApi apiInstance = new InvoicesApi(defaultClient);
    String invoiceId = "invoiceId_example"; // String | 
    try {
      InvoiceResponse result = apiInstance.markSentApiV1InvoicesInvoiceIdMarkSentPost(invoiceId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoicesApi#markSentApiV1InvoicesInvoiceIdMarkSentPost");
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
| **invoiceId** | **String**|  | |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

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

<a id="markUnpaidApiV1InvoicesInvoiceIdMarkUnpaidPost"></a>
# **markUnpaidApiV1InvoicesInvoiceIdMarkUnpaidPost**
> InvoiceResponse markUnpaidApiV1InvoicesInvoiceIdMarkUnpaidPost(invoiceId)

Mark Unpaid

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.InvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    InvoicesApi apiInstance = new InvoicesApi(defaultClient);
    String invoiceId = "invoiceId_example"; // String | 
    try {
      InvoiceResponse result = apiInstance.markUnpaidApiV1InvoicesInvoiceIdMarkUnpaidPost(invoiceId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoicesApi#markUnpaidApiV1InvoicesInvoiceIdMarkUnpaidPost");
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
| **invoiceId** | **String**|  | |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

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

<a id="patchInvoiceApiV1InvoicesInvoiceIdPatch"></a>
# **patchInvoiceApiV1InvoicesInvoiceIdPatch**
> InvoiceResponse patchInvoiceApiV1InvoicesInvoiceIdPatch(invoiceId, invoicePatchRequest, idempotencyKey)

Patch Invoice

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.InvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    InvoicesApi apiInstance = new InvoicesApi(defaultClient);
    String invoiceId = "invoiceId_example"; // String | 
    InvoicePatchRequest invoicePatchRequest = new InvoicePatchRequest(); // InvoicePatchRequest | 
    String idempotencyKey = "idempotencyKey_example"; // String | 
    try {
      InvoiceResponse result = apiInstance.patchInvoiceApiV1InvoicesInvoiceIdPatch(invoiceId, invoicePatchRequest, idempotencyKey);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoicesApi#patchInvoiceApiV1InvoicesInvoiceIdPatch");
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
| **invoiceId** | **String**|  | |
| **invoicePatchRequest** | [**InvoicePatchRequest**](InvoicePatchRequest.md)|  | |
| **idempotencyKey** | **String**|  | [optional] |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

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

<a id="previewInvoiceApiV1InvoicesPreviewPost"></a>
# **previewInvoiceApiV1InvoicesPreviewPost**
> Object previewInvoiceApiV1InvoicesPreviewPost(invoicePreviewRequest)

Preview Invoice

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.InvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    InvoicesApi apiInstance = new InvoicesApi(defaultClient);
    InvoicePreviewRequest invoicePreviewRequest = new InvoicePreviewRequest(); // InvoicePreviewRequest | 
    try {
      Object result = apiInstance.previewInvoiceApiV1InvoicesPreviewPost(invoicePreviewRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoicesApi#previewInvoiceApiV1InvoicesPreviewPost");
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
| **invoicePreviewRequest** | [**InvoicePreviewRequest**](InvoicePreviewRequest.md)|  | |

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

<a id="renderInvoiceApiV1InvoicesInvoiceIdRendersPost"></a>
# **renderInvoiceApiV1InvoicesInvoiceIdRendersPost**
> Object renderInvoiceApiV1InvoicesInvoiceIdRendersPost(invoiceId, invoiceRenderRequest, idempotencyKey)

Render Invoice

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.InvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    InvoicesApi apiInstance = new InvoicesApi(defaultClient);
    String invoiceId = "invoiceId_example"; // String | 
    InvoiceRenderRequest invoiceRenderRequest = new InvoiceRenderRequest(); // InvoiceRenderRequest | 
    String idempotencyKey = "idempotencyKey_example"; // String | 
    try {
      Object result = apiInstance.renderInvoiceApiV1InvoicesInvoiceIdRendersPost(invoiceId, invoiceRenderRequest, idempotencyKey);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoicesApi#renderInvoiceApiV1InvoicesInvoiceIdRendersPost");
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
| **invoiceId** | **String**|  | |
| **invoiceRenderRequest** | [**InvoiceRenderRequest**](InvoiceRenderRequest.md)|  | |
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

<a id="replaceInvoiceApiV1InvoicesInvoiceIdPut"></a>
# **replaceInvoiceApiV1InvoicesInvoiceIdPut**
> InvoiceResponse replaceInvoiceApiV1InvoicesInvoiceIdPut(invoiceId, invoiceCreateRequest, idempotencyKey)

Replace Invoice

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.InvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    InvoicesApi apiInstance = new InvoicesApi(defaultClient);
    String invoiceId = "invoiceId_example"; // String | 
    InvoiceCreateRequest invoiceCreateRequest = new InvoiceCreateRequest(); // InvoiceCreateRequest | 
    String idempotencyKey = "idempotencyKey_example"; // String | 
    try {
      InvoiceResponse result = apiInstance.replaceInvoiceApiV1InvoicesInvoiceIdPut(invoiceId, invoiceCreateRequest, idempotencyKey);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoicesApi#replaceInvoiceApiV1InvoicesInvoiceIdPut");
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
| **invoiceId** | **String**|  | |
| **invoiceCreateRequest** | [**InvoiceCreateRequest**](InvoiceCreateRequest.md)|  | |
| **idempotencyKey** | **String**|  | [optional] |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

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

<a id="restoreInvoiceApiV1InvoicesInvoiceIdRestorePost"></a>
# **restoreInvoiceApiV1InvoicesInvoiceIdRestorePost**
> InvoiceResponse restoreInvoiceApiV1InvoicesInvoiceIdRestorePost(invoiceId)

Restore Invoice

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.InvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    InvoicesApi apiInstance = new InvoicesApi(defaultClient);
    String invoiceId = "invoiceId_example"; // String | 
    try {
      InvoiceResponse result = apiInstance.restoreInvoiceApiV1InvoicesInvoiceIdRestorePost(invoiceId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoicesApi#restoreInvoiceApiV1InvoicesInvoiceIdRestorePost");
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
| **invoiceId** | **String**|  | |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

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

<a id="sendInvoiceApiV1InvoicesInvoiceIdSendPost"></a>
# **sendInvoiceApiV1InvoicesInvoiceIdSendPost**
> DeliveryResponse sendInvoiceApiV1InvoicesInvoiceIdSendPost(invoiceId, deliverySendRequest)

Send Invoice

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.InvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    InvoicesApi apiInstance = new InvoicesApi(defaultClient);
    String invoiceId = "invoiceId_example"; // String | 
    DeliverySendRequest deliverySendRequest = new DeliverySendRequest(); // DeliverySendRequest | 
    try {
      DeliveryResponse result = apiInstance.sendInvoiceApiV1InvoicesInvoiceIdSendPost(invoiceId, deliverySendRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoicesApi#sendInvoiceApiV1InvoicesInvoiceIdSendPost");
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
| **invoiceId** | **String**|  | |
| **deliverySendRequest** | [**DeliverySendRequest**](DeliverySendRequest.md)|  | |

### Return type

[**DeliveryResponse**](DeliveryResponse.md)

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

<a id="validateInvoiceApiV1InvoicesValidatePost"></a>
# **validateInvoiceApiV1InvoicesValidatePost**
> Map&lt;String, Object&gt; validateInvoiceApiV1InvoicesValidatePost(invoiceDraftRequest)

Validate Invoice

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.InvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    InvoicesApi apiInstance = new InvoicesApi(defaultClient);
    InvoiceDraftRequest invoiceDraftRequest = new InvoiceDraftRequest(); // InvoiceDraftRequest | 
    try {
      Map<String, Object> result = apiInstance.validateInvoiceApiV1InvoicesValidatePost(invoiceDraftRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoicesApi#validateInvoiceApiV1InvoicesValidatePost");
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
| **invoiceDraftRequest** | [**InvoiceDraftRequest**](InvoiceDraftRequest.md)|  | |

### Return type

**Map&lt;String, Object&gt;**

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

<a id="voidInvoiceApiV1InvoicesInvoiceIdVoidPost"></a>
# **voidInvoiceApiV1InvoicesInvoiceIdVoidPost**
> InvoiceResponse voidInvoiceApiV1InvoicesInvoiceIdVoidPost(invoiceId)

Void Invoice

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.InvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    InvoicesApi apiInstance = new InvoicesApi(defaultClient);
    String invoiceId = "invoiceId_example"; // String | 
    try {
      InvoiceResponse result = apiInstance.voidInvoiceApiV1InvoicesInvoiceIdVoidPost(invoiceId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoicesApi#voidInvoiceApiV1InvoicesInvoiceIdVoidPost");
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
| **invoiceId** | **String**|  | |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

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

