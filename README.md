# Neova


sudo apt update && sudo apt install -y apt-transport-https ca-certificates curl gnupg lsb-release && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg && echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null && sudo apt update && sudo apt install -y docker-ce docker-ce-cli containerd.io && sudo systemctl start docker && sudo systemctl enable docker


sudo docker pull neovaprotocol/provider && sudo docker run -d --name neova --restart always -e EVM_ADDRESS=evmadres neovaprotocol/provider

screen -S neova

docker logs -f neova




Mevcut Konteyneri Kaldırarak Yeniden Başlatma
Eğer mevcut konteyneri yeniden oluşturmak istiyorsanız, önce onu durdurup silmeniz gerekir:


sudo docker stop neova
sudo docker rm neova
