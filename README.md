

Criando um ambiente Big Data na nuvem


Acessar S3: https://s3.console.aws.amazon.com/s3/


Criar estrutura de data lake : dio-live-datalake


Criar estrutura de pastas:

data
output
temp

Acessar EMR: https://console.aws.amazon.com/elasticmapreduce/

O cluster será criado pelo MrJob e não pelo console

Infraestrutura como código

Criar chave SSH

Acessar Console do EC2: https://console.aws.amazon.com/ec2/ -> Key Pairs -> Create Key Pair
Download .pem file

Obter Id e chave secreta AWS para configurar MrJob
Profile
My Security Credentials: https://console.aws.amazon.com/iam/home?region={region}#/security_credentials

Access Keys - Create new access key

Fazer download - única chance de visualizar
Ambiente linux

Criar ambiente virtual python: virtualenv --python=python3.6 venv_diolive
Acessar com o vs code

Instalar vscode no Ubuntu
code .

Criar algoritmo de análise de palavras
dio-live-wordcount-test.py
map-reduce-count : contar
Instalar boto3: pip install boto3
Instalar mrjob: pip install mrjob
Acessar S3
Upload de arquivo para o bucket
Ambiente virtual python: source venv_teste/bin/activate
nano ~/.mrjob.conf
python3 dio-live-wordcount-test.py -r emr s3://{your_s3_bucket_name}/data/SherlockHolmes.txt --output-dir=s3://{your_s3_bucket_name}/output/logs1 --cloud-tmp-dir=s3://{your_s3_bucket_name}/temp/
