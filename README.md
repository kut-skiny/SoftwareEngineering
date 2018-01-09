# SoftWareEngineering
安否確認システム  
# クローン方法など  
以下のサイトを参考にしてください。不安なら澤田まで。  
<https://seleck.cc/630>
# 注意点
作業は各ブランチで行い、masterブランチでは作業をしないでください。  
ブランチの作成方法を下に書いておきます。  
branchの作成  
`git branch [branch名]`  
branchの切り替え  
`git checkout [branch名]`  
branchのプッシュ  
`git push -u origin [branch名]`  
各ブランチの作業をmasterブランチに反映させたい場合はPull Requestをおこなってください.  
# masterブランチの変更を自分のブランチに反映させる
　　　　git checkout [自分のブランチ名]  
　　　　git checkout master  
　　　　git pull  
　　　　git checkout [自分のブランチ名]  
　　　　git merge master  

# ローカル環境のmysqlにデータベースの設定を反映させる
本システム用のデータベースを作成。データベース名は'mimic'とする。なお、予めmysqlは起動しておく。  
`$ mysql -u root`  
`mysql-> create database mimic;`  
`mysql-> quit;`  
カレントディレクトリを'SoftWareEngineering/db'にし、sqlファイルを実行する。  
`$ mysql -u root mimic < mimic_db_create.sql`
# mysqlに初期データを流し込む
初期データを挿入する。ただし、元あるレコードはすべて削除される。なお、予めmysqlは起動しておく。  
カレントディレクトリを'SoftWareEngineering/db'にし、sqlファイルを実行する。 
`$ mysql -u root mimic < mimic_db_initialize.sql`