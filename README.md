# Google Hacking Database (GHDB) Cheat Sheet

This cheat sheet contains common Google dorks and search operators to help you gather information for ethical hacking and security research purposes. **Use responsibly and legally**.

---

## 📌 Basic Search Operators

| Operator                 | Description                                | Example                        |
|--------------------------|--------------------------------------------|--------------------------------|
| `"keyword"`               | Search for an exact phrase                 | `"admin login page"`           |
| `OR`                     | Logical OR (either term)                   | `php OR laravel tutorials`     |
| `-`                      | Exclude a term                             | `security -policy`             |
| `*`                      | Wildcard (any word)                        | `"error * line"`               |



## 📌 Advanced Search Operators

| Operator                 | Description                                | Example                                        |
|--------------------------|--------------------------------------------|------------------------------------------------|
| `site:`                  | Restrict to a specific site or domain      | `site:example.com`                             |
| `intitle:`               | Search within the title                    | `intitle:"index of /admin"`                    |
| `inurl:`                 | Search within the URL                      | `inurl:admin`                                  |
| `filetype:`              | Search for specific file types             | `filetype:pdf "security policies"`             |
| `intext:`                | Search within the page body text           | `intext:"error database"`                      |


## 📌 Narrowing Search Results

| Operator                 | Description                                | Example                                        |
|--------------------------|--------------------------------------------|------------------------------------------------|
| `cache:`                 | View the cached version of a page          | `cache:example.com`                            |
| `related:`               | Find sites related to a domain             | `related:example.com`                          |
| `define:`                | Get definitions for a word or phrase       | `define:SQL injection`                         |
| `link:`                  | Find sites linking to a specific URL       | `link:example.com`                             |



## 📌 Combining Operators

| Operator                 | Description                                | Example                                        |
|--------------------------|--------------------------------------------|------------------------------------------------|
| `allintitle:`            | Search multiple words in the title         | `allintitle:admin login page`                  |
| `allinurl:`              | Search multiple words in the URL           | `allinurl:admin login`                         |
| `allintext:`             | Search multiple words in the page text     | `allintext:database username password`         |



## 📌 Time-Specific Search

| Operator                 | Description                                | Example                                        |
|--------------------------|--------------------------------------------|------------------------------------------------|
| `daterange:`             | Search within a specific date range        | `daterange:2458834-2458844 "data breach"`      |
| **Note:**                | Use the **Tools** menu for time filtering  | N/A                                            |



## 📌 Common Dorks for Sensitive Information

### 🔒 Exposing Sensitive Directories

| Dork                                | Purpose                                     |
|-------------------------------------|---------------------------------------------|
| `intitle:"index of" "admin"`        | Finds directories containing admin files    |
| `intitle:"index of" "password"`     | Locates directories with password files     |
| `intitle:"index of" "backup"`       | Finds backup directories                    |

### 🔑 Finding Passwords

| Dork                                | Purpose                                     |
|-------------------------------------|---------------------------------------------|
| `intext:"DB_PASSWORD" filetype:env` | Finds exposed environment files with passwords |
| `inurl:"wp-config.php"`             | Searches for WordPress config files         |
| `filetype:sql "password"`           | Finds SQL files with sensitive data         |

### 🖥 Discovering Login Portals

| Dork                                | Purpose                                     |
|-------------------------------------|---------------------------------------------|
| `intitle:"login" "admin"`           | Finds admin login portals                   |
| `inurl:admin/login`                 | Searches for admin login URLs               |
| `intitle:"admin panel" "login"`     | Exposes various admin panels                |

### 🔍 Finding Vulnerable Devices

| Dork                                | Purpose                                     |
|-------------------------------------|---------------------------------------------|
| `inurl:"ViewerFrame?Mode="`         | Accesses unsecured IP cameras               |
| `intitle:"webcamXP 5"`              | Finds webcams running webcamXP 5            |
| `inurl:":10000" intitle:"Webmin"`   | Locates Webmin admin interfaces             |



## 📌 Files Containing Juicy Info

| Dork                                | Purpose                                     |
|-------------------------------------|---------------------------------------------|
| `filetype:log inurl:"/logs/"`       | Finds log files that may contain sensitive info |
| `filetype:bak inurl:"/backup/"`     | Locates backup files                       |



## 📌 Finding SQL Injection Vulnerabilities

| Dork                                | Purpose                                     |
|-------------------------------------|---------------------------------------------|
| `inurl:index.php?id=`               | Identifies URLs prone to SQL injection      |
| `inurl:".php?id=" "You have an error in your SQL syntax"` | Finds SQL errors, indicating vulnerability |
| `inurl:".php?id=" "mysql_fetch_array()"` | Searches for pages showing MySQL errors   |



## ⚠️ **Disclaimer:**
This cheat sheet is intended for **ethical hacking and educational purposes** only. Always ensure you have permission before performing any actions on a website. Unauthorized access is illegal.



## 📚 **Resources:**
- [Exploit-DB Google Hacking Database](https://www.exploit-db.com/google-hacking-database)
- [Google Advanced Search](https://www.google.com/advanced_search)

---

**Stay safe, stay ethical!**