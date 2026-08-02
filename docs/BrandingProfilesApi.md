# BrandingProfilesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createProfileApiV1BrandingProfilesPost**](BrandingProfilesApi.md#createProfileApiV1BrandingProfilesPost) | **POST** /api/v1/branding-profiles | Create Profile |
| [**deleteLogoApiV1BrandingProfilesProfileIdLogoDelete**](BrandingProfilesApi.md#deleteLogoApiV1BrandingProfilesProfileIdLogoDelete) | **DELETE** /api/v1/branding-profiles/{profile_id}/logo | Delete Logo |
| [**deleteProfileApiV1BrandingProfilesProfileIdDelete**](BrandingProfilesApi.md#deleteProfileApiV1BrandingProfilesProfileIdDelete) | **DELETE** /api/v1/branding-profiles/{profile_id} | Delete Profile |
| [**getProfileApiV1BrandingProfilesProfileIdGet**](BrandingProfilesApi.md#getProfileApiV1BrandingProfilesProfileIdGet) | **GET** /api/v1/branding-profiles/{profile_id} | Get Profile |
| [**listProfilesApiV1BrandingProfilesGet**](BrandingProfilesApi.md#listProfilesApiV1BrandingProfilesGet) | **GET** /api/v1/branding-profiles | List Profiles |
| [**setDefaultApiV1BrandingProfilesProfileIdDefaultPost**](BrandingProfilesApi.md#setDefaultApiV1BrandingProfilesProfileIdDefaultPost) | **POST** /api/v1/branding-profiles/{profile_id}/default | Set Default |
| [**updateProfileApiV1BrandingProfilesProfileIdPatch**](BrandingProfilesApi.md#updateProfileApiV1BrandingProfilesProfileIdPatch) | **PATCH** /api/v1/branding-profiles/{profile_id} | Update Profile |
| [**uploadLogoApiV1BrandingProfilesProfileIdLogoPost**](BrandingProfilesApi.md#uploadLogoApiV1BrandingProfilesProfileIdLogoPost) | **POST** /api/v1/branding-profiles/{profile_id}/logo | Upload Logo |


<a id="createProfileApiV1BrandingProfilesPost"></a>
# **createProfileApiV1BrandingProfilesPost**
> BrandingProfileResponse createProfileApiV1BrandingProfilesPost(brandingProfileCreateRequest)

Create Profile

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BrandingProfilesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BrandingProfilesApi apiInstance = new BrandingProfilesApi(defaultClient);
    BrandingProfileCreateRequest brandingProfileCreateRequest = new BrandingProfileCreateRequest(); // BrandingProfileCreateRequest | 
    try {
      BrandingProfileResponse result = apiInstance.createProfileApiV1BrandingProfilesPost(brandingProfileCreateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BrandingProfilesApi#createProfileApiV1BrandingProfilesPost");
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
| **brandingProfileCreateRequest** | [**BrandingProfileCreateRequest**](BrandingProfileCreateRequest.md)|  | |

### Return type

[**BrandingProfileResponse**](BrandingProfileResponse.md)

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

<a id="deleteLogoApiV1BrandingProfilesProfileIdLogoDelete"></a>
# **deleteLogoApiV1BrandingProfilesProfileIdLogoDelete**
> SimpleBoolResponse deleteLogoApiV1BrandingProfilesProfileIdLogoDelete(profileId)

Delete Logo

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BrandingProfilesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BrandingProfilesApi apiInstance = new BrandingProfilesApi(defaultClient);
    String profileId = "profileId_example"; // String | 
    try {
      SimpleBoolResponse result = apiInstance.deleteLogoApiV1BrandingProfilesProfileIdLogoDelete(profileId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BrandingProfilesApi#deleteLogoApiV1BrandingProfilesProfileIdLogoDelete");
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
| **profileId** | **String**|  | |

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

<a id="deleteProfileApiV1BrandingProfilesProfileIdDelete"></a>
# **deleteProfileApiV1BrandingProfilesProfileIdDelete**
> SimpleBoolResponse deleteProfileApiV1BrandingProfilesProfileIdDelete(profileId)

Delete Profile

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BrandingProfilesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BrandingProfilesApi apiInstance = new BrandingProfilesApi(defaultClient);
    String profileId = "profileId_example"; // String | 
    try {
      SimpleBoolResponse result = apiInstance.deleteProfileApiV1BrandingProfilesProfileIdDelete(profileId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BrandingProfilesApi#deleteProfileApiV1BrandingProfilesProfileIdDelete");
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
| **profileId** | **String**|  | |

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

<a id="getProfileApiV1BrandingProfilesProfileIdGet"></a>
# **getProfileApiV1BrandingProfilesProfileIdGet**
> BrandingProfileResponse getProfileApiV1BrandingProfilesProfileIdGet(profileId)

Get Profile

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BrandingProfilesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BrandingProfilesApi apiInstance = new BrandingProfilesApi(defaultClient);
    String profileId = "profileId_example"; // String | 
    try {
      BrandingProfileResponse result = apiInstance.getProfileApiV1BrandingProfilesProfileIdGet(profileId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BrandingProfilesApi#getProfileApiV1BrandingProfilesProfileIdGet");
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
| **profileId** | **String**|  | |

### Return type

[**BrandingProfileResponse**](BrandingProfileResponse.md)

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

<a id="listProfilesApiV1BrandingProfilesGet"></a>
# **listProfilesApiV1BrandingProfilesGet**
> BrandingProfilesListResponse listProfilesApiV1BrandingProfilesGet()

List Profiles

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BrandingProfilesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BrandingProfilesApi apiInstance = new BrandingProfilesApi(defaultClient);
    try {
      BrandingProfilesListResponse result = apiInstance.listProfilesApiV1BrandingProfilesGet();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BrandingProfilesApi#listProfilesApiV1BrandingProfilesGet");
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

[**BrandingProfilesListResponse**](BrandingProfilesListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

<a id="setDefaultApiV1BrandingProfilesProfileIdDefaultPost"></a>
# **setDefaultApiV1BrandingProfilesProfileIdDefaultPost**
> BrandingProfileResponse setDefaultApiV1BrandingProfilesProfileIdDefaultPost(profileId)

Set Default

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BrandingProfilesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BrandingProfilesApi apiInstance = new BrandingProfilesApi(defaultClient);
    String profileId = "profileId_example"; // String | 
    try {
      BrandingProfileResponse result = apiInstance.setDefaultApiV1BrandingProfilesProfileIdDefaultPost(profileId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BrandingProfilesApi#setDefaultApiV1BrandingProfilesProfileIdDefaultPost");
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
| **profileId** | **String**|  | |

### Return type

[**BrandingProfileResponse**](BrandingProfileResponse.md)

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

<a id="updateProfileApiV1BrandingProfilesProfileIdPatch"></a>
# **updateProfileApiV1BrandingProfilesProfileIdPatch**
> BrandingProfileResponse updateProfileApiV1BrandingProfilesProfileIdPatch(profileId, brandingProfilePatchRequest)

Update Profile

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BrandingProfilesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BrandingProfilesApi apiInstance = new BrandingProfilesApi(defaultClient);
    String profileId = "profileId_example"; // String | 
    BrandingProfilePatchRequest brandingProfilePatchRequest = new BrandingProfilePatchRequest(); // BrandingProfilePatchRequest | 
    try {
      BrandingProfileResponse result = apiInstance.updateProfileApiV1BrandingProfilesProfileIdPatch(profileId, brandingProfilePatchRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BrandingProfilesApi#updateProfileApiV1BrandingProfilesProfileIdPatch");
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
| **profileId** | **String**|  | |
| **brandingProfilePatchRequest** | [**BrandingProfilePatchRequest**](BrandingProfilePatchRequest.md)|  | |

### Return type

[**BrandingProfileResponse**](BrandingProfileResponse.md)

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

<a id="uploadLogoApiV1BrandingProfilesProfileIdLogoPost"></a>
# **uploadLogoApiV1BrandingProfilesProfileIdLogoPost**
> BrandingProfileResponse uploadLogoApiV1BrandingProfilesProfileIdLogoPost(profileId, _file)

Upload Logo

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BrandingProfilesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BrandingProfilesApi apiInstance = new BrandingProfilesApi(defaultClient);
    String profileId = "profileId_example"; // String | 
    File _file = new File("/path/to/file"); // File | 
    try {
      BrandingProfileResponse result = apiInstance.uploadLogoApiV1BrandingProfilesProfileIdLogoPost(profileId, _file);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BrandingProfilesApi#uploadLogoApiV1BrandingProfilesProfileIdLogoPost");
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
| **profileId** | **String**|  | |
| **_file** | **File**|  | |

### Return type

[**BrandingProfileResponse**](BrandingProfileResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

