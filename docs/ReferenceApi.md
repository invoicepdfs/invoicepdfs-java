# ReferenceApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**listCountries**](ReferenceApi.md#listCountries) | **GET** /api/v1/reference/countries | List Countries |
| [**listCurrencies**](ReferenceApi.md#listCurrencies) | **GET** /api/v1/reference/currencies | List Currencies |
| [**listDocumentTypes**](ReferenceApi.md#listDocumentTypes) | **GET** /api/v1/reference/document-types | List Document Types |
| [**listLocales**](ReferenceApi.md#listLocales) | **GET** /api/v1/reference/locales | List Locales |
| [**listPageSizes**](ReferenceApi.md#listPageSizes) | **GET** /api/v1/reference/page-sizes | List Page Sizes |
| [**listTaxCategories**](ReferenceApi.md#listTaxCategories) | **GET** /api/v1/reference/tax-categories | List Tax Categories |
| [**listTaxSchemes**](ReferenceApi.md#listTaxSchemes) | **GET** /api/v1/reference/tax-schemes | List Tax Schemes |
| [**listTimezones**](ReferenceApi.md#listTimezones) | **GET** /api/v1/reference/timezones | List Timezones |
| [**listUnitCodes**](ReferenceApi.md#listUnitCodes) | **GET** /api/v1/reference/unit-codes | List Unit Codes |


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

<a id="listTaxCategories"></a>
# **listTaxCategories**
> CodeListResponse listTaxCategories()

List Tax Categories

UNCL5305, in full — the VAT treatment of a line, which its rate does not say.  Two lines at 0% may be zero-rated, exempt, reverse-charge or outside scope, and EN 16931 puts them in separate VAT breakdown groups with different mandatory fields. Exhaustive: a category outside this list is wrong.

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
      CodeListResponse result = apiInstance.listTaxCategories();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReferenceApi#listTaxCategories");
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

[**CodeListResponse**](CodeListResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

<a id="listTaxSchemes"></a>
# **listTaxSchemes**
> CodeListResponse listTaxSchemes()

List Tax Schemes

UNCL5153 — which tax regime a document is issued under, one per document.  &#x60;VAT&#x60; is the only member an e-invoice can carry; the others exist so a caller can state that their tax is *not* VAT and be told so, rather than have VAT assumed on their behalf. There is no default: a PDF does not need a scheme, and guessing one puts a claim in a document a tax authority reads that the caller never made.

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
      CodeListResponse result = apiInstance.listTaxSchemes();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReferenceApi#listTaxSchemes");
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

[**CodeListResponse**](CodeListResponse.md)

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

<a id="listUnitCodes"></a>
# **listUnitCodes**
> CodeListResponse listUnitCodes()

List Unit Codes

UN/ECE Recommendation 20 — the unit a line item is measured in.  A **shortlist**: twenty-one of hundreds, ordered by how often an invoice needs them. &#x60;exhaustive&#x60; is false, and it means it — &#x60;unit_code&#x60; accepts any value, nothing validates against this list, and an uncommon code is still correct. Offered because the field takes a code rather than the printed label: mapping \&quot;hrs\&quot; to HUR is an inference that is right until it silently is not, and the audience for the result is a tax authority.

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
      CodeListResponse result = apiInstance.listUnitCodes();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ReferenceApi#listUnitCodes");
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

[**CodeListResponse**](CodeListResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

