# 【3】2018年3月品优购电商系统开发
04
	spring-security-demo
05	
	fastDFSdemo
08
	SpringDataRedisDemo
13
	jmsDemo
	springjms_consumer
	springjms_producer
14
	itcast_sms_service
	springBootDemo
15
	casclient_demo1
	casclient_demo2
	casclient_demo3

```mermaid
graph TB
  pojo-->dao
  
  subgraph parent
  parent-->pojo
  parent-->common
  parent-->dao
  end
  
  subgraph page12d
  page-i-->page-s
  dao-->page-s
  end
  
  subgraph pay18c
  pay-i-->pay-s
  common-->pay-s
  end
  
  subgraph search9c
  pojo-->search-i
  search-i-->search-s
  common-->search-s
  search-i-->search-web
  end
  

  subgraph cart16
  pojo-->cart-i
  cart-i-->cart-s
  common-->cart-s
  dao-->cart-s
  end
  
  subgraph content8
  pojo-->content-i
  content-i-->content-s
  common-->content-s
  dao-->content-s
  end
  
  subgraph order17
  pojo-->order-i
  order-i-->order-s
  common-->order-s
  dao-->order-s
  end
  
  subgraph seckill19
  pojo-->seckill-i
  seckill-i-->seckill-s
  common-->seckill-s
  dao-->seckill-s
  end
  
  subgraph sellgoods1
  pojo-->sellgoods-i
  sellgoods-i-->sellgoods-s
  common-->sellgoods-s
  dao-->sellgoods-s
  end
  
  subgraph user14
  pojo-->|pojo-i-s^common,dao|user-i
  user-i-->user-s
  common-->user-s
  dao-->user-s
  end
  
  common-->|cart,order,pay,user|cart-web
  cart-i-->cart-web
  order-i-->cart-web
  pay-i-->cart-web
  user-i-->cart-web
  
  common-->|content,sellgoods|manager-web
  content-i-->manager-web
  sellgoods-i-->manager-web
  
  common-->|content8|portal-web
  content-i-->portal-web
  
  common-->|seckill,pay|seckill-web
  seckill-i-->seckill-web
  pay-i-->seckill-web
  
  common-->|sellgoods4|shop-web
  sellgoods-i-->shop-web
  
  common-->|user|user-web
  user-i-->user-web
  
  common-->task-service
  dao-->task-service
  
  dao-->solr-util9
```