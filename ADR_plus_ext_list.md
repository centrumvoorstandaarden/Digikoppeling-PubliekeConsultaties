normative Design Rules

|Rule|Auto|method|
|---|---|---|
|API-01: Adhere to HTTP safety and idempotency semantics for operations|no||
|API-02: Do not maintain session state on the server|no||
|API-03: Only apply standard HTTP methods|yes|inspecting oas|
|API-04: Define interfaces in Dutch unless there is an official English glossary available|yes|complex|
|API-05: Use nouns to name resources|?||
|API-06: Use nested URIs for child resources|yes|complex|
|API-10: Model resource operations as a sub-resource or dedicated resource|?||
|API-16: Use OpenAPI Specification for documentation|yes||
|API-17: Publish documentation in Dutch unless there is existing documentation in English|yes|complex|
|API-18: Include a deprecation schedule when publishing API changes|?||
|API-19: Schedule a fixed transition period for a new major API version|no||
|API-20: Include the major version number in the URI|yes||
|API-48: Leave off trailing slashes from URIs|yes||
|API-51: Publish OAS document at a standard location in JSON-format|yes||
|API-53: Hide irrelevant implementation details|no||
|API-54: Use plural nouns to name collection resources|?||
|API-55: Publish a changelog for API changes between versions|no||
|API-56: Adhere to the Semantic Versioning model when releasing API changes|?||
|API-57: Return the full version number in a response header|yes||


Extensions

|Rule|Auto|method|
|---|---|---|
|API-09: Implement custom representation if supported|no||
|API-11: Encrypt connections using TLS|yes||
|API-13: Accept tokens as HTTP headers only|?||
|API-15: Use PKIoverheid certificates for access-restricted or purpose-limited API authentication|yes||
|API-21: Inform users of a deprecated API actively|no||
|API-22: JSON first - APIs receive and send JSON|?||
|API-23: APIs may provide a JSON Schema|no||
|API-24: Support content negotiation|no||
|API-25: Check the Content-Type header value|no||
|API-26: Define field names in camelCase|?||
|API-27: Disable pretty print|no||
|API-28: Send a JSON-response without enclosing envelope|no||
|API-29: Support JSON request body for POST and PUT operations|no||
|API-30: Use query parameters corresponding to the queryable fields|no||
|API-31: Use the query parameter sort to apply sorting|no||
|API-32: Use the query parameter search for full-text search|no||
|API-33: Support both * and ? wildcard characters for full-text search APIs|no||
|API-34: Support GeoJSON for geospatial APIs|no||
|API-35: Include GeoJSON as part of the embedded resource in the JSON response|no||
|API-36: Provide a POST endpoint for geo queries|no||
|API-37: Support mixed queries at POST endpoints|no||
|API-38: Put results of a global spatial query in the relevant geometric context|no||
|API-39: Use ETRS89 as the preferred coordinate reference system (CRS)|no||
|API-40: Pass the coordinate reference system (CRS) of the request and the response in the headers|no||
|API-41: Use content negotiation to serve different CRSs|no||
|API-42: Use JSON+HAL with media type application/hal+json for pagination|no||
|API-43: Apply caching to improve performance|no||
|API-44: Apply rate limiting|no||
|API-45: Provide rate limiting information|no||
|API-46: Use default error handling|no||
|API-47: Use the required HTTP status codes|no||
|API-49: Use public API-keys|no||
|API-50: Use CORS to control access|no||
|API-52: Use OAuth 2.0 for authorization with rights delegation|no||

lalala
