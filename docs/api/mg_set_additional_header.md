# Civetweb API Reference

### `mg_set_additional_header( conn, header );`

### Parameters

| Parameter | Type | Description |
| :--- | :--- | :--- |
|**`conn`**|`struct mg_connection *`|The connection over which the data must be sent|
|**`header`**|`const char *`|The additional header to be sent|

### Description

The function `mg_set_additional_header()` can be used to specify one or more additional headers to be sent when sending the next server response.
The `header` string is sent verbatim, with only an appended `"\r\n"`, so must be in a standard HTTP header format such as `"Allow: GET, POST"`.
Multiple headers can be included in the string if they are separated by `"\r\n"`, such as `"Allow: GET, POST\r\nAccept: application/json"`.

An existing additional header can be removed by specifying `NULL` for `header`, or a zero-length string (`""`).

### See Also

* [`mg_send_http_error();`](mg_send_http_error.md)
* [`mg_send_http_ok();`](mg_send_http_ok.md)
* [`mg_send_http_redirect();`](mg_send_http_redirect.md)

