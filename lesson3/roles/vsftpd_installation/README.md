Role Name - vsftpd_installation
=========

Роль устанавливает и включает FTP (пакет vsftpd) с анонимным доступом в каталог /var/ftp/pub и возможностью записи в /var/ftp/pub/upload
Устанавливает SELinux контекст ftpd_anon_write в значение on, назначает public_content_rw_t на каталог /var/ftp/pub/upload.


Role Variables
--------------

# vars for vsftpd.conf
anonymous_enable: YES
local_enable: NO
write_enable: YES
anon_upload_enable: YES
anon_root: /var/ftp
vsftpd_config: /etc/vsftpd/vsftpd.conf
upload_dir: /var/ftp/pub/upload

# vars for configure selinux context for /var/ftp/pub/upload
context: public_content_rw_t


Author Information
------------------

Aleksandr Iashin
