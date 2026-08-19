# NumberingSequencesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**consumeSequenceNumber**](NumberingSequencesApi.md#consumeSequenceNumber) | **POST** /api/v1/numbering-sequences/{sequence_id}/next | Consume Sequence Number |
| [**createSequence**](NumberingSequencesApi.md#createSequence) | **POST** /api/v1/numbering-sequences | Create Sequence |
| [**deleteSequence**](NumberingSequencesApi.md#deleteSequence) | **DELETE** /api/v1/numbering-sequences/{sequence_id} | Delete Sequence |
| [**getSequence**](NumberingSequencesApi.md#getSequence) | **GET** /api/v1/numbering-sequences/{sequence_id} | Get Sequence |
| [**listSequences**](NumberingSequencesApi.md#listSequences) | **GET** /api/v1/numbering-sequences | List Sequences |
| [**previewSequence**](NumberingSequencesApi.md#previewSequence) | **POST** /api/v1/numbering-sequences/{sequence_id}/preview | Preview Sequence |
| [**updateSequence**](NumberingSequencesApi.md#updateSequence) | **PATCH** /api/v1/numbering-sequences/{sequence_id} | Update Sequence |


<a id="consumeSequenceNumber"></a>
# **consumeSequenceNumber**
> NumberingNextResponse consumeSequenceNumber(sequenceId)

Consume Sequence Number

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
      NumberingNextResponse result = apiInstance.consumeSequenceNumber(sequenceId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NumberingSequencesApi#consumeSequenceNumber");
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

[**NumberingNextResponse**](NumberingNextResponse.md)

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

<a id="createSequence"></a>
# **createSequence**
> NumberingSequenceResponse createSequence(numberingSequenceCreateRequest)

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
      NumberingSequenceResponse result = apiInstance.createSequence(numberingSequenceCreateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NumberingSequencesApi#createSequence");
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

<a id="deleteSequence"></a>
# **deleteSequence**
> SimpleBoolResponse deleteSequence(sequenceId)

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
      SimpleBoolResponse result = apiInstance.deleteSequence(sequenceId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NumberingSequencesApi#deleteSequence");
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

<a id="getSequence"></a>
# **getSequence**
> NumberingSequenceResponse getSequence(sequenceId)

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
      NumberingSequenceResponse result = apiInstance.getSequence(sequenceId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NumberingSequencesApi#getSequence");
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

<a id="listSequences"></a>
# **listSequences**
> NumberingSequencesListResponse listSequences(limit, cursor)

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
      NumberingSequencesListResponse result = apiInstance.listSequences(limit, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NumberingSequencesApi#listSequences");
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

<a id="previewSequence"></a>
# **previewSequence**
> NumberingSequencePreviewResponse previewSequence(sequenceId)

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
      NumberingSequencePreviewResponse result = apiInstance.previewSequence(sequenceId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NumberingSequencesApi#previewSequence");
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

<a id="updateSequence"></a>
# **updateSequence**
> NumberingSequenceResponse updateSequence(sequenceId, numberingSequencePatchRequest)

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
      NumberingSequenceResponse result = apiInstance.updateSequence(sequenceId, numberingSequencePatchRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling NumberingSequencesApi#updateSequence");
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

