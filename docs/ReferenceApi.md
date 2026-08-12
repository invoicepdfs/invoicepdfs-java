# ReferenceApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**listCountries**](ReferenceApi.md#listCountries) | **GET** /api/v1/reference/countries | List Countries |
| [**listCurrencies**](ReferenceApi.md#listCurrencies) | **GET** /api/v1/reference/currencies | List Currencies |
| [**listDocumentTypes**](ReferenceApi.md#listDocumentTypes) | **GET** /api/v1/reference/document-types | List Document Types |
| [**listLocales**](ReferenceApi.md#listLocales) | **GET** /api/v1/reference/locales | List Locales |
| [**listPageSizes**](ReferenceApi.md#listPageSizes) | **GET** /api/v1/reference/page-sizes | List Page Sizes |
| [**listTimezones**](ReferenceApi.md#listTimezones) | **GET** /api/v1/reference/timezones | List Timezones |


<a id="listCountries"></a>
# **listCountries**
> CountriesListResponse listCountries()

List Countries

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.ReferenceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ReferenceApi apiInstance = new ReferenceApi(defaultClient);
    try {
      CountriesListResponse result = apiInstance.listCountries();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReferenceApi#listCountries");
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

[**CountriesListResponse**](CountriesListResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

<a id="listCurrencies"></a>
# **listCurrencies**
> CurrenciesListResponse listCurrencies()

List Currencies

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.ReferenceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ReferenceApi apiInstance = new ReferenceApi(defaultClient);
    try {
      CurrenciesListResponse result = apiInstance.listCurrencies();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReferenceApi#listCurrencies");
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

[**CurrenciesListResponse**](CurrenciesListResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

<a id="listDocumentTypes"></a>
# **listDocumentTypes**
> DocumentTypesListResponse listDocumentTypes()

List Document Types

List every supported document type with the metadata a client needs to build a type-aware create form: the number prefix, whether it is payable / takes a source document / supports a reason, which line-item shape it uses (&#x60;&#x60;standard&#x60;&#x60; &#x3D; priced, &#x60;&#x60;shipped&#x60;&#x60; &#x3D; quantities only), and the lifecycle actions available to it.

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.ReferenceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ReferenceApi apiInstance = new ReferenceApi(defaultClient);
    try {
      DocumentTypesListResponse result = apiInstance.listDocumentTypes();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReferenceApi#listDocumentTypes");
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

[**DocumentTypesListResponse**](DocumentTypesListResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

<a id="listLocales"></a>
# **listLocales**
> LocalesListResponse listLocales()

List Locales

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.ReferenceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ReferenceApi apiInstance = new ReferenceApi(defaultClient);
    try {
      LocalesListResponse result = apiInstance.listLocales();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReferenceApi#listLocales");
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

[**LocalesListResponse**](LocalesListResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

<a id="listPageSizes"></a>
# **listPageSizes**
> PageSizesListResponse listPageSizes()

List Page Sizes

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.ReferenceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ReferenceApi apiInstance = new ReferenceApi(defaultClient);
    try {
      PageSizesListResponse result = apiInstance.listPageSizes();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReferenceApi#listPageSizes");
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

[**PageSizesListResponse**](PageSizesListResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

<a id="listTimezones"></a>
# **listTimezones**
> TimezonesListResponse listTimezones()

List Timezones

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.ReferenceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    ReferenceApi apiInstance = new ReferenceApi(defaultClient);
    try {
      TimezonesListResponse result = apiInstance.listTimezones();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReferenceApi#listTimezones");
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

[**TimezonesListResponse**](TimezonesListResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

