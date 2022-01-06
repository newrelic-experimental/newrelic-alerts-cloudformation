# Next
- Add our Alert definition to `create-ec2-instance.yaml`
- `aws cloudformation update-stack --region us-west-1 --template-body "file://create-ec2-instance.yaml" --stack-name MikesTestStack`

## Shell history getting things going
```shell
cd IdeaProjects/
git clone git@github.com:newrelic/cloudformation-partner-integration.git
cd cloudformation-partner-integration/
ll
mvn clean package
find . -name "cfn*"
cfn
"
grep -R cfn *
less pom.xml 
cfn
aws
aws --version
cd ~/Down
cd ~/Downloads/
ll -tr
tar tzf aws-cfn-bootstrap-py3-latest.tar.gz 
tar xzf aws-cfn-bootstrap-py3-latest.tar.gz 
cd aws-cfn-bootstrap-
cd aws-cfn-bootstrap-2.0/
ll
less setup.py 
chmod +x setup.py 
./setup.py 
./setup.py  --help-commands
./setup.py build install
sudo ./setup.py build install
cd ~/IdeaProjects/
ll -tr
cd cloudformation-partner-integration/
mvn clean install
less pom.xml 
pip install cloudformation-cli cloudformation-cli-java-plugin cloudformation-cli-go-plugin cloudformation-cli-python-plugin cloudformation-cli-typescript-plugin
pip
sudo port install pip
python --version
python3 --version
sudo port install py-pip
pip --version
sudo port select --set pip pip39
sudo port select --set pip3 pip39
pip --version
pip install cloudformation-cli cloudformation-cli-java-plugin cloudformation-cli-go-plugin cloudformation-cli-python-plugin cloudformation-cli-typescript-plugin
mvn clean package
which cfn
echo $PATH
export PATH=$PATH:/System/Volumes/Data/Users/mike/Library/Python/3.9/bin
which cfn
cfn --version
mvn clean package
mvn clean install
mvn clean package
ll
mvn clean
ll
mvn build
mvn generate
mvn generate-resources
mvn generate-sources
ll
ll NrqlAlertCondition/
mvn clean
ll NrqlAlertCondition/
mvn clean package
cfn submit -v --region us-east-2
ll -a
ll -a NrqlAlertCondition/
cd NrqlAlertCondition/
cfn submit -v --region us-east-2
grep -R AWS::AccountId
grep -R AWS::AccountId *
grep -Ri AWS::AccountId *
pwd
grep -Ri AWS::AccountId ../*
ll ..
grep -Ri AccountId ../*
ll -a
less resource-role.yaml 
less .rd
less .rpdk-config 
ll docs/
less docs/README.md 
less newrelic-alerts-nrqlalert.json 
cfn validate
pwd
ll
cfn submit -v --region us-east-2
fimd . -name yml
find . -name yml
find .. -name yml
find .. -name *.yml
find .. -name *.yaml
```

