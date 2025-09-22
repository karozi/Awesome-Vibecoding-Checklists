# 🧰 curl Cheat Sheet for Product Builders

> **curl**: Command-line tool for transferring data to and from servers using URLs.  
> Use for API testing, automations, web scraping, downloads, uploads, and more.
>
> Copy, remix, and share - **[Product with Attitude](https://karozieminski.substack.com/)** loves a shoutout.

---

## 🚦 Table of Contents

1. [Basic GET Request](#1-basic-get-request)
2. [GET Request With Headers](#2-get-request-with-headers)
3. [GET With Query Parameters](#3-get-with-query-parameters)
4. [POST Request With JSON Body](#4-post-request-with-json-body)
5. [PUT/PATCH Request (Update Data)](#5-putpatch-request-update-data)
6. [DELETE Request](#6-delete-request)
7. [Download a File](#7-download-a-file)
8. [Upload a File (multipart/form-data)](#8-upload-a-file-multipartform-data)
9. [Verbose Output (Debug)](#9-verbose-output-debug)
10. [Save Output to a File](#10-save-output-to-a-file)
11. [Follow Redirects](#11-follow-redirects)
12. [Custom HTTP Methods](#12-custom-http-methods)
13. [Download With Progress Bar](#13-download-with-progress-bar)
14. [Send Data as Form URL Encoded](#14-send-data-as-form-url-encoded)
15. [Set a Custom User-Agent](#15-set-a-custom-user-agent)
16. [Include Cookies](#16-include-cookies)
17. [Show Only Response Headers](#17-show-only-response-headers)
18. [Save and Reuse Cookies](#18-save-and-reuse-cookies)
19. [Download Multiple Files](#19-download-multiple-files)
20. [Timeouts (Limit Wait Time)](#20-timeouts-limit-wait-time)
21. [🧠 Pro Tips](#-pro-tips)

---

## 1. Basic GET Request

```bash
curl https://api.example.com/endpoint
```
**When to use:**  
- Test if a site or API is responding  
- Quick “is this up?” checks  

---

## 2. GET Request With Headers

```bash
curl -H "Authorization: Bearer <token>" https://api.example.com/private
```
**When to use:**  
- Access endpoints requiring API keys or tokens  
- Simulate authenticated requests

---

## 3. GET With Query Parameters

```bash
curl "https://api.example.com/users?role=admin&active=true"
```
**When to use:**  
- Fetch filtered, searched, or paginated data

---

## 4. POST Request With JSON Body

```bash
curl -X POST -H "Content-Type: application/json" \
  -d '{"name":"Karo","role":"PM"}' \
  https://api.example.com/users
```
**When to use:**  
- Create resources (users, tasks, posts) via API  
- Test “create” endpoints

---

## 5. PUT/PATCH Request (Update Data)

```bash
curl -X PUT -H "Content-Type: application/json" \
  -d '{"role":"Bestseller"}' \
  https://api.example.com/users/123
```
**When to use:**  
- Update or edit existing data  
- Patch user profiles, settings, etc.

---

## 6. DELETE Request

```bash
curl -X DELETE https://api.example.com/users/123
```
**When to use:**  
- Remove a resource (user, post, etc.)  
- Test delete endpoints (with care!)

---

## 7. Download a File

```bash
curl -O https://example.com/report.pdf
```
**When to use:**  
- Save a file from a URL  
- Retain original filename

---

## 8. Upload a File (multipart/form-data)

```bash
curl -X POST -F "file=@/path/to/yourfile.png" https://api.example.com/upload
```
**When to use:**  
- Test file upload endpoints  
- Simulate image/doc uploads

---

## 9. Verbose Output (Debug)

```bash
curl -v https://api.example.com
```
**When to use:**  
- Debug API requests  
- See full request/response headers

---

## 10. Save Output to a File

```bash
curl https://example.com/data.csv -o data.csv
```
**When to use:**  
- Download and name files directly

---

## 11. Follow Redirects

```bash
curl -L https://bit.ly/some-link
```
**When to use:**  
- Handle shortened/redirected links (e.g. Bitly, 301/302)

---

## 12. Custom HTTP Methods

```bash
curl -X PATCH https://api.example.com/endpoint
```
**When to use:**  
- Use non-standard methods (PATCH, OPTIONS, etc.)

---

## 13. Download With Progress Bar

```bash
curl -# -O https://largefile.zip
```
**When to use:**  
- Visualize download progress for large files

---

## 14. Send Data as Form URL Encoded

```bash
curl -X POST -d "name=Karo&role=AI+PM" https://api.example.com/submit
```
**When to use:**  
- Simulate HTML form submissions

---

## 15. Set a Custom User-Agent

```bash
curl -A "ProductWithAttitudeBot/1.0" https://api.example.com
```
**When to use:**  
- Mimic browsers/bots  
- Test bot detection

---

## 16. Include Cookies

```bash
curl --cookie "sessionid=abcd1234" https://api.example.com/profile
```
**When to use:**  
- Simulate logged-in user sessions

---

## 17. Show Only Response Headers

```bash
curl -I https://api.example.com
```
**When to use:**  
- Check server headers  
- Test CORS, content type, etc.

---

## 18. Save and Reuse Cookies

```bash
curl -c cookies.txt -b cookies.txt https://api.example.com
```
**When to use:**  
- Persist sessions across multiple requests

---

## 19. Download Multiple Files

```bash
curl -O https://example.com/file1.jpg -O https://example.com/file2.jpg
```
**When to use:**  
- Download several files at once

---

## 20. Timeouts (Limit Wait Time)

```bash
curl --max-time 10 https://api.example.com/slow-endpoint
```
**When to use:**  
- Prevent curl from hanging forever on slow APIs

---

## 🧠 Pro Tips

- Use `curl` to debug APIs, reproduce bugs, and automate content ops.
- Add `-v` for verbose (debug), `-L` to follow redirects, and `-o <file>` to save output.
- For OAuth/JWT-protected APIs, always pass the correct `Authorization` header.
- Wrap common curl calls into shell scripts for repeatable workflows.

---

