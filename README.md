##  PHP Vulnerability Hunting Cheat Sheet

A quick reference for identifying common vulnerability patterns during source code review and bug hunting.

---

###  1. User Input Sources

```php
$_GET
$_POST
$_REQUEST
$_COOKIE
$_FILES
$_SERVER
php://input
```

---

###  2. XSS Sinks

```php
echo
print
printf
print_r
die
exit
<?= ?>
```

---

###  3. Command Execution (RCE)

```php
exec
system
shell_exec
passthru
popen
proc_open
```

---

###  4. Code Execution

```php
eval
assert
create_function
preg_replace
```

---

###  5. File Inclusion / Deletion

```php
include
include_once
require
require_once
unlink
```

---

###  6. File Upload Handling

```php
move_uploaded_file
```

---

###  7. SSRF

```php
file_get_contents
curl_exec
curl_multi_exec
```

##  Goal

Use this checklist during:

* Source code review
* Local CVE hunting
* Bug bounty reconnaissance

---
