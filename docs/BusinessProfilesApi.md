# BusinessProfilesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createBusinessProfile**](BusinessProfilesApi.md#createBusinessProfile) | **POST** /api/v1/business-profiles | Create Business Profile |
| [**deleteBusinessProfile**](BusinessProfilesApi.md#deleteBusinessProfile) | **DELETE** /api/v1/business-profiles/{business_profile_id} | Delete Business Profile |
| [**getBusinessProfile**](BusinessProfilesApi.md#getBusinessProfile) | **GET** /api/v1/business-profiles/{business_profile_id} | Get Business Profile |
| [**listBusinessProfiles**](BusinessProfilesApi.md#listBusinessProfiles) | **GET** /api/v1/business-profiles | List Business Profiles |
| [**updateBusinessProfile**](BusinessProfilesApi.md#updateBusinessProfile) | **PATCH** /api/v1/business-profiles/{business_profile_id} | Update Business Profile |


<a id="createBusinessProfile"></a>
# **createBusinessProfile**
> BusinessProfileResponse createBusinessProfile(businessProfileCreate, idempotencyKey)

Create Business Profile

Create an identity to issue documents as: the seller side.  &#x60;legal_name&#x60;, &#x60;tax_id&#x60;, address and bank details are what appears as the issuer, and what an e-invoicing ruleset checks. Distinct from a branding profile, which sets colours and a logo and says nothing about who you are.

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
      BusinessProfileResponse result = apiInstance.createBusinessProfile(businessProfileCreate, idempotencyKey);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BusinessProfilesApi#createBusinessProfile");
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

<a id="deleteBusinessProfile"></a>
# **deleteBusinessProfile**
> SimpleBoolResponse deleteBusinessProfile(businessProfileId)

Delete Business Profile

Remove a business profile.  &#x60;409&#x60; if any document was issued under it, naming what still points at it.

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
      SimpleBoolResponse result = apiInstance.deleteBusinessProfile(businessProfileId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BusinessProfilesApi#deleteBusinessProfile");
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
| **409** | The profile is named on documents or recurring invoices. &#x60;details.referenced_by&#x60; counts each one. |  -  |
| **422** | Validation Error |  -  |

<a id="getBusinessProfile"></a>
# **getBusinessProfile**
> BusinessProfileResponse getBusinessProfile(businessProfileId)

Get Business Profile

One business profile.

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
      BusinessProfileResponse result = apiInstance.getBusinessProfile(businessProfileId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BusinessProfilesApi#getBusinessProfile");
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

<a id="listBusinessProfiles"></a>
# **listBusinessProfiles**
> BusinessProfilesListResponse listBusinessProfiles(limit, cursor)

List Business Profiles

The identities you issue documents *as*, newest first.  One per entity you bill from — a business with two trading names or two tax registrations needs two. For how documents *look* rather than who issues them, see the branding profiles.

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
      BusinessProfilesListResponse result = apiInstance.listBusinessProfiles(limit, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BusinessProfilesApi#listBusinessProfiles");
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

<a id="updateBusinessProfile"></a>
# **updateBusinessProfile**
> BusinessProfileResponse updateBusinessProfile(businessProfileId, businessProfilePatch, idempotencyKey)

Update Business Profile

Change a business profile.  Only the fields you send are changed. Documents already issued keep the issuer details they carried at the time.

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
      BusinessProfileResponse result = apiInstance.updateBusinessProfile(businessProfileId, businessProfilePatch, idempotencyKey);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BusinessProfilesApi#updateBusinessProfile");
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

