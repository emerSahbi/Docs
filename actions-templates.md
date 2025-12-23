# actions-templates

This repository stores reusable GitHub Actions templates for standardizing CI/CD workflows across the CyberRangeCZ project. Instead of defining the same CI/CD logic in every repository, other repositories can simply reference these templates.

The repository contains workflow templates for:

*   **Different project types**: `frontend_template.yml`, `java_template.yml`, `python_build_template.yml`
*   **Common tasks**: `get_version.yml`, `tag_control_template.yml`, `tag_push_template.yml`, `branch_config.yml`
*   **Caching**: `nvd_cache.yml` for caching National Vulnerability Database (NVD) data.

It also includes helper scripts in the `scripts` directory for tasks like managing feature branches and protecting `develop` and `master` branches.

By centralizing these workflows, the CyberRangeCZ project ensures consistency and makes it easier to maintain and update the CI/CD pipelines.
