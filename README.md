# OpenVPN-Server-Client-Setup

# 🔐 OpenVPN Server-Client Setup | Configuration VPN Sécurisé

## 📋 Description
Mise en place d'un tunnel VPN sécurisé entre un serveur Kali Linux et un client Windows avec OpenVPN.
Ce projet démontre la configuration complète d'une infrastructure PKI (Public Key Infrastructure), 
la génération de certificats SSL/TLS, et l'établissement d'une connexion VPN chiffrée.

## 🛠️ Technologies utilisées
- **Serveur** : Kali Linux, OpenVPN, Easy-RSA
- **Client** : Windows 10/11, OpenVPN GUI
- **Chiffrement** : SSL/TLS avec authentification mutuelle
- **Protocole** : UDP sur port 1194

## ✅ Fonctionnalités implémentées
✔️ Infrastructure PKI complète (CA, certificats serveur/client)
✔️ Tunnel VPN routé (interface tun) avec sous-réseau dédié (10.8.0.0/24)
✔️ Chiffrement des communications avec TLS-Auth
✔️ Configuration NAT/Masquerading pour routage inter-réseaux
✔️ Tests de connectivité et validation du tunnel



## 🚀 Étapes clés du projet
1. **Initialisation PKI** : Génération de l'autorité de certification (CA)
2. **Certificats** : Création des certificats serveur/client + clé TLS-Auth
3. **Configuration serveur** : Fichier `server.conf` avec routage et NAT
4. **Configuration client** : Fichier `client.ovpn` + transfert des certificats
5. **Tests** : Validation du tunnel VPN (ping 10.8.0.1 → SUCCESS)

## 📸 Résultats
- ✅ Connexion établie avec succès
- ✅ Attribution IP VPN : 10.8.0.2 (client) ↔ 10.8.0.1 (serveur)
- ✅ État : `CONNECTED, SUCCESS`
- ✅ Communication chiffrée bidirectionnelle validée

## 🔧 Configuration technique
### Serveur (Kali Linux)
- Interface virtuelle : `tun0`
- Réseau VPN : `10.8.0.0/24`
- Port : UDP 1194
- Routage : Activation IP forwarding + iptables

### Client (Windows)
- Certificats : ca.crt, client1.crt, client1.key, ta.key
- Protocole : UDP
- Persistance de connexion activée

## 📚 Compétences démontrées
- Administration système Linux
- Sécurité réseau (VPN, chiffrement SSL/TLS)
- Gestion d'infrastructure PKI
- Configuration firewall (iptables)
- Debugging et troubleshooting réseau

## 👤 Auteur
**Chaimae Bouassab**  
Master Sécurité IT & Big Data | Université Abdelmalek Essaadi  

