# aws-cf-stack

## 概要
AWSのCloudFormationStackを管理するリポジトリ。  

## NW
* vpc.yml  
VPCを作成し、パブリックサブネットとプライベートサブネットをそれぞれ2つ作る。  
* nat_ec2.yml
NATインスタンスを作成し、プライベートのルートテーブルの`0.0.0.0/0`の経路として登録する。  
* public_single_ec2.yml  
パブリックサブネットにec2を1つ作り、Elastic IPをアタッチする。  
`ssh -i my-ec2-key.pem ec2-user@ElasticIP`で接続。
* private_single_ec2.yml  
プライベートサブネットにec2を1つ作る。  
