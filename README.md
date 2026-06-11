name: Apple 国际特性解锁覆写
desc: 解锁 Apple Intelligence, Apple News, Siri 海外版, 罗盘经纬度及 iCloud 闸道代理
rules:
  # 1. Apple Intelligence & Siri 核心分流
  - DOMAIN-SUFFIX,apple-relay.apple.com,PROXY
  - DOMAIN-SUFFIX,gateway.icloud.com,PROXY
  - DOMAIN-SUFFIX,smoot.apple.com,PROXY
  - DOMAIN-SUFFIX,apple.news,PROXY
  - DOMAIN-SUFFIX,appleintelligence.apple,PROXY
  - DOMAIN-SUFFIX,apple-relay.cloudflare.com,PROXY
  - DOMAIN-SUFFIX,cp4.cloudflare.com,PROXY
  - DOMAIN-SUFFIX,gspe1-ssl.ls.apple.com,PROXY
  - DOMAIN-SUFFIX,apps.mzstatic.com,PROXY

  # 2. Apple News 核心分流
  - DOMAIN-SUFFIX,apple.news,自动选择
  - DOMAIN-SUFFIX,news-edge.apple.com,自动选择
  - DOMAIN-SUFFIX,news-events.apple.com,自动选择

  # 3. iCloud 闸道与地理位置判定（减少中国特征的关键）
  - DOMAIN-SUFFIX,gateway.icloud.com,自动选择
  - DOMAIN-SUFFIX,configuration.ls.apple.com,自动选择
  - DOMAIN-SUFFIX,gs-loc.apple.com,自动选择
  - DOMAIN-SUFFIX,gspe1-ssl.ls.apple.com,自动选择

  # 4. 其他相关增强
  - DOMAIN-SUFFIX,cp4.cloudflare.com,自动选择
  - DOMAIN-SUFFIX,apps.mzstatic.com,自动选择
