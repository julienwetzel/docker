# Utiliser une image de base légère
FROM alpine:latest

# Mettre à jour les paquets et installer vsftpd
RUN apk update && apk add --no-cache vsftpd

# Ajouter un fichier de configuration pour vsftpd
COPY vsftpd.conf /etc/vsftpd/vsftpd.conf

# Exposer le port FTP standard
EXPOSE 21

# Lancer vsftpd au démarrage du conteneur
CMD ["/usr/sbin/vsftpd", "/etc/vsftpd/vsftpd.conf"]
