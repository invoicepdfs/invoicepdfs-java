# NumberingSequencesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**consumeNextApiV1NumberingSequencesSequenceIdNextPost**](NumberingSequencesApi.md#consumeNextApiV1NumberingSequencesSequenceIdNextPost) | **POST** /api/v1/numbering-sequences/{sequence_id}/next | Consume Next |
| [**createSequenceApiV1NumberingSequencesPost**](NumberingSequencesApi.md#createSequenceApiV1NumberingSequencesPost) | **POST** /api/v1/numbering-sequences | Create Sequence |
| [**deleteSequenceApiV1NumberingSequencesSequenceIdDelete**](NumberingSequencesApi.md#deleteSequenceApiV1NumberingSequencesSequenceIdDelete) | **DELETE** /api/v1/numbering-sequences/{sequence_id} | Delete Sequence |
| [**getSequenceApiV1NumberingSequencesSequenceIdGet**](NumberingSequencesApi.md#getSequenceApiV1NumberingSequencesSequenceIdGet) | **GET** /api/v1/numbering-sequences/{sequence_id} | Get Sequence |
| [**listSequencesApiV1NumberingSequencesGet**](NumberingSequencesApi.md#listSequencesApiV1NumberingSequencesGet) | **GET** /api/v1/numbering-sequences | List Sequences |
| [**previewSequenceApiV1NumberingSequencesSequenceIdPreviewPost**](NumberingSequencesApi.md#previewSequenceApiV1NumberingSequencesSequenceIdPreviewPost) | **POST** /api/v1/numbering-sequences/{sequence_id}/preview | Preview Sequence |
| [**updateSequenceApiV1NumberingSequencesSequenceIdPatch**](NumberingSequencesApi.md#updateSequenceApiV1NumberingSequencesSequenceIdPatch) | **PATCH** /api/v1/numbering-sequences/{sequence_id} | Update Sequence |


<a id="consumeNextApiV1NumberingSequencesSequenceIdNextPost"></a>
# **consumeNextApiV1NumberingSequencesSequenceIdNextPost**
> NumberingSequenceResponse consumeNextApiV1NumberingSequencesSequenceIdNextPost(sequenceId)

Consume Next

Consume and return the next number, incrementing the counter.

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.NumberingSequencesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    NumberingSequencesApi apiInstance = new NumberingSequencesApi(defaultClient);
    String sequenceId = "sequenceId_example"; // String | 
    try {
      NumberingSequenceResponse result = apiInstance.consumeNextApiV1NumberingSequencesSequenceIdNextPost(sequenceId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NumberingSequencesApi#consumeNextApiV1NumberingSequencesSequenceIdNextPost");
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
| **sequenceId** | **String**|  | |

### Return type

[**NumberingSequenceResponse**](NumberingSequenceResponse.md)

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

<a id="createSequenceApiV1NumberingSequencesPost"></a>
# **createSequenceApiV1NumberingSequencesPost**
> NumberingSequenceResponse createSequenceApiV1NumberingSequencesPost(numberingSequenceCreateRequest)

Create Sequence

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.NumberingSequencesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    NumberingSequencesApi apiInstance = new NumberingSequencesApi(defaultClient);
    NumberingSequenceCreateRequest numberingSequenceCreateRequest = new NumberingSequenceCreateRequest(); // NumberingSequenceCreateRequest | 
    try {
      NumberingSequenceResponse result = apiInstance.createSequenceApiV1NumberingSequencesPost(numberingSequenceCreateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NumberingSequencesApi#createSequenceApiV1NumberingSequencesPost");
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
| **numberingSequenceCreateRequest** | [**NumberingSequenceCreateRequest**](NumberingSequenceCreateRequest.md)|  | |

### Return type

[**NumberingSequenceResponse**](NumberingSequenceResponse.md)

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

<a id="deleteSequenceApiV1NumberingSequencesSequenceIdDelete"></a>
# **deleteSequenceApiV1NumberingSequencesSequenceIdDelete**
> SimpleBoolResponse deleteSequenceApiV1NumberingSequencesSequenceIdDelete(sequenceId)

Delete Sequence

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.NumberingSequencesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    NumberingSequencesApi apiInstance = new NumberingSequencesApi(defaultClient);
    String sequenceId = "sequenceId_example"; // String | 
    try {
      SimpleBoolResponse result = apiInstance.deleteSequenceApiV1NumberingSequencesSequenceIdDelete(sequenceId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NumberingSequencesApi#deleteSequenceApiV1NumberingSequencesSequenceIdDelete");
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
| **sequenceId** | **String**|  | |

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

<a id="getSequenceApiV1NumberingSequencesSequenceIdGet"></a>
# **getSequenceApiV1NumberingSequencesSequenceIdGet**
> NumberingSequenceResponse getSequenceApiV1NumberingSequencesSequenceIdGet(sequenceId)

Get Sequence

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.NumberingSequencesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    NumberingSequencesApi apiInstance = new NumberingSequencesApi(defaultClient);
    String sequenceId = "sequenceId_example"; // String | 
    try {
      NumberingSequenceResponse result = apiInstance.getSequenceApiV1NumberingSequencesSequenceIdGet(sequenceId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NumberingSequencesApi#getSequenceApiV1NumberingSequencesSequenceIdGet");
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
| **sequenceId** | **String**|  | |

### Return type

[**NumberingSequenceResponse**](NumberingSequenceResponse.md)

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

<a id="listSequencesApiV1NumberingSequencesGet"></a>
# **listSequencesApiV1NumberingSequencesGet**
> NumberingSequencesListResponse listSequencesApiV1NumberingSequencesGet(limit, cursor)

List Sequences

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.NumberingSequencesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    NumberingSequencesApi apiInstance = new NumberingSequencesApi(defaultClient);
    Integer limit = 50; // Integer | 
    String cursor = "cursor_example"; // String | 
    try {
      NumberingSequencesListResponse result = apiInstance.listSequencesApiV1NumberingSequencesGet(limit, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NumberingSequencesApi#listSequencesApiV1NumberingSequencesGet");
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

[**NumberingSequencesListResponse**](NumberingSequencesListResponse.md)

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

<a id="previewSequenceApiV1NumberingSequencesSequenceIdPreviewPost"></a>
# **previewSequenceApiV1NumberingSequencesSequenceIdPreviewPost**
> NumberingSequencePreviewResponse previewSequenceApiV1NumberingSequencesSequenceIdPreviewPost(sequenceId)

Preview Sequence

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.NumberingSequencesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    NumberingSequencesApi apiInstance = new NumberingSequencesApi(defaultClient);
    String sequenceId = "sequenceId_example"; // String | 
    try {
      NumberingSequencePreviewResponse result = apiInstance.previewSequenceApiV1NumberingSequencesSequenceIdPreviewPost(sequenceId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NumberingSequencesApi#previewSequenceApiV1NumberingSequencesSequenceIdPreviewPost");
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
| **sequenceId** | **String**|  | |

### Return type

[**NumberingSequencePreviewResponse**](NumberingSequencePreviewResponse.md)

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

<a id="updateSequenceApiV1NumberingSequencesSequenceIdPatch"></a>
# **updateSequenceApiV1NumberingSequencesSequenceIdPatch**
> NumberingSequenceResponse updateSequenceApiV1NumberingSequencesSequenceIdPatch(sequenceId, numberingSequencePatchRequest)

Update Sequence

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.NumberingSequencesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    NumberingSequencesApi apiInstance = new NumberingSequencesApi(defaultClient);
    String sequenceId = "sequenceId_example"; // String | 
    NumberingSequencePatchRequest numberingSequencePatchRequest = new NumberingSequencePatchRequest(); // NumberingSequencePatchRequest | 
    try {
      NumberingSequenceResponse result = apiInstance.updateSequenceApiV1NumberingSequencesSequenceIdPatch(sequenceId, numberingSequencePatchRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NumberingSequencesApi#updateSequenceApiV1NumberingSequencesSequenceIdPatch");
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
| **sequenceId** | **String**|  | |
| **numberingSequencePatchRequest** | [**NumberingSequencePatchRequest**](NumberingSequencePatchRequest.md)|  | |

### Return type

[**NumberingSequenceResponse**](NumberingSequenceResponse.md)

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

