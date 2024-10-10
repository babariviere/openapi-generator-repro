# To reproduce

```sh
npm install -D @openapitools/openapi-generator-cli
npx openapi-generator-cli version-manager set 7.9.0
npx openapi-generator-cli generate -i openapi.yaml -g typescript-fetch --skip-validate-spec -o out --additional-properties=withoutRuntimeChecks=true
```

Now, when looking at `out/models/index.ts`, we see this:

```typescript
export interface Get200Response {
    /**
     *
     * @type {string}
     * @memberof Get200Response
     */
    _configuration?: string;
}
```
