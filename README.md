# voxty.github.io
vox

```
let licenseKeyApi: string | null = null;
let portalApi: string | null = null;

export function loadBackendApis() {
  fetch('https://raw.githubusercontent.com/voxty/voxty.github.io/main/api/urls.json')
    .then(response => response.json())
    .then(data => {
      licenseKeyApi = data.licenseKeyBackend;
      portalApi = data.portalBackend;
    })
    .catch(error => {
      console.error("Failed to load backend APIs", error);
    });
}

export { licenseKeyApi, portalApi };
```

```
loadBackendApis();

console.log(portalApi);
```
