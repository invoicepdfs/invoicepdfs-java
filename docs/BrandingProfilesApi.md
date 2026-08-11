# BrandingProfilesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createBrandingProfile**](BrandingProfilesApi.md#createBrandingProfile) | **POST** /api/v1/branding-profiles | Create Branding Profile |
| [**deleteBrandingLogo**](BrandingProfilesApi.md#deleteBrandingLogo) | **DELETE** /api/v1/branding-profiles/{profile_id}/logo | Delete Branding Logo |
| [**deleteBrandingProfile**](BrandingProfilesApi.md#deleteBrandingProfile) | **DELETE** /api/v1/branding-profiles/{profile_id} | Delete Branding Profile |
| [**getBrandingProfile**](BrandingProfilesApi.md#getBrandingProfile) | **GET** /api/v1/branding-profiles/{profile_id} | Get Branding Profile |
| [**listBrandingProfiles**](BrandingProfilesApi.md#listBrandingProfiles) | **GET** /api/v1/branding-profiles | List Branding Profiles |
| [**setDefaultBrandingProfile**](BrandingProfilesApi.md#setDefaultBrandingProfile) | **POST** /api/v1/branding-profiles/{profile_id}/default | Set Default Branding Profile |
| [**updateBrandingProfile**](BrandingProfilesApi.md#updateBrandingProfile) | **PATCH** /api/v1/branding-profiles/{profile_id} | Update Branding Profile |
| [**uploadBrandingLogo**](BrandingProfilesApi.md#uploadBrandingLogo) | **POST** /api/v1/branding-profiles/{profile_id}/logo | Upload Branding Logo |


<a id="createBrandingProfile"></a>
# **createBrandingProfile**
> BrandingProfileResponse createBrandingProfile(brandingProfileCreateRequest)

Create Branding Profile

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
      BrandingProfileResponse result = apiInstance.createBrandingProfile(brandingProfileCreateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BrandingProfilesApi#createBrandingProfile");
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

<a id="deleteBrandingLogo"></a>
# **deleteBrandingLogo**
> SimpleBoolResponse deleteBrandingLogo(profileId)

Delete Branding Logo

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
      SimpleBoolResponse result = apiInstance.deleteBrandingLogo(profileId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BrandingProfilesApi#deleteBrandingLogo");
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

<a id="deleteBrandingProfile"></a>
# **deleteBrandingProfile**
> SimpleBoolResponse deleteBrandingProfile(profileId)

Delete Branding Profile

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
      SimpleBoolResponse result = apiInstance.deleteBrandingProfile(profileId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BrandingProfilesApi#deleteBrandingProfile");
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

<a id="getBrandingProfile"></a>
# **getBrandingProfile**
> BrandingProfileResponse getBrandingProfile(profileId)

Get Branding Profile

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
      BrandingProfileResponse result = apiInstance.getBrandingProfile(profileId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BrandingProfilesApi#getBrandingProfile");
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

<a id="listBrandingProfiles"></a>
# **listBrandingProfiles**
> BrandingProfilesListResponse listBrandingProfiles()

List Branding Profiles

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
      BrandingProfilesListResponse result = apiInstance.listBrandingProfiles();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BrandingProfilesApi#listBrandingProfiles");
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

<a id="setDefaultBrandingProfile"></a>
# **setDefaultBrandingProfile**
> BrandingProfileResponse setDefaultBrandingProfile(profileId)

Set Default Branding Profile

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
      BrandingProfileResponse result = apiInstance.setDefaultBrandingProfile(profileId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BrandingProfilesApi#setDefaultBrandingProfile");
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

<a id="updateBrandingProfile"></a>
# **updateBrandingProfile**
> BrandingProfileResponse updateBrandingProfile(profileId, brandingProfilePatchRequest)

Update Branding Profile

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
      BrandingProfileResponse result = apiInstance.updateBrandingProfile(profileId, brandingProfilePatchRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BrandingProfilesApi#updateBrandingProfile");
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

<a id="uploadBrandingLogo"></a>
# **uploadBrandingLogo**
> BrandingProfileResponse uploadBrandingLogo(profileId, _file)

Upload Branding Logo

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
      BrandingProfileResponse result = apiInstance.uploadBrandingLogo(profileId, _file);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BrandingProfilesApi#uploadBrandingLogo");
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

