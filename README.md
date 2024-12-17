# mod_harbour
modulo Apache para permitir executar a linguagem Harbour 

- Nesse exemplo, o Apache está instalado em C:\APACHE24

- Copiar as dll para c:\apache24\htdocs
- Copiar o arquivo .so para c:\apache24\modules
- Alterar httpd.conf em c:\apache24\config e incluir as linhas no final:

```
LoadModule mod_harbourV2_module modules/mod_harbour.v2.so

MH_LIBRARY c:\\apache24\htdocs\\libmhapache.dll
MH_NVMS 10

<FilesMatch "\.(prg|hrb)$">
    SetHandler harbour
</FilesMatch>
```
