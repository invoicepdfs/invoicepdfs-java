# ApiKeysApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createApiKeyApiV1ApiKeysPost**](ApiKeysApi.md#createApiKeyApiV1ApiKeysPost) | **POST** /api/v1/api-keys | Create Api Key |
| [**getApiKeyApiV1ApiKeysApiKeyIdGet**](ApiKeysApi.md#getApiKeyApiV1ApiKeysApiKeyIdGet) | **GET** /api/v1/api-keys/{api_key_id} | Get Api Key |
| [**listApiKeysApiV1ApiKeysGet**](ApiKeysApi.md#listApiKeysApiV1ApiKeysGet) | **GET** /api/v1/api-keys | List Api Keys |
| [**patchApiKeyApiV1ApiKeysApiKeyIdPatch**](ApiKeysApi.md#patchApiKeyApiV1ApiKeysApiKeyIdPatch) | **PATCH** /api/v1/api-keys/{api_key_id} | Patch Api Key |
| [**revokeApiKeyApiV1ApiKeysApiKeyIdDelete**](ApiKeysApi.md#revokeApiKeyApiV1ApiKeysApiKeyIdDelete) | **DELETE** /api/v1/api-keys/{api_key_id} | Revoke Api Key |
| [**rotateApiKeyApiV1ApiKeysApiKeyIdRotatePost**](ApiKeysApi.md#rotateApiKeyApiV1ApiKeysApiKeyIdRotatePost) | **POST** /api/v1/api-keys/{api_key_id}/rotate | Rotate Api Key |


<a id="createApiKeyApiV1ApiKeysPost"></a>
# **createApiKeyApiV1ApiKeysPost**
> ApiKeyCreateResponse createApiKeyApiV1ApiKeysPost(apiKeyCreateRequest)

Create Api Key

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.ApiKeysApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    ApiKeysApi apiInstance = new ApiKeysApi(defaultClient);
    ApiKeyCreateRequest apiKeyCreateRequest = new ApiKeyCreateRequest(); // ApiKeyCreateRequest | 
    try {
      ApiKeyCreateResponse result = apiInstance.createApiKeyApiV1ApiKeysPost(apiKeyCreateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApiKeysApi#createApiKeyApiV1ApiKeysPost");
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
| **apiKeyCreateRequest** | [**ApiKeyCreateRequest**](ApiKeyCreateRequest.md)|  | |

### Return type

[**ApiKeyCreateResponse**](ApiKeyCreateResponse.md)

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

<a id="getApiKeyApiV1ApiKeysApiKeyIdGet"></a>
# **getApiKeyApiV1ApiKeysApiKeyIdGet**
> ApiKeyDetailResponse getApiKeyApiV1ApiKeysApiKeyIdGet(apiKeyId)

Get Api Key

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.ApiKeysApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    ApiKeysApi apiInstance = new ApiKeysApi(defaultClient);
    String apiKeyId = "apiKeyId_example"; // String | 
    try {
      ApiKeyDetailResponse result = apiInstance.getApiKeyApiV1ApiKeysApiKeyIdGet(apiKeyId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApiKeysApi#getApiKeyApiV1ApiKeysApiKeyIdGet");
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
| **apiKeyId** | **String**|  | |

### Return type

[**ApiKeyDetailResponse**](ApiKeyDetailResponse.md)

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

<a id="listApiKeysApiV1ApiKeysGet"></a>
# **listApiKeysApiV1ApiKeysGet**
> ApiKeyListResponse listApiKeysApiV1ApiKeysGet()

List Api Keys

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.ApiKeysApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    ApiKeysApi apiInstance = new ApiKeysApi(defaultClient);
    try {
      ApiKeyListResponse result = apiInstance.listApiKeysApiV1ApiKeysGet();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApiKeysApi#listApiKeysApiV1ApiKeysGet");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ApiKeyListResponse**](ApiKeyListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

<a id="patchApiKeyApiV1ApiKeysApiKeyIdPatch"></a>
# **patchApiKeyApiV1ApiKeysApiKeyIdPatch**
> ApiKeyDetailResponse patchApiKeyApiV1ApiKeysApiKeyIdPatch(apiKeyId, apiKeyPatchRequest)

Patch Api Key

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.ApiKeysApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    ApiKeysApi apiInstance = new ApiKeysApi(defaultClient);
    String apiKeyId = "apiKeyId_example"; // String | 
    ApiKeyPatchRequest apiKeyPatchRequest = new ApiKeyPatchRequest(); // ApiKeyPatchRequest | 
    try {
      ApiKeyDetailResponse result = apiInstance.patchApiKeyApiV1ApiKeysApiKeyIdPatch(apiKeyId, apiKeyPatchRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApiKeysApi#patchApiKeyApiV1ApiKeysApiKeyIdPatch");
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
| **apiKeyId** | **String**|  | |
| **apiKeyPatchRequest** | [**ApiKeyPatchRequest**](ApiKeyPatchRequest.md)|  | |

### Return type

[**ApiKeyDetailResponse**](ApiKeyDetailResponse.md)

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

<a id="revokeApiKeyApiV1ApiKeysApiKeyIdDelete"></a>
# **revokeApiKeyApiV1ApiKeysApiKeyIdDelete**
> ApiKeyRevokeResponse revokeApiKeyApiV1ApiKeysApiKeyIdDelete(apiKeyId)

Revoke Api Key

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.ApiKeysApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    ApiKeysApi apiInstance = new ApiKeysApi(defaultClient);
    String apiKeyId = "apiKeyId_example"; // String | 
    try {
      ApiKeyRevokeResponse result = apiInstance.revokeApiKeyApiV1ApiKeysApiKeyIdDelete(apiKeyId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApiKeysApi#revokeApiKeyApiV1ApiKeysApiKeyIdDelete");
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
| **apiKeyId** | **String**|  | |

### Return type

[**ApiKeyRevokeResponse**](ApiKeyRevokeResponse.md)

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

<a id="rotateApiKeyApiV1ApiKeysApiKeyIdRotatePost"></a>
# **rotateApiKeyApiV1ApiKeysApiKeyIdRotatePost**
> ApiKeyRotateResponse rotateApiKeyApiV1ApiKeysApiKeyIdRotatePost(apiKeyId)

Rotate Api Key

Revoke the existing key and create a new one with the same name.

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.ApiKeysApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    ApiKeysApi apiInstance = new ApiKeysApi(defaultClient);
    String apiKeyId = "apiKeyId_example"; // String | 
    try {
      ApiKeyRotateResponse result = apiInstance.rotateApiKeyApiV1ApiKeysApiKeyIdRotatePost(apiKeyId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApiKeysApi#rotateApiKeyApiV1ApiKeysApiKeyIdRotatePost");
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
| **apiKeyId** | **String**|  | |

### Return type

[**ApiKeyRotateResponse**](ApiKeyRotateResponse.md)

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

