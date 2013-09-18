---
layout: post
title: Error ketika melakukan php artisan migrate di Laravel 4 pada Mac
categories : [laravel]
tags : [php, beginner]
---

Dalam tutorial Laravel 4, saya mengalami sebuah error dengan menggunakan konfigurasi 
<pre><code>
  'mysql' => array(
      'driver'    => 'mysql',
      'host'      => 'localhost',
      'port'      => '8889',
      'database'  => 'laravel',
      'username'  => 'root',
      'password'  => 'root',
      'charset'   => 'utf8',
      'collation' => 'utf8_unicode_ci',
      'prefix'    => '',
    ),
</code></pre>

error yang muncul adalah : 
![SQLSTATE[HY000] [2003] Can't connect to MySQL server on 'localhost:8889' (4)](http://s22.postimg.org/3vm01jxht/Screen_shot_2013_09_18_at_1_09_52_PM.png "SQLSTATE[HY000] [2003] Can't connect to MySQL server on 'localhost:8889' (4)")


hal ini terjadi ketika saya melakukan migrasi database
<pre><code>php artisan migrate</code></pre> 

setelah membaca beberapa solusi yang sudah disampaikan dari hasil googling, cara yang berhasil untuk saya adalah dengan mengubah konfigurasi menjadi
<pre><code>
  'mysql' => array(
      'driver'    => 'mysql',
      'host'      => '127.0.0.1',
      'port'      => '8889',
      'unix_socket' => '/Applications/MAMP/tmp/mysql/mysql.sock',
      'database'  => 'laravel',
      'username'  => 'root',
      'password'  => 'root',
      'charset'   => 'utf8',
      'collation' => 'utf8_unicode_ci',
      'prefix'    => '',
    ),
</code></pre>

setelah anda melakukan migrasi lagi
<pre><code>php artisan migrate</code></pre> 

jangan lupa untuk mengubah kembali "host" menjadi "localhost"
<pre><code>'host'      => 'localhost'</code></pre>


~zy