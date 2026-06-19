# FF-Dashboard helm chart

Deploys:
  - https://github.com/Minding000/fff-dashboard-frontend
  - https://github.com/Minding000/fff-dashboard-backend

## Release

```bash
helm package .
helm push .\\ff-dashboard-0.1.9.tgz oci://registry.minding.blog/ff-fechenheim/dashboard
git tag 0.1.9
git push
git push --tags
```

## Development

### Troubleshooting

```bash
helm template . --debug --skip-schema-validation
```