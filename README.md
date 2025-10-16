# Ansible Role: swap

An Ansible role that deploys and configures a swap file on Linux boxes.

## 🚀 Motivation

Since Linux kernel 2.6, swap files have the same level of performance and reliability that swap partitions. Details can be found [here][01].

Swap files, however, also present the following advantages:

1. The possibility of quickly and easily increasing and decreasing the swap area;
1. A fewer number of partitions on disc, potentially making its administration easier;

## 📑 Role Variables

Check [here][02].

## 🧰 Dependencies

None.

## ⚡ Quick start

An example of how integrate this role to an Ansible playbook can be found here:

```yml
---
- name: Deploy swap file
  hosts: all
  become: true
  gather_facts: true
  roles:
    - fernandobohrer.swap
```

## ⚙️ Compatibility

This role was tested on and is confirmed to work with the following Linux distributions:

- `Debian 13`
- `Ubuntu 24.04`

Details can be found in the [Molecule][03] scenarios available in the `molecule` folder.

## ⚠️ Warning

This Ansible role was tested on the above mentioned Linux distributions considering their default configuration. Your environment might have a different configuration or requirements which might conflict with the options that this role uses.

With the above in mind, it is **imperative** that you familiarize yourself with what this role does and test it on non-production machines **before** applying it to machines in a production environment.

## 📝 License

This project is licensed under the terms of the [MIT license][04].

[01]: https://lkml.org/lkml/2005/7/7/326
[02]: defaults/main.yml
[03]: https://github.com/fernandobohrer/ansible-molecule-scenarios
[04]: /LICENSE
