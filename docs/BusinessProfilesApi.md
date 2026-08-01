# BusinessProfilesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createBusinessProfileApiV1BusinessProfilesPost**](BusinessProfilesApi.md#createBusinessProfileApiV1BusinessProfilesPost) | **POST** /api/v1/business-profiles | Create Business Profile |
| [**deleteBusinessProfileApiV1BusinessProfilesBusinessProfileIdDelete**](BusinessProfilesApi.md#deleteBusinessProfileApiV1BusinessProfilesBusinessProfileIdDelete) | **DELETE** /api/v1/business-profiles/{business_profile_id} | Delete Business Profile |
| [**getBusinessProfileApiV1BusinessProfilesBusinessProfileIdGet**](BusinessProfilesApi.md#getBusinessProfileApiV1BusinessProfilesBusinessProfileIdGet) | **GET** /api/v1/business-profiles/{business_profile_id} | Get Business Profile |
| [**listBusinessProfilesApiV1BusinessProfilesGet**](BusinessProfilesApi.md#listBusinessProfilesApiV1BusinessProfilesGet) | **GET** /api/v1/business-profiles | List Business Profiles |
| [**patchBusinessProfileApiV1BusinessProfilesBusinessProfileIdPatch**](BusinessProfilesApi.md#patchBusinessProfileApiV1BusinessProfilesBusinessProfileIdPatch) | **PATCH** /api/v1/business-profiles/{business_profile_id} | Patch Business Profile |


<a id="createBusinessProfileApiV1BusinessProfilesPost"></a>
# **createBusinessProfileApiV1BusinessProfilesPost**
> BusinessProfileResponse createBusinessProfileApiV1BusinessProfilesPost(businessProfileCreate, idempotencyKey)

Create Business Profile

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BusinessProfilesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BusinessProfilesApi apiInstance = new BusinessProfilesApi(defaultClient);
    BusinessProfileCreate businessProfileCreate = new BusinessProfileCreate(); // BusinessProfileCreate | 
    String idempotencyKey = "idempotencyKey_example"; // String | 
    try {
      BusinessProfileResponse result = apiInstance.createBusinessProfileApiV1BusinessProfilesPost(businessProfileCreate, idempotencyKey);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BusinessProfilesApi#createBusinessProfileApiV1BusinessProfilesPost");
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
| **businessProfileCreate** | [**BusinessProfileCreate**](BusinessProfileCreate.md)|  | |
| **idempotencyKey** | **String**|  | [optional] |

### Return type

[**BusinessProfileResponse**](BusinessProfileResponse.md)

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

<a id="deleteBusinessProfileApiV1BusinessProfilesBusinessProfileIdDelete"></a>
# **deleteBusinessProfileApiV1BusinessProfilesBusinessProfileIdDelete**
> SimpleBoolResponse deleteBusinessProfileApiV1BusinessProfilesBusinessProfileIdDelete(businessProfileId)

Delete Business Profile

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BusinessProfilesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BusinessProfilesApi apiInstance = new BusinessProfilesApi(defaultClient);
    String businessProfileId = "businessProfileId_example"; // String | 
    try {
      SimpleBoolResponse result = apiInstance.deleteBusinessProfileApiV1BusinessProfilesBusinessProfileIdDelete(businessProfileId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BusinessProfilesApi#deleteBusinessProfileApiV1BusinessProfilesBusinessProfileIdDelete");
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
| **businessProfileId** | **String**|  | |

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

<a id="getBusinessProfileApiV1BusinessProfilesBusinessProfileIdGet"></a>
# **getBusinessProfileApiV1BusinessProfilesBusinessProfileIdGet**
> BusinessProfileResponse getBusinessProfileApiV1BusinessProfilesBusinessProfileIdGet(businessProfileId)

Get Business Profile

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BusinessProfilesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BusinessProfilesApi apiInstance = new BusinessProfilesApi(defaultClient);
    String businessProfileId = "businessProfileId_example"; // String | 
    try {
      BusinessProfileResponse result = apiInstance.getBusinessProfileApiV1BusinessProfilesBusinessProfileIdGet(businessProfileId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BusinessProfilesApi#getBusinessProfileApiV1BusinessProfilesBusinessProfileIdGet");
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
| **businessProfileId** | **String**|  | |

### Return type

[**BusinessProfileResponse**](BusinessProfileResponse.md)

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

<a id="listBusinessProfilesApiV1BusinessProfilesGet"></a>
# **listBusinessProfilesApiV1BusinessProfilesGet**
> BusinessProfilesListResponse listBusinessProfilesApiV1BusinessProfilesGet(limit, cursor)

List Business Profiles

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BusinessProfilesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BusinessProfilesApi apiInstance = new BusinessProfilesApi(defaultClient);
    Integer limit = 50; // Integer | 
    String cursor = "cursor_example"; // String | 
    try {
      BusinessProfilesListResponse result = apiInstance.listBusinessProfilesApiV1BusinessProfilesGet(limit, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BusinessProfilesApi#listBusinessProfilesApiV1BusinessProfilesGet");
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

[**BusinessProfilesListResponse**](BusinessProfilesListResponse.md)

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

<a id="patchBusinessProfileApiV1BusinessProfilesBusinessProfileIdPatch"></a>
# **patchBusinessProfileApiV1BusinessProfilesBusinessProfileIdPatch**
> BusinessProfileResponse patchBusinessProfileApiV1BusinessProfilesBusinessProfileIdPatch(businessProfileId, businessProfilePatch, idempotencyKey)

Patch Business Profile

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BusinessProfilesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BusinessProfilesApi apiInstance = new BusinessProfilesApi(defaultClient);
    String businessProfileId = "businessProfileId_example"; // String | 
    BusinessProfilePatch businessProfilePatch = new BusinessProfilePatch(); // BusinessProfilePatch | 
    String idempotencyKey = "idempotencyKey_example"; // String | 
    try {
      BusinessProfileResponse result = apiInstance.patchBusinessProfileApiV1BusinessProfilesBusinessProfileIdPatch(businessProfileId, businessProfilePatch, idempotencyKey);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BusinessProfilesApi#patchBusinessProfileApiV1BusinessProfilesBusinessProfileIdPatch");
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
| **businessProfileId** | **String**|  | |
| **businessProfilePatch** | [**BusinessProfilePatch**](BusinessProfilePatch.md)|  | |
| **idempotencyKey** | **String**|  | [optional] |

### Return type

[**BusinessProfileResponse**](BusinessProfileResponse.md)

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

