  systemctl start hysteria-client     # включить VPN
  systemctl stop hysteria-client      # выключить VPN
  systemctl restart hysteria-client   # перезапустить, например после нового обхода в NM
  systemctl status hysteria-client    # состояние

  Проверить, что трафик идет через VPN:
  curl https://api.ipify.org          # должно быть 95.214.8.243