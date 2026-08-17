# quanttide-product 状态报告

> 更新日期：2026-08-16
> 最新主仓库 commit：b947da1

## apps/ — 应用

| 子模块 | 版本 | commit |
|--------|------|--------|
| `qtcloud-product` | studio/v0.1.0-alpha.1 | 4dec5a7 |

## data/ — 陈述性记忆

| 子模块 | 版本 | commit |
|--------|------|--------|
| `context` | heads/main | 4f163b7 |
| `insight` | heads/main | fbf8155 |
| `journal` | heads/main | bfeea65 |
| `profile` | heads/main | e614309 |

## docs/ — 程序性记忆

| 子模块 | 版本 | commit |
|--------|------|--------|
| `handbook` | heads/main | 50fe9da |
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
