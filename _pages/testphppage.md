---
ID: 260
post_title: testphppage
author: admin
post_excerpt: ""
layout: page
permalink: >
  https://findcaringarea.ga/index.php/testphppage/
published: true
post_date: 2018-09-29 05:57:00
---
<?php
if($_REQUEST['unsubscribe'] == 'true'){
    deleteUserMeta($_REQUEST['userID']);
}
?>