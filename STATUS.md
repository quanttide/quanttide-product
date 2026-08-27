# quanttide-product 状态报告

> 更新日期：2026-08-22
> 最新主仓库 commit：e61d38bc275a91f49cda38d9743f12076513f670

## apps/ — 应用

| 子模块 | 版本 | commit |
|--------|------|--------|
| `qtcloud-product` | studio/v0.1.0-beta.3 | c23e7e7 |

## data/ — 陈述性记忆

| 子模块 | 版本 | commit |
|--------|------|--------|
| `archive` | heads/main | 5efc82d |
| `brochure` | heads/main | 5115399 |
| `context` | heads/main | 8375eec |
| `insight` | heads/main | 590fb77 |
| `journal` | heads/main | 4672404 |
| `profile` | heads/main | 6504500 |
| `report` | heads/main | 204b65e |

## docs/ — 程序性记忆

| 子模块 | 版本 | commit |
|--------|------|--------|
| `gallery` | heads/main | 69d7ed4 |
| `handbook` | heads/main | 1206180 |
| `specification` | heads/main | 5840468 |
| `tutorial` | heads/main | 02b8760 |

## examples/ — 实验室

| 子模块 | 版本 | commit |
|--------|------|--------|
| `default` | heads/main | d64d26d |

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
