name: Apple 国际特性解锁覆写
desc: 解锁 Apple Intelligence, Apple News, Siri 海外版, 罗盘经纬度及 iCloud 闸道代理
rules:
  # 1. Apple Intelligence & Siri 核心分流
DOMAIN-SUFFIX,apple-relay.apple.com,PROXY
DOMAIN-SUFFIX,gateway.icloud.com,PROXY
DOMAIN-SUFFIX,smoot.apple.com,PROXY
DOMAIN-SUFFIX,apple.news,PROXY
DOMAIN-SUFFIX,appleintelligence.apple,PROXY
DOMAIN-SUFFIX,apple-relay.cloudflare.com,PROXY
DOMAIN-SUFFIX,cp4.cloudflare.com,PROXY
DOMAIN-SUFFIX,gspe1-ssl.ls.apple.com,PROXY
DOMAIN-SUFFIX,apps.mzstatic.com,PROXY
