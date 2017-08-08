# neo4j4nwconf
Manage network configration using neo4j

## how to use
sample_queryをneo4jにコピペで貼り付ける

## 構成確認コマンド例
 * 全体構成：MATCH (s) RETURN s
 * SW-SW接続：MATCH (s)-[:HAVE]-(m)-[:SW_SW]-(n)-[:HAVE]-(l) RETURN s,m,n,l
 * SV-SW接続：MATCH (s)-[:HAVE]-(m)-[:SV_SW]-(n)-[:HAVE]-(l) RETURN s,m,n,l
 * 個別構成：MATCH (s {name:'tenant01★ここにSW/サーバ名を記載'})-[:HAVE]-(m)-[:SV_SW]-(n)-[:HAVE]-(l) RETURN s,m,n,l
 * DB全削除：MATCH (n) OPTIONAL MATCH (n)-[r]-() DELETE n,r
