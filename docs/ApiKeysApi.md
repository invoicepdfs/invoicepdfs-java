# ApiKeysApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createApiKey**](ApiKeysApi.md#createApiKey) | **POST** /api/v1/api-keys | Create Api Key |
| [**getApiKey**](ApiKeysApi.md#getApiKey) | **GET** /api/v1/api-keys/{api_key_id} | Get Api Key |
| [**listApiKeys**](ApiKeysApi.md#listApiKeys) | **GET** /api/v1/api-keys | List Api Keys |
| [**revokeApiKey**](ApiKeysApi.md#revokeApiKey) | **DELETE** /api/v1/api-keys/{api_key_id} | Revoke Api Key |
| [**rotateApiKey**](ApiKeysApi.md#rotateApiKey) | **POST** /api/v1/api-keys/{api_key_id}/rotate | Rotate Api Key |
| [**updateApiKey**](ApiKeysApi.md#updateApiKey) | **PATCH** /api/v1/api-keys/{api_key_id} | Update Api Key |


<a id="createApiKey"></a>
# **createApiKey**
> ApiKeyCreateResponse createApiKey(apiKeyCreateRequest)

Create Api Key

Create an API key and return it once.  The response is the only place the key appears — it is stored hashed, so a lost key cannot be recovered, only replaced.  Keys are not scoped: any key can do anything this account can, including creating further keys and deleting data. Treat one as a full credential.

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
      ApiKeyCreateResponse result = apiInstance.createApiKey(apiKeyCreateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApiKeysApi#createApiKey");
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

<a id="getApiKey"></a>
# **getApiKey**
> ApiKeyDetailResponse getApiKey(apiKeyId)

Get Api Key

One API key&#39;s details by id, without the key itself.

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
      ApiKeyDetailResponse result = apiInstance.getApiKey(apiKeyId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApiKeysApi#getApiKey");
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

<a id="listApiKeys"></a>
# **listApiKeys**
> ApiKeyListResponse listApiKeys()

List Api Keys

Every API key on the account, including revoked ones.  Shows only the last four characters: the key itself is stored hashed and cannot be recovered.

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
      ApiKeyListResponse result = apiInstance.listApiKeys();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApiKeysApi#listApiKeys");
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

<a id="revokeApiKey"></a>
# **revokeApiKey**
> ApiKeyRevokeResponse revokeApiKey(apiKeyId)

Revoke Api Key

Stop an API key working, permanently.  Takes effect immediately and cannot be undone — issue a new key with &#x60;create_api_key&#x60; instead. The record is kept, so the key still appears in &#x60;list_api_keys&#x60; with a revoked date and the audit log stays readable.  Revoking an already-revoked key succeeds and changes nothing.

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
      ApiKeyRevokeResponse result = apiInstance.revokeApiKey(apiKeyId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApiKeysApi#revokeApiKey");
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

<a id="rotateApiKey"></a>
# **rotateApiKey**
> ApiKeyRotateResponse rotateApiKey(apiKeyId)

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
      ApiKeyRotateResponse result = apiInstance.rotateApiKey(apiKeyId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApiKeysApi#rotateApiKey");
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

<a id="updateApiKey"></a>
# **updateApiKey**
> ApiKeyDetailResponse updateApiKey(apiKeyId, apiKeyPatchRequest)

Update Api Key

Rename an API key.  The key itself is unchanged and keeps working. To replace the secret while keeping the record, use &#x60;rotate_api_key&#x60;.

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
      ApiKeyDetailResponse result = apiInstance.updateApiKey(apiKeyId, apiKeyPatchRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ApiKeysApi#updateApiKey");
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

