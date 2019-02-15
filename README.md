---
code_name: TM-W_MARK-COLLAB_WEB_VUE_TSC_PART
create_date: 2017-06
author: TM
author_site: timsmanter.net
editor: Visual Studio Code
language: [C#, TypeScript]
framework: [.NET Core, ASP.NET Core, Entity Framework Core, Vue.js]
locale: en_US
license: MIT
status: [Dev, Sample]
---

# MarkCollab Editor

- [Overview](#overview)
- [Screenshots](#screenshots)
- [API Reference](#api-reference)
  - [Get all documents](#get-all-documents)
  - [Get single document of {id}](#get-single-document-of-id)
  - [Create new document with title in body](#create-new-document-with-title-in-body)
  - [Update document content in body](#update-document-content-in-body)
  - [Update document title in body](#update-document-title-in-body)
  - [Delete document of {id}](#delete-document-of-id)

## Overview

MarkCollab is a simple collaboration tool for creating various types of documents using Markdown syntax. The main idea is to create a self-hosted Web Application that contains everything to create Markdown documents by many people in the same time.

## Screenshots

![Editor View](docs/screenshots/editor.png)
![Sidenav](docs/screenshots/sidenav.png)

## API Reference

### Get all documents
```http
GET {root}/api/docs
```

### Get single document of {id}
```http
GET {root}/api/docs/{id}
```

### Create new document with title in body
```http
POST {root}/api/docs
```
> Note: Remember to add `Content-Type: text/plain` header.

### Update document content in body
```http
PATCH {root}/api/docs/{id}/content
```
> Note: Remember to add `Content-Type: text/plain` header.

### Update document title in body
```http
PATCH {root}/api/docs/{id}/title
```
> Note: Remember to add `Content-Type: text/plain` header.

### Delete document of {id}
```http
DELETE {root}/api/docs/{id}
```