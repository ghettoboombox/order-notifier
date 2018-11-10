The module sends a new order's data to a specified URL in a JSON format.

## How to install
```
bin/magento maintenance:enable
composer require mage2pro/order-notifier:*
bin/magento setup:upgrade
rm -rf var/di var/generation generated/code && bin/magento setup:di:compile
rm -rf pub/static/* && bin/magento setup:static-content:deploy en_US <additional locales, e.g.: de_DE>
bin/magento maintenance:disable
```

## How to update

```
bin/magento maintenance:enable
composer update mage2pro/order-notifier
bin/magento setup:upgrade
rm -rf var/di var/generation generated/code && bin/magento setup:di:compile
rm -rf pub/static/* && bin/magento setup:static-content:deploy en_US <additional locales, e.g.: de_DE>
bin/magento maintenance:disable
```

## Backend settings

![](https://mage2.pro/uploads/default/original/2X/2/24d60a7898a939b2a41b8056e8a0a08c174c60fc.png)

## Data example

```
{
    "billing_address": {
        "customer_address_id": 1,
        "firstname": "Dmitry",
        "lastname": "Fedyuk",
        "company": "Mage2.PRO",
        "street": "49 West 32nd Street",
        "city": "New York City",
        "region": "New York",
        "region_id": 43,
        "postcode": "10001",
        "country_id": "US",
        "telephone": "+1 (212) 736-3800",
        "email": "admin@mage2.pro",
        "address_type": "billing",
        "quote_address_id": "3"
    },
    "customer": {
        "entity_id": "1",
        "website_id": "1",
        "email": "admin@mage2.pro",
        "group_id": "1",
        "store_id": "1",
        "created_at": "2018-11-10 03:43:40",
        "updated_at": "2018-11-10 03:45:05",
        "is_active": "1",
        "disable_auto_group_change": "0",
        "created_in": "Default Store View",
        "firstname": "Dmitry",
        "lastname": "Fedyuk",
        "password_hash": "2883bc388fc6e435a487ad764651d8330837752624190d7e676bf643083cad40:GdM9zNcXdyBWQ9ynDfWAcwsnJCg34JJz:1",
        "rp_token": "p9APUBBSZfsLiz9KJSwF9F30jcdr73vu",
        "rp_token_created_at": "2018-11-10 03:43:40",
        "default_billing": "1",
        "default_shipping": "1",
        "failures_num": "0"
    },
    "line_items": [
        {
            "id": "2",
            "image": "https://localhost.com:2003/pub/media/catalog/product/cache/10f519365b01716ddb90abc57de5a837/1/8/18fe627tul_chm_main_1_1.jpeg",
            "name": "Lamé Embroidered Tulle Cocktail Dress-4",
            "price": 7190,
            "price_with_discount": 7190,
            "price_with_discount_and_tax": 7190,
            "price_with_tax": 7190,
            "qty": 1,
            "sku": "18FE627TUL-4",
            "tax_rate": 0,
            "url": "https://localhost.com:2003/lame-embroidered-tulle-cocktail-dress.html"
        },
        {
            "id": "6",
            "image": "https://localhost.com:2003/pub/media/catalog/product/cache/10f519365b01716ddb90abc57de5a837/1/8/18fh7002vlt_1.jpg",
            "name": "Embroidered Velvet Rogan Clutch",
            "price": 1990,
            "price_with_discount": 1990,
            "price_with_discount_and_tax": 1990,
            "price_with_tax": 1990,
            "qty": 1,
            "sku": "18FH7002VLT",
            "tax_rate": 0,
            "url": "https://localhost.com:2003/embroidered-velvet-rogan-clutch.html"
        }
    ],
    "payment": {
        "method": "checkmo",
        "additional_information": {
            "method_title": "Check / Money order"
        },
        "amount_ordered": 9190,
        "base_amount_ordered": 9190,
        "shipping_amount": 10,
        "base_shipping_amount": 10
    },
    "shipping_address": {
        "customer_address_id": "1",
        "firstname": "Dmitry",
        "lastname": "Fedyuk",
        "company": "Mage2.PRO",
        "street": "49 West 32nd Street",
        "city": "New York City",
        "region": "New York",
        "region_id": "43",
        "postcode": "10001",
        "country_id": "US",
        "telephone": "+1 (212) 736-3800",
        "email": "admin@mage2.pro",
        "address_type": "shipping",
        "quote_address_id": "2"
    },
    "visitor": {
        "http_user_agent": "Mozilla/5.0 (Windows NT 6.1; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/70.0.3538.77 Safari/537.36",
        "remote_addr": "127.0.0.1"
    },
    "base_currency_code": "USD",
    "base_discount_amount": 0,
    "base_grand_total": 9190,
    "base_discount_tax_compensation_amount": 0,
    "base_shipping_amount": 10,
    "base_shipping_discount_amount": 0,
    "base_shipping_discount_tax_compensation_amnt": 0,
    "base_shipping_incl_tax": 10,
    "base_shipping_tax_amount": 0,
    "base_subtotal": 9180,
    "base_subtotal_incl_tax": 9180,
    "base_tax_amount": 0,
    "base_total_due": 9190,
    "base_to_global_rate": 1,
    "base_to_order_rate": 1,
    "customer_email": "admin@mage2.pro",
    "customer_firstname": "Dmitry",
    "customer_group_id": 1,
    "customer_id": "1",
    "customer_is_guest": 0,
    "customer_lastname": "Fedyuk",
    "customer_note_notify": 1,
    "discount_amount": 0,
    "global_currency_code": "USD",
    "grand_total": 9190,
    "discount_tax_compensation_amount": 0,
    "increment_id": "000000001",
    "is_virtual": 0,
    "order_currency_code": "USD",
    "quote_id": "1",
    "remote_ip": "127.0.0.1",
    "shipping_amount": 10,
    "shipping_description": "Flat Rate - Fixed",
    "shipping_discount_amount": 0,
    "shipping_discount_tax_compensation_amount": 0,
    "shipping_incl_tax": 10,
    "shipping_tax_amount": 0,
    "store_currency_code": "USD",
    "store_id": 1,
    "store_to_base_rate": 0,
    "store_to_order_rate": 0,
    "subtotal": 9180,
    "subtotal_incl_tax": 9180,
    "tax_amount": 0,
    "total_due": 9190,
    "total_qty_ordered": 2,
    "weight": 1.5,
    "shipping_method": "flatrate_flatrate",
    "state": "new",
    "status": "pending",
    "store_name": "Main Website\r\nMain Website Store\r\nDefault Store View",
    "total_item_count": 2,
    "protect_code": "62ef31f388160d69ee03991765ae1b52",
    "entity_id": "1",
    "id": "1",
    "created_at": "2018-11-10 04:35:13",
    "updated_at": "2018-11-10 04:35:13"
}
```