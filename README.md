# Create_DNS_Server_Container
DNSサーバをDockerコンテナとして作成する。

- [Create_DNS_Server_Container](#create_dns_server_container)
  - [コマンド](#コマンド)
    - [コンテナ起動](#コンテナ起動)
    - [動作確認](#動作確認)
  - [参考](#参考)

## コマンド

### コンテナ起動

```
docker-compose up -d
```

### 動作確認

```
curl www.google.co.jp --dns-servers 127.0.0.1
```
※ --dns-serversオプションはDebian, Ubuntu用ビルドcurlバイナリに含まれていない。



## 参考

- [DockerでDnsmasqを使った内部DNSサーバを構築するメモ](https://7me.nobiki.com/2020/04/22/dnsmasq-docker-memo/)
  - 何だこれ。ちょう簡単じゃん・・・
- [闘うITエンジニアの覚え書き:cURLメモ](https://www.magata.net/memo/index.php?cURL%A5%E1%A5%E2#x66a3dc9)
  - curlでDNSサーバを指定する方法
- [](https://www.it-swarm-ja.tech/ja/networking/dns%E3%82%AA%E3%83%97%E3%82%B7%E3%83%A7%E3%83%B3%E3%82%92%E4%BD%BF%E7%94%A8%E3%81%97%E3%81%A6curl%E3%82%92%E5%AE%9F%E8%A1%8C%E3%81%99%E3%82%8B%E9%9A%9B%E3%81%AE%E5%95%8F%E9%A1%8C/997990830/)
  - curlのオプションが効かない
- [Qiita:Dockerコンテナ上にdns環境を構築する](https://qiita.com/hakaicode/items/478ba39055c101d6197d)
