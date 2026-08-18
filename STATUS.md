# quanttide-product 状态报告

> 更新日期：2026-08-18
> 最新主仓库 commit：d73fa6e

## apps/ — 应用

| 子模块 | 版本 | commit |
|--------|------|--------|
| `qtcloud-product` | studio/v0.1.0-alpha.7 | 1b3e9cf |

## data/ — 陈述性记忆

| 子模块 | 版本 | commit |
|--------|------|--------|
| `archive` | heads/main | 5efc82d |
| `brochure` | heads/main | b0da8db |
| `context` | heads/main | 4f163b7 |
| `insight` | heads/main | 590fb77 |
| `journal` | heads/main | 333cd36 |
| `profile` | heads/main | ee49fa8 |

## docs/ — 程序性记忆

| 子模块 | 版本 | commit |
|--------|------|--------|
| `gallery` | heads/main | 443be63 |
| `handbook` | heads/main | c64bdc4 |
| `specification` | heads/main | 5840468 |
| `tutorial` | heads/main | 02b8760 |

## examples/ — 实验室

| 子模块 | 版本 | commit |
|--------|------|--------|
| `company` | heads/main | cd83342 |
| `default` | heads/main | c8be2d9 |

## packages/ — 工具包

| 子模块 | 版本 | commit |
|--------|------|--------|
| `default` | heads/main | ce2a0d1 |

## 部署

| 项 | 值 |
|----|----|
| Studio 线上地址 | https://product.cloud.quanttide.com（已上线，2026-08-16） |
| 部署链路 | `studio/*` tag → GitHub Actions（flutter build web）→ OSS `qtcloud-product-studio` → CDN |
| IaC | `apps/qtcloud-product/manifests/terraform`（OSS 桶 + CDN + DNS，状态存 OSS `quanttide-product/terraform.tfstate`） |
| 证书 | acme.sh 签发 `product.cloud.quanttide.com` 单域名证书（DNS-01，自动续期 + CDN reload） |
