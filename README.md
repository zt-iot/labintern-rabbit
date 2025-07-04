# 研究室インターン＠五十嵐研
Rabbit を使ってみる

## DNSを書いてみた

```
dns
| - dns.rab
| - secure_dns.rab
```

- `dns.rab` は普通のDNSをモデル化したもの
- `secure_dns.rab` DoHとDNSSECのモデルを追加

攻撃は以下のことを行うと想定
- クライアントやキャッシュサーバーが受け取るメッセージを改ざん
- クライアントのクエリを覗き見

`dns.rab` では攻撃が成功するが，DoHとDNSSECを追加した `secure_dns.rab` では攻撃が失敗することを確認．