# BatchesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**cancelBatchApiV1BatchesBatchIdCancelPost**](BatchesApi.md#cancelBatchApiV1BatchesBatchIdCancelPost) | **POST** /api/v1/batches/{batch_id}/cancel | Cancel Batch |
| [**createBatchApiV1BatchesPost**](BatchesApi.md#createBatchApiV1BatchesPost) | **POST** /api/v1/batches | Create Batch |
| [**downloadBatchApiV1BatchesBatchIdDownloadGet**](BatchesApi.md#downloadBatchApiV1BatchesBatchIdDownloadGet) | **GET** /api/v1/batches/{batch_id}/download | Download Batch |
| [**getBatchApiV1BatchesBatchIdGet**](BatchesApi.md#getBatchApiV1BatchesBatchIdGet) | **GET** /api/v1/batches/{batch_id} | Get Batch |
| [**listBatchItemsApiV1BatchesBatchIdItemsGet**](BatchesApi.md#listBatchItemsApiV1BatchesBatchIdItemsGet) | **GET** /api/v1/batches/{batch_id}/items | List Batch Items |
| [**listBatchesApiV1BatchesGet**](BatchesApi.md#listBatchesApiV1BatchesGet) | **GET** /api/v1/batches | List Batches |


<a id="cancelBatchApiV1BatchesBatchIdCancelPost"></a>
# **cancelBatchApiV1BatchesBatchIdCancelPost**
> BatchResponse cancelBatchApiV1BatchesBatchIdCancelPost(batchId)

Cancel Batch

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
      BatchResponse result = apiInstance.cancelBatchApiV1BatchesBatchIdCancelPost(batchId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BatchesApi#cancelBatchApiV1BatchesBatchIdCancelPost");
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

<a id="createBatchApiV1BatchesPost"></a>
# **createBatchApiV1BatchesPost**
> BatchResponse createBatchApiV1BatchesPost(batchCreateRequest)

Create Batch

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
      BatchResponse result = apiInstance.createBatchApiV1BatchesPost(batchCreateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BatchesApi#createBatchApiV1BatchesPost");
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
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="downloadBatchApiV1BatchesBatchIdDownloadGet"></a>
# **downloadBatchApiV1BatchesBatchIdDownloadGet**
> Object downloadBatchApiV1BatchesBatchIdDownloadGet(batchId)

Download Batch

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
      Object result = apiInstance.downloadBatchApiV1BatchesBatchIdDownloadGet(batchId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BatchesApi#downloadBatchApiV1BatchesBatchIdDownloadGet");
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

**Object**

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

<a id="getBatchApiV1BatchesBatchIdGet"></a>
# **getBatchApiV1BatchesBatchIdGet**
> BatchResponse getBatchApiV1BatchesBatchIdGet(batchId)

Get Batch

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
      BatchResponse result = apiInstance.getBatchApiV1BatchesBatchIdGet(batchId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BatchesApi#getBatchApiV1BatchesBatchIdGet");
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

<a id="listBatchItemsApiV1BatchesBatchIdItemsGet"></a>
# **listBatchItemsApiV1BatchesBatchIdItemsGet**
> BatchItemsListResponse listBatchItemsApiV1BatchesBatchIdItemsGet(batchId, limit, cursor)

List Batch Items

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
      BatchItemsListResponse result = apiInstance.listBatchItemsApiV1BatchesBatchIdItemsGet(batchId, limit, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BatchesApi#listBatchItemsApiV1BatchesBatchIdItemsGet");
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

<a id="listBatchesApiV1BatchesGet"></a>
# **listBatchesApiV1BatchesGet**
> BatchesListResponse listBatchesApiV1BatchesGet(limit, cursor)

List Batches

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
      BatchesListResponse result = apiInstance.listBatchesApiV1BatchesGet(limit, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BatchesApi#listBatchesApiV1BatchesGet");
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

