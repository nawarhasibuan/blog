# Blog Content

Repository untuk menyimpan konten blog personalku.

###### Daftar Isi

- [Overview](#overview)
- [Struktur Folder](#struktur-folder)
- [Pemanggilan](#pemanggilang-api-github)

## Overview

Semua konten ditulis dalam `markdown` mengikuti `syntax` pada `ReactMarkdown`

## Struktur Folder

Konten dikelompokkan dalam folder seperti berikut:

```
📦blog
 ┣ 📂opini
 ┃ ┗ 📜*.md
 ┣ 📂pembelajaran
 ┃ ┣ 📂informatika
 ┃ ┃ ┗ 📂{nama bab}
 ┃ ┃ ┃ ┗ 📜*.md
 ┃ ┗ 📂matematika
 ┃ ┃ ┗ 📂{nama bab}
 ┃ ┃ ┃ ┗ 📜*.md
 ┣ 📂soal
 ┃ ┣ 📂aljabar
 ┃ ┃ ┗ 📜*.md
 ┃ ┣ 📂aritmatika
 ┃ ┃ ┗ 📜*.md
 ┃ ┣ 📂kombinatorika
 ┃ ┃ ┗ 📜*.md
 ┃ ┣ 📂osn
 ┃ ┃ ┣ 📂informatika
 ┃ ┃ ┃ ┣ 📂{tahun}
 ┃ ┃ ┃ ┃ ┗ 📜osk*.md
 ┃ ┃ ┃ ┃ ┗ 📜osp*.md
 ┃ ┃ ┃ ┃ ┗ 📜osn*.md
 ┃ ┃ ┗ 📂matematika
 ┃ ┃ ┃ ┣ 📂{tahun}
 ┃ ┃ ┃ ┃ ┗ 📜osk*.md
 ┃ ┃ ┃ ┃ ┗ 📜osp*.md
 ┃ ┃ ┃ ┃ ┗ 📜osn*.md
 ┃ ┣ 📂pemrograman
 ┃ ┃ ┗ 📜*.md
 ┃ ┣ 📂utbk
 ┃ ┃ ┗ 📜*.md
 ┣ 📂travel
 ┃ ┗ 📜*.md
 ┣ 📂waris
 ┃ ┗ 📜*.md
 ┗ 📜README.md
```

## Pemanggilang API GitHub

Sesuai dengan [API](https://docs.github.com/en/rest/repos/contents) yang disediakan oleh github

Gunakan

```
application/vnd.github.raw
```

`GET` method

```c
curl -L \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: Bearer <YOUR-TOKEN>"\
  -H "X-GitHub-Api-Version: 2022-11-28" \
  https://api.github.com/repos/OWNER/REPO/contents/PATH
```

`PUT` method

```js
// Octokit.js
// https://github.com/octokit/core.js#readme
const octokit = new Octokit({
  auth: "YOUR-TOKEN",
});

await octokit.request("PUT /repos/{owner}/{repo}/contents/{path}", {
  owner: "OWNER",
  repo: "REPO",
  path: "PATH",
  message: "my commit message",
  committer: {
    name: "Monalisa Octocat",
    email: "octocat@github.com",
  },
  content: "bXkgbmV3IGZpbGUgY29udGVudHM=",
  headers: {
    "X-GitHub-Api-Version": "2022-11-28",
  },
});
```
