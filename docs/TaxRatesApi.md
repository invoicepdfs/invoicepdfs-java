# TaxRatesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createTaxRateApiV1TaxRatesPost**](TaxRatesApi.md#createTaxRateApiV1TaxRatesPost) | **POST** /api/v1/tax-rates | Create Tax Rate |
| [**deleteTaxRateApiV1TaxRatesTaxRateIdDelete**](TaxRatesApi.md#deleteTaxRateApiV1TaxRatesTaxRateIdDelete) | **DELETE** /api/v1/tax-rates/{tax_rate_id} | Delete Tax Rate |
| [**getTaxRateApiV1TaxRatesTaxRateIdGet**](TaxRatesApi.md#getTaxRateApiV1TaxRatesTaxRateIdGet) | **GET** /api/v1/tax-rates/{tax_rate_id} | Get Tax Rate |
| [**listTaxRatesApiV1TaxRatesGet**](TaxRatesApi.md#listTaxRatesApiV1TaxRatesGet) | **GET** /api/v1/tax-rates | List Tax Rates |
| [**updateTaxRateApiV1TaxRatesTaxRateIdPatch**](TaxRatesApi.md#updateTaxRateApiV1TaxRatesTaxRateIdPatch) | **PATCH** /api/v1/tax-rates/{tax_rate_id} | Update Tax Rate |


<a id="createTaxRateApiV1TaxRatesPost"></a>
# **createTaxRateApiV1TaxRatesPost**
> TaxRateResponse createTaxRateApiV1TaxRatesPost(taxRateCreateRequest)

Create Tax Rate

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.TaxRatesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    TaxRatesApi apiInstance = new TaxRatesApi(defaultClient);
    TaxRateCreateRequest taxRateCreateRequest = new TaxRateCreateRequest(); // TaxRateCreateRequest | 
    try {
      TaxRateResponse result = apiInstance.createTaxRateApiV1TaxRatesPost(taxRateCreateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TaxRatesApi#createTaxRateApiV1TaxRatesPost");
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
| **taxRateCreateRequest** | [**TaxRateCreateRequest**](TaxRateCreateRequest.md)|  | |

### Return type

[**TaxRateResponse**](TaxRateResponse.md)

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

<a id="deleteTaxRateApiV1TaxRatesTaxRateIdDelete"></a>
# **deleteTaxRateApiV1TaxRatesTaxRateIdDelete**
> SimpleBoolResponse deleteTaxRateApiV1TaxRatesTaxRateIdDelete(taxRateId)

Delete Tax Rate

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.TaxRatesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    TaxRatesApi apiInstance = new TaxRatesApi(defaultClient);
    String taxRateId = "taxRateId_example"; // String | 
    try {
      SimpleBoolResponse result = apiInstance.deleteTaxRateApiV1TaxRatesTaxRateIdDelete(taxRateId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TaxRatesApi#deleteTaxRateApiV1TaxRatesTaxRateIdDelete");
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
| **taxRateId** | **String**|  | |

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

<a id="getTaxRateApiV1TaxRatesTaxRateIdGet"></a>
# **getTaxRateApiV1TaxRatesTaxRateIdGet**
> TaxRateResponse getTaxRateApiV1TaxRatesTaxRateIdGet(taxRateId)

Get Tax Rate

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.TaxRatesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    TaxRatesApi apiInstance = new TaxRatesApi(defaultClient);
    String taxRateId = "taxRateId_example"; // String | 
    try {
      TaxRateResponse result = apiInstance.getTaxRateApiV1TaxRatesTaxRateIdGet(taxRateId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TaxRatesApi#getTaxRateApiV1TaxRatesTaxRateIdGet");
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
| **taxRateId** | **String**|  | |

### Return type

[**TaxRateResponse**](TaxRateResponse.md)

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

<a id="listTaxRatesApiV1TaxRatesGet"></a>
# **listTaxRatesApiV1TaxRatesGet**
> TaxRatesListResponse listTaxRatesApiV1TaxRatesGet(limit, cursor)

List Tax Rates

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.TaxRatesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    TaxRatesApi apiInstance = new TaxRatesApi(defaultClient);
    Integer limit = 50; // Integer | 
    String cursor = "cursor_example"; // String | 
    try {
      TaxRatesListResponse result = apiInstance.listTaxRatesApiV1TaxRatesGet(limit, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TaxRatesApi#listTaxRatesApiV1TaxRatesGet");
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

[**TaxRatesListResponse**](TaxRatesListResponse.md)

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

<a id="updateTaxRateApiV1TaxRatesTaxRateIdPatch"></a>
# **updateTaxRateApiV1TaxRatesTaxRateIdPatch**
> TaxRateResponse updateTaxRateApiV1TaxRatesTaxRateIdPatch(taxRateId, taxRatePatchRequest)

Update Tax Rate

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.TaxRatesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    TaxRatesApi apiInstance = new TaxRatesApi(defaultClient);
    String taxRateId = "taxRateId_example"; // String | 
    TaxRatePatchRequest taxRatePatchRequest = new TaxRatePatchRequest(); // TaxRatePatchRequest | 
    try {
      TaxRateResponse result = apiInstance.updateTaxRateApiV1TaxRatesTaxRateIdPatch(taxRateId, taxRatePatchRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling TaxRatesApi#updateTaxRateApiV1TaxRatesTaxRateIdPatch");
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
| **taxRateId** | **String**|  | |
| **taxRatePatchRequest** | [**TaxRatePatchRequest**](TaxRatePatchRequest.md)|  | |

### Return type

[**TaxRateResponse**](TaxRateResponse.md)

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

