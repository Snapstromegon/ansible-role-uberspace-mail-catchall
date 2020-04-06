# Ansible Role: uberspace-mail-catchall

This is part of the uberspace roles collection.

This is meant to be used on your [Uberspace](https://uberspace.de/).

Please be aware, that I'm neither part of the Uberspace team, nor am I associated to them other than having some Uberspaces myself.
This project was created, because I wanted to use the roles for myself and thought they were okay-ish enough to share them.


## What is this (from the uberspace manual)

A catch-all mailbox will “catch all” of the emails addressed to the domains on your account that do not exist in the mail server - this can help avoid losing emails due to misspelling. Without a catch-all mailbox these mails will get rejected by the server.

You can find the documentation of the replaced tool `uberspace mail catchall` in the Uberspace Manual [here](https://manual.uberspace.de/mail-mailboxes.html#catch-all-mailbox).

## Usage

| Variable | Choices/Default                            | Description                                              |
| :------: | :----------------------------------------- | :------------------------------------------------------- |
|   user   |                                            | The mailbox user to use as catchall                      |
|  state   | <ul><li>present ✔</li><li>absent</li></ul> | "present" to enable the catchall, "absent" to disable it |

## Examples

### Enable Catchall

```yaml
- hosts: uberspace
  roles:
    - name: uberspace-mail-catchall
      user: post
```

### Disable Catchall

```yaml
- hosts: uberspace
  roles:
    - name: uberspace-mail-catchall
      state: absent
```
