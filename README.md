# FileEncryption
基于3DES、blowfish、MD5的文件加密/解密系统

使用：
1、选择待加密的文件；
2、选择加密方式：单一加密方式/两次加密方式
3、执行加密

说明：
一次加密可以分别采用3DES或者blowfish，连续加密采用先3DES后blowfish的方式

存在问题：
1、3DES加密与blowfish不匹配；
2、MD5校验值追加到密文尾部并不合理；
3、采用两次加密时，在解密时解密顺序需要与加密相反。

待改善：
1、秘钥保存方式修改，可增加MySQL存储；
2、两次加密方式混合成单一的加密比较好；
3、优化代码，提升速度，尽量采用多线程或者进行数据分割优化。
