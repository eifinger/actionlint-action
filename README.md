# actionlint-action

Installs [actionlint](https://github.com/rhysd/actionlint) and runs it on all workflow files in the repository. Validates the checksum of the downloaded binary against the checksums published in the [actionlint release notes](https://github.com/rhysd/actionlint/releases).

## Usage

```yaml
- name: Lint GitHub Actions
  uses: eifinger/actionlint-action@v1
```

You can also install a specific version:

```yaml
- name: Lint GitHub Actions
  uses: eifinger/actionlint-action@v1
  with:
    version: "v1.6.24"
```

## Validating the checksum

For versions `v1.6.24` up to `v1.6.25` the checksum of the downloaded binary is verified against the checksums published in the [actionlint release notes](https://github.com/rhysd/actionlint/releases).
For later versions you can use the `checksum` input to verify the checksum of the downloaded binary.

```yaml
- name: Lint GitHub Actions
  uses: eifinger/actionlint-action@v1
  with:
    version: "v99.0.1"
    checksum: "4c5818744143a5d6754edd3dcc4c2b32c9dfcdd3bb30e0e108fb5e5c505262d4"
---

<a href="https://www.buymeacoffee.com/eifinger" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/black_img.png" alt="Buy Me A Coffee" style="height: auto !important;width: auto !important;" ></a><br>
