# wsgi_app
Test project to build a simple python application and deploy it on windows server with apache and mod_wsgi.

Everything is 32-bit, and more specifically...

 - Python 2.7.9
 - Apache 2.2
 - Windows Server 2012

Referenced https://github.com/GrahamDumpleton/mod_wsgi/blob/master/win32/README.rst to be sure I used the correct pre-compiled binary for my environment

The  the latest windows binaries (as of today) are downloaded from here: https://github.com/GrahamDumpleton/mod_wsgi/releases/tag/4.4.6

The appropriate mod_wsgi.so for my environment is then taken from "mod_wsgi-windows-4.4.6\Apache22-win32-VC9\modules\mod_wsgi-py27-VC9.so" and saved locally in "C:\Apache22\modules" where it is referenced in httpd.conf via `LoadModule wsgi_module modules/mod_wsgi-py27-VC9.so`.

Run apache, and the application displays text in the browser as expeceted.

`$ httpd.exe -e debug` is helpful for debugging