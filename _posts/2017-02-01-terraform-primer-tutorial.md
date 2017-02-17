---
layout: post
title:  "Terraform Primer Tutorial"
date:   2017-02-01 00:00:00
categories: [tutorial]
comments: false
---


{% highlight terraform %}
resource "azurerm_storage_account" "test" {
    name = "accsa"
    resource_group_name = "${azurerm_resource_group.test.name}"
    location = "westus"
    account_type = "Standard_LRS"

    tags {
        environment = "staging"
    }
}
{% endhighlight %}

