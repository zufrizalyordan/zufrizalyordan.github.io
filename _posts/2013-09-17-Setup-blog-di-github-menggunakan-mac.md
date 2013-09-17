---
layout: post
title: Setup blog di github menggunakan Mac
categories : [jekyll, bootstrap, github]
tags : [setup, beginner/intermediate]
---

Kebutuhan :
+ Terminal
+ Account di Github
+ Ruby > 1.9 
  apabila belum punya ruby atau versi di komputer anda di bawah 1.9, silahkan kunjungi [https://www.ruby-lang.org/en/downloads/](https://www.ruby-lang.org/en/downloads/) dan ikuti langkah untuk Ruby for Mac.

Level :
+ beginner - intermediate


1. login ke account Github
2. buat repo sesuai nama username
  misal username anda adalah namarepoanda, maka bikin repo dengan nama namarepoanda.github.com
3. supaya lebih praktis dalam pengecekan di local, bisa install Jekyll-Bootstrap
  
  » clone jekyll-bootstrap.git sesuai dengan repo anda namarepoanda.github.io
    <pre><code>git clone https://github.com/plusjade/jekyll-bootstrap.git namarepoanda.github.io</code></pre>
  » masuk ke namarepoanda
    <pre><code>cd namarepoanda.github.io</code></pre>
  » set repo local untuk menunjuk repo remote
    <pre><code>git remote set-url origin git@github.com:NamaUserGitHubAnda/namarepoanda.github.io.git</code></pre>
  » upload file Jekyll-Bootstrap di local ke repo namarepoanda.github.io
    <pre><code>git push origin master</code></pre>

apabila sudah berhasil instalasi Jekyll-Bootstrap, buka Terminal
ketik : <pre><code>jekyll serve</code></pre>

buka browser dan ketik 
<pre><code>http://localhost:4000</code></pre>

apabila ada halaman yang tampil, selamat anda berhasil!

~zy

