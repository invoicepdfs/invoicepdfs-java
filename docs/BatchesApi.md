# BatchesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**cancelBatch**](BatchesApi.md#cancelBatch) | **POST** /api/v1/batches/{batch_id}/cancel | Cancel Batch |
| [**createBatch**](BatchesApi.md#createBatch) | **POST** /api/v1/batches | Create Batch |
| [**downloadBatch**](BatchesApi.md#downloadBatch) | **GET** /api/v1/batches/{batch_id}/download | Download Batch |
| [**getBatch**](BatchesApi.md#getBatch) | **GET** /api/v1/batches/{batch_id} | Get Batch |
| [**listBatchItems**](BatchesApi.md#listBatchItems) | **GET** /api/v1/batches/{batch_id}/items | List Batch Items |
| [**listBatches**](BatchesApi.md#listBatches) | **GET** /api/v1/batches | List Batches |


<a id="cancelBatch"></a>
# **cancelBatch**
> BatchResponse cancelBatch(batchId)

Cancel Batch

Stop a batch that has not finished.  Items not yet started are cancelled. An item already rendering completes — the work is done and cancelling it would waste it.

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BatchesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BatchesApi apiInstance = new BatchesApi(defaultClient);
    String batchId = "batchId_example"; // String | 
    try {
      BatchResponse result = apiInstance.cancelBatch(batchId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BatchesApi#cancelBatch");
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
| **batchId** | **String**|  | |

### Return type

[**BatchResponse**](BatchResponse.md)

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

<a id="createBatch"></a>
# **createBatch**
> BatchResponse createBatch(batchCreateRequest)

Create Batch

Queue many documents to be rendered at once.  Returns &#x60;202&#x60; — the batch is recorded and a worker renders it; nothing is rendered inside this request. Poll &#x60;get_batch&#x60; for progress, then &#x60;download_batch&#x60; for the results.  The whole batch is refused if it would exceed the monthly quota, rather than rendering part of it.

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BatchesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BatchesApi apiInstance = new BatchesApi(defaultClient);
    BatchCreateRequest batchCreateRequest = new BatchCreateRequest(); // BatchCreateRequest | 
    try {
      BatchResponse result = apiInstance.createBatch(batchCreateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BatchesApi#createBatch");
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
| **batchCreateRequest** | [**BatchCreateRequest**](BatchCreateRequest.md)|  | |

### Return type

[**BatchResponse**](BatchResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="downloadBatch"></a>
# **downloadBatch**
> File downloadBatch(batchId)

Download Batch

Every completed render in the batch, as a ZIP.  &#x60;409&#x60; until the batch is &#x60;completed&#x60;. Items that failed are simply absent, so check &#x60;failed_items&#x60; rather than counting files.

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BatchesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BatchesApi apiInstance = new BatchesApi(defaultClient);
    String batchId = "batchId_example"; // String | 
    try {
      File result = apiInstance.downloadBatch(batchId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BatchesApi#downloadBatch");
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
| **batchId** | **String**|  | |

### Return type

[**File**](File.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/zip, application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | ZIP archive of every completed render in the batch |  -  |
| **422** | Validation Error |  -  |

<a id="getBatch"></a>
# **getBatch**
> BatchResponse getBatch(batchId)

Get Batch

A batch&#39;s status and its per-item counts.  The poll surface: &#x60;total_items&#x60;, &#x60;completed_items&#x60; and &#x60;failed_items&#x60; say how far it has got without listing every item.

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BatchesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BatchesApi apiInstance = new BatchesApi(defaultClient);
    String batchId = "batchId_example"; // String | 
    try {
      BatchResponse result = apiInstance.getBatch(batchId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BatchesApi#getBatch");
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
| **batchId** | **String**|  | |

### Return type

[**BatchResponse**](BatchResponse.md)

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

<a id="listBatchItems"></a>
# **listBatchItems**
> BatchItemsListResponse listBatchItems(batchId, limit, cursor)

List Batch Items

Every item in a batch with its own status, newest first.  Where to look when &#x60;failed_items&#x60; is not zero: each row carries its error and, once rendered, its &#x60;render_id&#x60;.

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BatchesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BatchesApi apiInstance = new BatchesApi(defaultClient);
    String batchId = "batchId_example"; // String | 
    Integer limit = 50; // Integer | 
    String cursor = "cursor_example"; // String | 
    try {
      BatchItemsListResponse result = apiInstance.listBatchItems(batchId, limit, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BatchesApi#listBatchItems");
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
| **batchId** | **String**|  | |
| **limit** | **Integer**|  | [optional] [default to 50] |
| **cursor** | **String**|  | [optional] |

### Return type

[**BatchItemsListResponse**](BatchItemsListResponse.md)

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

<a id="listBatches"></a>
# **listBatches**
> BatchesListResponse listBatches(limit, cursor)

List Batches

Batch jobs on this account, newest first.

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BatchesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BatchesApi apiInstance = new BatchesApi(defaultClient);
    Integer limit = 50; // Integer | 
    String cursor = "cursor_example"; // String | 
    try {
      BatchesListResponse result = apiInstance.listBatches(limit, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BatchesApi#listBatches");
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

### Return type

[**BatchesListResponse**](BatchesListResponse.md)

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

