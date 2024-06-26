# Hugo Clarity for Company Website

A [Hugo](https://gohugo.io/) theme based on [Hugo Clarity](https://github.com/chipzoller/hugo-clarity/) with customization for company website.

## Set author and description of home page
The template(`layouts/partials/opengraph.html`) reads the description from a page frontmatter. For the homepage, that would be in `content/_index.md`.

```
+++
author = "My Company"
description = "My Company. Since 1984" # set your site's description here. will be use for home page content meta tags (seo).
+++
```

## Customization
* Show Hotline

  Set `"hotline"` in `/data/company.json`.
  If "hotline" is set(not empty), phone numbers of contacts will be **hidden**.

* Show company contact information on the side bar
  
  Set `"contacts"`(slice) in `/data/company.json`

  contact object description

  | field | type | desc |
  | :--: | :--: | :--: |
  | name | string | contact name |
  | address | string | address information |
  | phone_nums | string slice | phone numbers |
  | work_time | string | work time |

* Show 微博(weibo) link

  | field | type | desc |
  | :--: | :--: | :--: |
  | weibo | string | Weibo account |

* Show 微信(weixin) ID and keyword
  
  weixin object

  | field | type | desc |
  | :--: | :--: | :--: |
  | id | string | Wechat ID |
  | keyword | string | keyword to search in Wechat |

* Show ICP 备案 and 公安备案 for China users

  | field | type | desc |
  | :--: | :--: | :--: |
  | icp | string | ICP 备案号 |
  | gongan_beian | string | 公安备案号 |

## Example Configuration in [exampleSite/data/company.json](exampleSite/data/company.json)

```
{
        "hotline": "400-xxx-xxxx",
        "contacts": [
            {
                "name":"上海办事处",
                "address":"徐汇区xx路xx号",
                "phone_nums":["66666666", "88888888"],
                "work_time":"10:00至18:00（周一休息）"
            },
            {
                "name":"北京办事处",
                "address":"海淀区xx路xx号",
                "phone_nums":["33333333", "55555555"],
                "work_time":"11:00至17:00（周六，日休息）"
            }
           ],
        "weibo": "https://weibo.com/YOUR_WEIBO_ACCOUNT",
        "weixin": {"id": "YOUR_WECHAT_ID", "keyword": "公司名称"},
        "icp": "沪ICP备XX号",
        "gongan_beian": "沪公安备XX号"
}
```
