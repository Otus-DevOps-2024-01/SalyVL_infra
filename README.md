# SalyVL_infra

Alias configuration ~/.ssh/config

Host someinternalhost
    HostName 10.128.0.29
    User appuser
    IdentityFile ~/.ssh/appuser
    ProxyJump appuser@178.154.205.20

Host bastion
	Hostname 178.154.205.20
	User appuser
	IdentityFile ~/.ssh/appuser

ssh someinternalhost
ssh bastion

bastion_IP = 178.154.205.20
someinternalhost_IP = 10.128.0.29
