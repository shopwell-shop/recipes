# Symfony Flex Recipes

This repository is hosting Symfony Flex Recipes for Shopwell 6. If you are new to Symfony Flex, please read the [blog post](https://www.shopwell.cn/en/news/shopwell-goes-symfony-flex/).

## Available Recipes

### Shopwell

| Recipe | Description |
|---|---|
| `shopwell/core` | Full Shopwell 6 project skeleton including config, env vars, Docker Compose for MariaDB, and all core bundles |
| `shopwell/administration` | Registers the Administration bundle and copies admin build scripts |
| `shopwell/storefront` | Registers the Storefront bundle, copies build/watch scripts, and sets HTTP cache env vars |
| `shopwell/elasticsearch` | OpenSearch/Elasticsearch integration with config, env vars, and Docker Compose service |
| `shopwell/docker` | Production-ready Dockerfile for building a Shopwell Docker image |
| `shopwell/docker-dev` | Docker Compose development environment with PHP, Node, Caddy, Adminer, and a Makefile |
| `shopwell/dev-tools` | Alias-only recipe for the Shopwell dev-tools package |
| `shopwell/fastly-meta` | Fastly CDN integration with VCL snippet configs and deployment tooling |
| `shopwell/k8s-meta` | Kubernetes deployment configuration for the Shopwell Kubernetes Operator |
| `shopwell/paas-meta` | Platform.sh / Shopwell PaaS deployment configuration and scripts |
| `shopwell/opentelemetry` | OpenTelemetry observability bundle integration |
| `shopwell/fixture-bundle` | Registers the FixtureBundle for creating test/demo data fixtures |

### Symfony

| Recipe | Description |
|---|---|
| `symfony/framework-bundle` | Symfony FrameworkBundle registration and configuration |
| `symfony/console` | Symfony Console composer scripts |
| `symfony/routing` | Symfony Routing configuration |
| `symfony/messenger` | Symfony Messenger transport configuration |
| `symfony/amqp-messenger` | LavinMQ (AMQP) Docker Compose service for Symfony Messenger |
| `symfony/monolog-bundle` | Monolog logging bundle and configuration |
| `symfony/debug-bundle` | Symfony DebugBundle for the dev environment |
| `symfony/mailer` | Mailpit email catcher Docker Compose service |
| `symfony/twig-bundle` | Symfony TwigBundle registration |
| `symfony/translation` | Symfony Translation composer scripts |
| `symfony/validator` | Symfony Validator registration |
| `symfony/lock` | Symfony Lock component |
| `symfony/scheduler` | Symfony Scheduler skeleton class |
| `symfony/property-info` | Symfony PropertyInfo composer scripts |

### Other

| Recipe | Description |
|---|---|
| `doctrine/annotations` | Doctrine Annotations composer scripts |
| `enqueue/dbal` | Enqueue DBAL transport |
| `enqueue/enqueue-bundle` | Enqueue messaging bundle registration |
| `enqueue/redis` | Enqueue Redis transport |
| `sroze/messenger-enqueue-transport` | Adapter connecting Symfony Messenger to Enqueue transports |
| `nyholm/psr7` | PSR-7 HTTP message configuration |
| `open-telemetry/opentelemetry-logger-monolog` | OpenTelemetry Monolog handler for production logging |
| `pentatrion/vite-bundle` | Vite asset bundler integration |

## Contributing

Each recipe is a directory containing a `manifest.json` file. The `manifest.json` file contains the recipe metadata and the list of files to copy.

You can look into the [Symfony documentation](https://github.com/symfony/recipes#creating-recipes) for more information about the recipe format.

The `shopwell/platform` package is automatically updated by the CI. Change only the `core`, `administration` packages.

## Migrating an existing application to Symfony Flex

See [Migration Guide in docs](https://developer.shopwell.cn/docs/guides/installation/template#how-do-i-migrate-from-production-template-to-symfony-flex).
