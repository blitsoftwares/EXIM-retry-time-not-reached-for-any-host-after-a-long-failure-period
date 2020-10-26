# EXIM-retry-time-not-reached-for-any-host-after-a-long-failure-period
Mensagem de erro ao enviar email: retry time not reached for any host after a long failure period

Verifique antes se seu servidor não está com problemas no DNS REVERSO.

Caso esteja ok siga as dicas abaixo:

Causa: seus arquivos db do exim estão corrompidos.
Solução:

Vá para

```
/var/spool/exim/db
```

apague os arquivos: ***retry , retry.lockfile , wait-remote_smtp, wait-remote_smtp.lockfile***

```
cd /var/spool/exim/db && rm -rf retry retry.lockfile wait-remote_smtp wait-remote_smtp.lockfile wait-dkim_remote_smtp wait-dkim_remote_smtp.lockfile && ls
```

reinicie o exim

Talvez você tambem tenha que deletar os arquivos das pastas abaixo:
***/var/spool/exim/input***
e
***/var/spool/exim/msglog***

Reinicie o exim.

 

Qualquer dúvida estamos a disposição,

 

Sds.
