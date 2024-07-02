# ec2-node-bootstrapper

## Commands

### Update

- Update instance

```
sudo yum update -y
```

### Setup routing

- Install iptables

```
sudo yum install iptables
```

- port forwarding

```
sudo iptables -t nat -A PREROUTING -p tcp --dport 80 -j REDIRECT --to-ports 3000
```

- Open ports

```
sudo iptables -A INPUT -p tcp -m tcp --sport 80 -j ACCEPT
sudo iptables -A OUTPUT-p tcp -m tcp --Dport 80 -j ACCEPT
```

### Install Node and express server

- Download and install Node version manager

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
source ~/.bashrc
```

- Install npm

```
nvm install --lts
node -e "console.log('Running Node.js ' + process.version)"
```

- Install express

```
npm i -g express
```

### install git

```
sudo yum install git -y
```

### Clone project

git clone https://github.com/arongas/ec2-node-bootstrapper.git
cd node-js-sample
npn install
npm start


### Code creation
npm install -g express-generator
express ec2-node-bootstrapper
SET DEBUG=ec2-node-bootstrapper:* & npm start