# ReferenceApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**listCountriesApiV1ReferenceCountriesGet**](ReferenceApi.md#listCountriesApiV1ReferenceCountriesGet) | **GET** /api/v1/reference/countries | List Countries |
| [**listCurrenciesApiV1ReferenceCurrenciesGet**](ReferenceApi.md#listCurrenciesApiV1ReferenceCurrenciesGet) | **GET** /api/v1/reference/currencies | List Currencies |
| [**listDocumentTypesApiV1ReferenceDocumentTypesGet**](ReferenceApi.md#listDocumentTypesApiV1ReferenceDocumentTypesGet) | **GET** /api/v1/reference/document-types | List Document Types |
| [**listLocalesApiV1ReferenceLocalesGet**](ReferenceApi.md#listLocalesApiV1ReferenceLocalesGet) | **GET** /api/v1/reference/locales | List Locales |
| [**listPageSizesApiV1ReferencePageSizesGet**](ReferenceApi.md#listPageSizesApiV1ReferencePageSizesGet) | **GET** /api/v1/reference/page-sizes | List Page Sizes |
| [**listTimezonesApiV1ReferenceTimezonesGet**](ReferenceApi.md#listTimezonesApiV1ReferenceTimezonesGet) | **GET** /api/v1/reference/timezones | List Timezones |


<a id="listCountriesApiV1ReferenceCountriesGet"></a>
# **listCountriesApiV1ReferenceCountriesGet**
> Map&lt;String, Object&gt; listCountriesApiV1ReferenceCountriesGet()

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
      Map<String, Object> result = apiInstance.listCountriesApiV1ReferenceCountriesGet();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReferenceApi#listCountriesApiV1ReferenceCountriesGet");
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

**Map&lt;String, Object&gt;**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

<a id="listCurrenciesApiV1ReferenceCurrenciesGet"></a>
# **listCurrenciesApiV1ReferenceCurrenciesGet**
> Map&lt;String, Object&gt; listCurrenciesApiV1ReferenceCurrenciesGet()

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
      Map<String, Object> result = apiInstance.listCurrenciesApiV1ReferenceCurrenciesGet();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReferenceApi#listCurrenciesApiV1ReferenceCurrenciesGet");
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

**Map&lt;String, Object&gt;**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

<a id="listDocumentTypesApiV1ReferenceDocumentTypesGet"></a>
# **listDocumentTypesApiV1ReferenceDocumentTypesGet**
> Map&lt;String, Object&gt; listDocumentTypesApiV1ReferenceDocumentTypesGet()

List Document Types

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
      Map<String, Object> result = apiInstance.listDocumentTypesApiV1ReferenceDocumentTypesGet();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReferenceApi#listDocumentTypesApiV1ReferenceDocumentTypesGet");
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

**Map&lt;String, Object&gt;**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

<a id="listLocalesApiV1ReferenceLocalesGet"></a>
# **listLocalesApiV1ReferenceLocalesGet**
> Map&lt;String, Object&gt; listLocalesApiV1ReferenceLocalesGet()

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
      Map<String, Object> result = apiInstance.listLocalesApiV1ReferenceLocalesGet();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReferenceApi#listLocalesApiV1ReferenceLocalesGet");
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

**Map&lt;String, Object&gt;**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

<a id="listPageSizesApiV1ReferencePageSizesGet"></a>
# **listPageSizesApiV1ReferencePageSizesGet**
> Map&lt;String, Object&gt; listPageSizesApiV1ReferencePageSizesGet()

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
      Map<String, Object> result = apiInstance.listPageSizesApiV1ReferencePageSizesGet();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReferenceApi#listPageSizesApiV1ReferencePageSizesGet");
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

**Map&lt;String, Object&gt;**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

<a id="listTimezonesApiV1ReferenceTimezonesGet"></a>
# **listTimezonesApiV1ReferenceTimezonesGet**
> Map&lt;String, Object&gt; listTimezonesApiV1ReferenceTimezonesGet()

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
      Map<String, Object> result = apiInstance.listTimezonesApiV1ReferenceTimezonesGet();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReferenceApi#listTimezonesApiV1ReferenceTimezonesGet");
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

**Map&lt;String, Object&gt;**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

