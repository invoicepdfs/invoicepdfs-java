# BrandingApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**deleteLogoApiV1BrandingLogoDelete**](BrandingApi.md#deleteLogoApiV1BrandingLogoDelete) | **DELETE** /api/v1/branding/logo | Delete Logo |
| [**getBrandingApiV1BrandingGet**](BrandingApi.md#getBrandingApiV1BrandingGet) | **GET** /api/v1/branding | Get Branding |
| [**updateBrandingApiV1BrandingPut**](BrandingApi.md#updateBrandingApiV1BrandingPut) | **PUT** /api/v1/branding | Update Branding |
| [**uploadLogoApiV1BrandingLogoPost**](BrandingApi.md#uploadLogoApiV1BrandingLogoPost) | **POST** /api/v1/branding/logo | Upload Logo |


<a id="deleteLogoApiV1BrandingLogoDelete"></a>
# **deleteLogoApiV1BrandingLogoDelete**
> SimpleBoolResponse deleteLogoApiV1BrandingLogoDelete()

Delete Logo

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BrandingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BrandingApi apiInstance = new BrandingApi(defaultClient);
    try {
      SimpleBoolResponse result = apiInstance.deleteLogoApiV1BrandingLogoDelete();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BrandingApi#deleteLogoApiV1BrandingLogoDelete");
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

<a id="getBrandingApiV1BrandingGet"></a>
# **getBrandingApiV1BrandingGet**
> BrandingResponse getBrandingApiV1BrandingGet()

Get Branding

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BrandingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BrandingApi apiInstance = new BrandingApi(defaultClient);
    try {
      BrandingResponse result = apiInstance.getBrandingApiV1BrandingGet();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BrandingApi#getBrandingApiV1BrandingGet");
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

[**BrandingResponse**](BrandingResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

<a id="updateBrandingApiV1BrandingPut"></a>
# **updateBrandingApiV1BrandingPut**
> BrandingResponse updateBrandingApiV1BrandingPut(brandingUpdateRequest)

Update Branding

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BrandingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BrandingApi apiInstance = new BrandingApi(defaultClient);
    BrandingUpdateRequest brandingUpdateRequest = new BrandingUpdateRequest(); // BrandingUpdateRequest | 
    try {
      BrandingResponse result = apiInstance.updateBrandingApiV1BrandingPut(brandingUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BrandingApi#updateBrandingApiV1BrandingPut");
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
| **brandingUpdateRequest** | [**BrandingUpdateRequest**](BrandingUpdateRequest.md)|  | |

### Return type

[**BrandingResponse**](BrandingResponse.md)

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

<a id="uploadLogoApiV1BrandingLogoPost"></a>
# **uploadLogoApiV1BrandingLogoPost**
> BrandingResponse uploadLogoApiV1BrandingLogoPost(_file)

Upload Logo

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BrandingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BrandingApi apiInstance = new BrandingApi(defaultClient);
    File _file = new File("/path/to/file"); // File | 
    try {
      BrandingResponse result = apiInstance.uploadLogoApiV1BrandingLogoPost(_file);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BrandingApi#uploadLogoApiV1BrandingLogoPost");
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
| **_file** | **File**|  | |

### Return type

[**BrandingResponse**](BrandingResponse.md)

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

