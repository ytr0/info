# info



## tailscale

```
# https://sakkuntyo.github.io/2024/02/12/udp-forwarding-tailscale-test/

sudo apt-get install curl
curl -fsSL https://tailscale.com/install.sh | sh
sudo tailscale up --advertise-exit-node

# Allow IPv4 Fowarding
echo 'net.ipv4.ip_forward = 1' | sudo tee -a /etc/sysctl.d/99-tailscale.conf
echo 'net.ipv6.conf.all.forwarding = 1' | sudo tee -a /etc/sysctl.d/99-tailscale.conf
sudo sysctl -p /etc/sysctl.d/99-tailscale.conf


```
