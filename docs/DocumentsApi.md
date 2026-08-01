# DocumentsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**archiveDocumentApiV1DocumentsDocumentIdArchivePost**](DocumentsApi.md#archiveDocumentApiV1DocumentsDocumentIdArchivePost) | **POST** /api/v1/documents/{document_id}/archive | Archive Document |
| [**calculateDocumentApiV1DocumentsCalculatePost**](DocumentsApi.md#calculateDocumentApiV1DocumentsCalculatePost) | **POST** /api/v1/documents/calculate | Calculate Document |
| [**createDocumentApiV1DocumentsPost**](DocumentsApi.md#createDocumentApiV1DocumentsPost) | **POST** /api/v1/documents | Create Document |
| [**deleteDocumentApiV1DocumentsDocumentIdDelete**](DocumentsApi.md#deleteDocumentApiV1DocumentsDocumentIdDelete) | **DELETE** /api/v1/documents/{document_id} | Delete Document |
| [**finalizeDocumentApiV1DocumentsDocumentIdFinalizePost**](DocumentsApi.md#finalizeDocumentApiV1DocumentsDocumentIdFinalizePost) | **POST** /api/v1/documents/{document_id}/finalize | Finalize Document |
| [**getDocumentApiV1DocumentsDocumentIdGet**](DocumentsApi.md#getDocumentApiV1DocumentsDocumentIdGet) | **GET** /api/v1/documents/{document_id} | Get Document |
| [**listDocumentDeliveriesApiV1DocumentsDocumentIdDeliveriesGet**](DocumentsApi.md#listDocumentDeliveriesApiV1DocumentsDocumentIdDeliveriesGet) | **GET** /api/v1/documents/{document_id}/deliveries | List Document Deliveries |
| [**listDocumentsApiV1DocumentsGet**](DocumentsApi.md#listDocumentsApiV1DocumentsGet) | **GET** /api/v1/documents | List Documents |
| [**markPaidApiV1DocumentsDocumentIdMarkPaidPost**](DocumentsApi.md#markPaidApiV1DocumentsDocumentIdMarkPaidPost) | **POST** /api/v1/documents/{document_id}/mark-paid | Mark Paid |
| [**markSentApiV1DocumentsDocumentIdMarkSentPost**](DocumentsApi.md#markSentApiV1DocumentsDocumentIdMarkSentPost) | **POST** /api/v1/documents/{document_id}/mark-sent | Mark Sent |
| [**markUnpaidApiV1DocumentsDocumentIdMarkUnpaidPost**](DocumentsApi.md#markUnpaidApiV1DocumentsDocumentIdMarkUnpaidPost) | **POST** /api/v1/documents/{document_id}/mark-unpaid | Mark Unpaid |
| [**patchDocumentApiV1DocumentsDocumentIdPatch**](DocumentsApi.md#patchDocumentApiV1DocumentsDocumentIdPatch) | **PATCH** /api/v1/documents/{document_id} | Patch Document |
| [**renderDocumentApiV1DocumentsDocumentIdRendersPost**](DocumentsApi.md#renderDocumentApiV1DocumentsDocumentIdRendersPost) | **POST** /api/v1/documents/{document_id}/renders | Render Document |
| [**renderDocumentApiV1DocumentsRenderPost**](DocumentsApi.md#renderDocumentApiV1DocumentsRenderPost) | **POST** /api/v1/documents/render | Render Document |
| [**restoreDocumentApiV1DocumentsDocumentIdRestorePost**](DocumentsApi.md#restoreDocumentApiV1DocumentsDocumentIdRestorePost) | **POST** /api/v1/documents/{document_id}/restore | Restore Document |
| [**sendDocumentApiV1DocumentsDocumentIdSendPost**](DocumentsApi.md#sendDocumentApiV1DocumentsDocumentIdSendPost) | **POST** /api/v1/documents/{document_id}/send | Send Document |
| [**validateDocumentApiV1DocumentsValidatePost**](DocumentsApi.md#validateDocumentApiV1DocumentsValidatePost) | **POST** /api/v1/documents/validate | Validate Document |
| [**voidDocumentApiV1DocumentsDocumentIdVoidPost**](DocumentsApi.md#voidDocumentApiV1DocumentsDocumentIdVoidPost) | **POST** /api/v1/documents/{document_id}/void | Void Document |


<a id="archiveDocumentApiV1DocumentsDocumentIdArchivePost"></a>
# **archiveDocumentApiV1DocumentsDocumentIdArchivePost**
> DocumentResponse archiveDocumentApiV1DocumentsDocumentIdArchivePost(documentId)

Archive Document

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
    String documentId = "documentId_example"; // String | 
    try {
      DocumentResponse result = apiInstance.archiveDocumentApiV1DocumentsDocumentIdArchivePost(documentId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#archiveDocumentApiV1DocumentsDocumentIdArchivePost");
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
| **documentId** | **String**|  | |

### Return type

[**DocumentResponse**](DocumentResponse.md)

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

<a id="createDocumentApiV1DocumentsPost"></a>
# **createDocumentApiV1DocumentsPost**
> DocumentResponse createDocumentApiV1DocumentsPost(documentCreateRequest, idempotencyKey)

Create Document

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
    DocumentCreateRequest documentCreateRequest = new DocumentCreateRequest(); // DocumentCreateRequest | 
    String idempotencyKey = "idempotencyKey_example"; // String | 
    try {
      DocumentResponse result = apiInstance.createDocumentApiV1DocumentsPost(documentCreateRequest, idempotencyKey);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#createDocumentApiV1DocumentsPost");
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
| **documentCreateRequest** | [**DocumentCreateRequest**](DocumentCreateRequest.md)|  | |
| **idempotencyKey** | **String**|  | [optional] |

### Return type

[**DocumentResponse**](DocumentResponse.md)

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

<a id="deleteDocumentApiV1DocumentsDocumentIdDelete"></a>
# **deleteDocumentApiV1DocumentsDocumentIdDelete**
> SimpleBoolResponse deleteDocumentApiV1DocumentsDocumentIdDelete(documentId)

Delete Document

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
    String documentId = "documentId_example"; // String | 
    try {
      SimpleBoolResponse result = apiInstance.deleteDocumentApiV1DocumentsDocumentIdDelete(documentId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#deleteDocumentApiV1DocumentsDocumentIdDelete");
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
| **documentId** | **String**|  | |

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

<a id="finalizeDocumentApiV1DocumentsDocumentIdFinalizePost"></a>
# **finalizeDocumentApiV1DocumentsDocumentIdFinalizePost**
> DocumentResponse finalizeDocumentApiV1DocumentsDocumentIdFinalizePost(documentId)

Finalize Document

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
    String documentId = "documentId_example"; // String | 
    try {
      DocumentResponse result = apiInstance.finalizeDocumentApiV1DocumentsDocumentIdFinalizePost(documentId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#finalizeDocumentApiV1DocumentsDocumentIdFinalizePost");
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
| **documentId** | **String**|  | |

### Return type

[**DocumentResponse**](DocumentResponse.md)

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

<a id="getDocumentApiV1DocumentsDocumentIdGet"></a>
# **getDocumentApiV1DocumentsDocumentIdGet**
> DocumentResponse getDocumentApiV1DocumentsDocumentIdGet(documentId)

Get Document

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
    String documentId = "documentId_example"; // String | 
    try {
      DocumentResponse result = apiInstance.getDocumentApiV1DocumentsDocumentIdGet(documentId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#getDocumentApiV1DocumentsDocumentIdGet");
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
| **documentId** | **String**|  | |

### Return type

[**DocumentResponse**](DocumentResponse.md)

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

<a id="listDocumentDeliveriesApiV1DocumentsDocumentIdDeliveriesGet"></a>
# **listDocumentDeliveriesApiV1DocumentsDocumentIdDeliveriesGet**
> DeliveriesListResponse listDocumentDeliveriesApiV1DocumentsDocumentIdDeliveriesGet(documentId, limit, cursor)

List Document Deliveries

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
    String documentId = "documentId_example"; // String | 
    Integer limit = 50; // Integer | 
    String cursor = "cursor_example"; // String | 
    try {
      DeliveriesListResponse result = apiInstance.listDocumentDeliveriesApiV1DocumentsDocumentIdDeliveriesGet(documentId, limit, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#listDocumentDeliveriesApiV1DocumentsDocumentIdDeliveriesGet");
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
| **documentId** | **String**|  | |
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

<a id="listDocumentsApiV1DocumentsGet"></a>
# **listDocumentsApiV1DocumentsGet**
> DocumentsListResponse listDocumentsApiV1DocumentsGet(limit, cursor, documentType, status)

List Documents

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
    Integer limit = 50; // Integer | 
    String cursor = "cursor_example"; // String | 
    String documentType = "documentType_example"; // String | 
    String status = "status_example"; // String | 
    try {
      DocumentsListResponse result = apiInstance.listDocumentsApiV1DocumentsGet(limit, cursor, documentType, status);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#listDocumentsApiV1DocumentsGet");
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
| **documentType** | **String**|  | [optional] |
| **status** | **String**|  | [optional] |

### Return type

[**DocumentsListResponse**](DocumentsListResponse.md)

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

<a id="markPaidApiV1DocumentsDocumentIdMarkPaidPost"></a>
# **markPaidApiV1DocumentsDocumentIdMarkPaidPost**
> DocumentResponse markPaidApiV1DocumentsDocumentIdMarkPaidPost(documentId)

Mark Paid

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
    String documentId = "documentId_example"; // String | 
    try {
      DocumentResponse result = apiInstance.markPaidApiV1DocumentsDocumentIdMarkPaidPost(documentId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#markPaidApiV1DocumentsDocumentIdMarkPaidPost");
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
| **documentId** | **String**|  | |

### Return type

[**DocumentResponse**](DocumentResponse.md)

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

<a id="markSentApiV1DocumentsDocumentIdMarkSentPost"></a>
# **markSentApiV1DocumentsDocumentIdMarkSentPost**
> DocumentResponse markSentApiV1DocumentsDocumentIdMarkSentPost(documentId)

Mark Sent

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
    String documentId = "documentId_example"; // String | 
    try {
      DocumentResponse result = apiInstance.markSentApiV1DocumentsDocumentIdMarkSentPost(documentId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#markSentApiV1DocumentsDocumentIdMarkSentPost");
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
| **documentId** | **String**|  | |

### Return type

[**DocumentResponse**](DocumentResponse.md)

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

<a id="markUnpaidApiV1DocumentsDocumentIdMarkUnpaidPost"></a>
# **markUnpaidApiV1DocumentsDocumentIdMarkUnpaidPost**
> DocumentResponse markUnpaidApiV1DocumentsDocumentIdMarkUnpaidPost(documentId)

Mark Unpaid

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
    String documentId = "documentId_example"; // String | 
    try {
      DocumentResponse result = apiInstance.markUnpaidApiV1DocumentsDocumentIdMarkUnpaidPost(documentId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#markUnpaidApiV1DocumentsDocumentIdMarkUnpaidPost");
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
| **documentId** | **String**|  | |

### Return type

[**DocumentResponse**](DocumentResponse.md)

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

<a id="patchDocumentApiV1DocumentsDocumentIdPatch"></a>
# **patchDocumentApiV1DocumentsDocumentIdPatch**
> DocumentResponse patchDocumentApiV1DocumentsDocumentIdPatch(documentId, documentPatchRequest)

Patch Document

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
    String documentId = "documentId_example"; // String | 
    DocumentPatchRequest documentPatchRequest = new DocumentPatchRequest(); // DocumentPatchRequest | 
    try {
      DocumentResponse result = apiInstance.patchDocumentApiV1DocumentsDocumentIdPatch(documentId, documentPatchRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#patchDocumentApiV1DocumentsDocumentIdPatch");
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
| **documentId** | **String**|  | |
| **documentPatchRequest** | [**DocumentPatchRequest**](DocumentPatchRequest.md)|  | |

### Return type

[**DocumentResponse**](DocumentResponse.md)

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

<a id="renderDocumentApiV1DocumentsDocumentIdRendersPost"></a>
# **renderDocumentApiV1DocumentsDocumentIdRendersPost**
> Object renderDocumentApiV1DocumentsDocumentIdRendersPost(documentId, appDocumentsSchemasDocumentRenderRequest, idempotencyKey)

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
    String documentId = "documentId_example"; // String | 
    AppDocumentsSchemasDocumentRenderRequest appDocumentsSchemasDocumentRenderRequest = new AppDocumentsSchemasDocumentRenderRequest(); // AppDocumentsSchemasDocumentRenderRequest | 
    String idempotencyKey = "idempotencyKey_example"; // String | 
    try {
      Object result = apiInstance.renderDocumentApiV1DocumentsDocumentIdRendersPost(documentId, appDocumentsSchemasDocumentRenderRequest, idempotencyKey);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#renderDocumentApiV1DocumentsDocumentIdRendersPost");
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
| **documentId** | **String**|  | |
| **appDocumentsSchemasDocumentRenderRequest** | [**AppDocumentsSchemasDocumentRenderRequest**](AppDocumentsSchemasDocumentRenderRequest.md)|  | |
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

<a id="renderDocumentApiV1DocumentsRenderPost"></a>
# **renderDocumentApiV1DocumentsRenderPost**
> Object renderDocumentApiV1DocumentsRenderPost(appSchemasV1DocumentRenderRequest, idempotencyKey)

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
    AppSchemasV1DocumentRenderRequest appSchemasV1DocumentRenderRequest = new AppSchemasV1DocumentRenderRequest(); // AppSchemasV1DocumentRenderRequest | 
    String idempotencyKey = "idempotencyKey_example"; // String | 
    try {
      Object result = apiInstance.renderDocumentApiV1DocumentsRenderPost(appSchemasV1DocumentRenderRequest, idempotencyKey);
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
| **appSchemasV1DocumentRenderRequest** | [**AppSchemasV1DocumentRenderRequest**](AppSchemasV1DocumentRenderRequest.md)|  | |
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

<a id="restoreDocumentApiV1DocumentsDocumentIdRestorePost"></a>
# **restoreDocumentApiV1DocumentsDocumentIdRestorePost**
> DocumentResponse restoreDocumentApiV1DocumentsDocumentIdRestorePost(documentId)

Restore Document

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
    String documentId = "documentId_example"; // String | 
    try {
      DocumentResponse result = apiInstance.restoreDocumentApiV1DocumentsDocumentIdRestorePost(documentId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#restoreDocumentApiV1DocumentsDocumentIdRestorePost");
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
| **documentId** | **String**|  | |

### Return type

[**DocumentResponse**](DocumentResponse.md)

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

<a id="sendDocumentApiV1DocumentsDocumentIdSendPost"></a>
# **sendDocumentApiV1DocumentsDocumentIdSendPost**
> DeliveryResponse sendDocumentApiV1DocumentsDocumentIdSendPost(documentId, deliverySendRequest)

Send Document

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
    String documentId = "documentId_example"; // String | 
    DeliverySendRequest deliverySendRequest = new DeliverySendRequest(); // DeliverySendRequest | 
    try {
      DeliveryResponse result = apiInstance.sendDocumentApiV1DocumentsDocumentIdSendPost(documentId, deliverySendRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#sendDocumentApiV1DocumentsDocumentIdSendPost");
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
| **documentId** | **String**|  | |
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

<a id="voidDocumentApiV1DocumentsDocumentIdVoidPost"></a>
# **voidDocumentApiV1DocumentsDocumentIdVoidPost**
> DocumentResponse voidDocumentApiV1DocumentsDocumentIdVoidPost(documentId)

Void Document

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
    String documentId = "documentId_example"; // String | 
    try {
      DocumentResponse result = apiInstance.voidDocumentApiV1DocumentsDocumentIdVoidPost(documentId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#voidDocumentApiV1DocumentsDocumentIdVoidPost");
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
| **documentId** | **String**|  | |

### Return type

[**DocumentResponse**](DocumentResponse.md)

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

