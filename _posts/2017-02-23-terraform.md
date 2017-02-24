---
layout: post
title:  Terraform
date:   2017-02-23 22:20:58 +1100
categories: blog
---

Organise your infrastructure with terraform

* [How to create reusable infrastructure with Terraform modules](https://blog.gruntwork.io/how-to-create-reusable-infrastructure-with-terraform-modules-25526d65f73d#.yvnibcfvn)
* [How to manage Terraform state](https://blog.gruntwork.io/how-to-manage-terraform-state-28f5697e68fa#.h342o6cbd)

But [HIL/HCL](https://www.terraform.io/docs/configuration/interpolation.html) is somehow limited

* [Support for nested maps in variables #2114](https://github.com/hashicorp/terraform/issues/2114)
* [Type system to support list and map element types](https://github.com/hashicorp/hil/pull/42)
* [Intermediate variables (OR: add interpolation support to input variables)](https://github.com/hashicorp/terraform/issues/4084)
  * Use `null_data_source`
* ~~[Can't create an output map](https://github.com/hashicorp/terraform/issues/8153#issuecomment-239548132)~~
