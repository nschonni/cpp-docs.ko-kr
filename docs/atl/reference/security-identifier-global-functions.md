---
title: "보안 식별자 전역 함수 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- security IDs [C++]
- SIDs [C++], returning SID objects
ms.assetid: 85404dcb-c59b-4535-ab3d-66cfa37e87de
caps.latest.revision: 20
author: mikeblome
ms.author: mblome
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
translationtype: Machine Translation
ms.sourcegitcommit: 604a4bf49490ad2599c857eb3afd527d67e1e25b
ms.openlocfilehash: 9e51fe30b0519514df34f1a77b1e731f51047520
ms.lasthandoff: 02/24/2017

---
# <a name="security-identifier-global-functions"></a>보안 식별자 전역 함수
이러한 함수는 개체 일반적인 잘 알려진 SID를 반환합니다.  
  
> [!IMPORTANT]
>  다음 표에 나열 된 함수에서 실행 되는 응용 프로그램에서 사용할 수 없습니다는 [!INCLUDE[wrt](../../atl/reference/includes/wrt_md.md)]합니다.  
  
|||  
|-|-|  
|[Sids::AccountOps](#accountops)|DOMAIN_ALIAS_RID_ACCOUNT_OPS SID를 반환합니다.|  
|[Sids::Admins](#admins)|DOMAIN_ALIAS_RID_ADMINS SID를 반환합니다.|  
|[Sids::AnonymousLogon](#anonymouslogon)|SECURITY_ANONYMOUS_LOGON_RID SID를 반환합니다.|  
|[Sids::AuthenticatedUser](#authenticateduser)|SECURITY_AUTHENTICATED_USER_RID SID를 반환합니다.|  
|[Sids::BackupOps](#backupops)|DOMAIN_ALIAS_RID_BACKUP_OPS SID를 반환합니다.|  
|[Sids::Batch](#batch)|SECURITY_BATCH_RID SID를 반환합니다.|  
|[Sids::CreatorGroup](#creatorgroup)|SECURITY_CREATOR_GROUP_RID SID를 반환합니다.|  
|[Sids::CreatorGroupServer](#creatorgroupserver)|SECURITY_CREATOR_GROUP_SERVER_RID SID를 반환합니다.|  
|[Sids::CreatorOwner](#creatorowner)|SECURITY_CREATOR_OWNER_RID SID를 반환합니다.|  
|[Sids::CreatorOwnerServer](#creatorownerserver)|SECURITY_CREATOR_OWNER_SERVER_RID SID를 반환합니다.|  
|[Sids::Dialup](#dialup)|SECURITY_DIALUP_RID SID를 반환합니다.|  
|[Sids::Guests](#guests)|DOMAIN_ALIAS_RID_GUESTS SID를 반환합니다.|  
|[Sids::Interactive](#interactive)|SECURITY_INTERACTIVE_RID SID를 반환합니다.|  
|[Sids::Local](#local)|SECURITY_LOCAL_RID SID를 반환합니다.|  
|[Sids::Network](#network)|SECURITY_NETWORK_RID SID를 반환합니다.|  
|[Sids::NetworkService](#networkservice)|SECURITY_NETWORK_SERVICE_RID SID를 반환합니다.|  
|[Sids::Null](#null)|SECURITY_NULL_RID SID를 반환합니다.|  
|[Sids::PreW2KAccess](#prew2kaccess)|DOMAIN_ALIAS_RID_PREW2KCOMPACCESS SID를 반환합니다.|  
|[Sids::PowerUsers](#powerusers)|DOMAIN_ALIAS_RID_POWER_USERS SID를 반환합니다.|  
|[Sids::PrintOps](#printops)|DOMAIN_ALIAS_RID_PRINT_OPS SID를 반환합니다.|  
|[Sids::Proxy](#proxy)|SECURITY_PROXY_RID SID를 반환합니다.|  
|[Sids::RasServers](#rasservers)|DOMAIN_ALIAS_RID_RAS_SERVERS SID를 반환합니다.|  
|[Sids::Replicator](#replicator)|DOMAIN_ALIAS_RID_REPLICATOR SID를 반환합니다.|  
|[Sids::RestrictedCode](#restrictedcode)|SECURITY_RESTRICTED_CODE_RID SID를 반환합니다.|  
|[Sids::Self](#self)|SECURITY_PRINCIPAL_SELF_RID SID를 반환합니다.|  
|[Sids::ServerLogon](#serverlogon)|SECURITY_SERVER_LOGON_RID SID를 반환합니다.|  
|[Sids::Service](#service)|SECURITY_SERVICE_RID SID를 반환합니다.|  
|[Sids::System](#system)|SECURITY_LOCAL_SYSTEM_RID SID를 반환합니다.|  
|[Sids::SystemOps](#systemops)|DOMAIN_ALIAS_RID_SYSTEM_OPS SID를 반환합니다.|  
|[Sids::TerminalServer](#terminalserver)|SECURITY_TERMINAL_SERVER_RID SID를 반환합니다.|  
|[Sids::Users](#users)|DOMAIN_ALIAS_RID_USERS SID를 반환합니다.|  
|[Sids::World](#world)|SECURITY_WORLD_RID SID를 반환합니다.|  

### <a name="requirements"></a>요구 사항  
 **헤더:** atlsecurity.h 

##  <a name="a-nameaccountopsa--sidsaccountops"></a><a name="accountops"></a>Sids::AccountOps  
 DOMAIN_ALIAS_RID_ACCOUNT_OPS SID를 반환합니다.    
  
```
CSid AccountOps() throw(...);
```  
  
##  <a name="a-nameadminsa--sidsadmins"></a><a name="admins"></a>Sids::Admins  
 DOMAIN_ALIAS_RID_ADMINS SID를 반환합니다.  
```
CSid Admins() throw(...);
```  
  
##  <a name="a-nameanonymouslogona--sidsanonymouslogon"></a><a name="anonymouslogon"></a>Sids::AnonymousLogon  
 SECURITY_ANONYMOUS_LOGON_RID SID를 반환합니다.  
```
CSid AnonymousLogon() throw(...);
```  
  
##  <a name="a-nameauthenticatedusera--sidsauthenticateduser"></a><a name="authenticateduser"></a>Sids::AuthenticatedUser  
 SECURITY_AUTHENTICATED_USER_RID SID를 반환합니다.  
```
CSid AuthenticatedUser() throw(...);
```  
  
##  <a name="a-namebackupopsa--sidsbackupops"></a><a name="backupops"></a>Sids::BackupOps  
 DOMAIN_ALIAS_RID_BACKUP_OPS SID를 반환합니다.  
```
CSid BackupOps() throw(...);
```  
  
##  <a name="a-namebatcha--sidsbatch"></a><a name="batch"></a>Sids::Batch  
 SECURITY_BATCH_RID SID를 반환합니다.  
```
CSid Batch() throw(...);
```  
  
##  <a name="a-namecreatorgroupa--sidscreatorgroup"></a><a name="creatorgroup"></a>Sids::CreatorGroup  
 SECURITY_CREATOR_GROUP_RID SID를 반환합니다.  
```
CSid CreatorGroup() throw(...);
```  
  
##  <a name="a-namecreatorgroupservera--sidscreatorgroupserver"></a><a name="creatorgroupserver"></a>Sids::CreatorGroupServer  
 SECURITY_CREATOR_GROUP_SERVER_RID SID를 반환합니다.  
```
CSid CreatorGroupServer() throw(...);
```  
  
##  <a name="a-namecreatorownera--sidscreatorowner"></a><a name="creatorowner"></a>Sids::CreatorOwner  
 SECURITY_CREATOR_OWNER_RID SID를 반환합니다.  
```
CSid CreatorOwner() throw(...);
```  
  
##  <a name="a-namecreatorownerservera--sidscreatorownerserver"></a><a name="creatorownerserver"></a>Sids::CreatorOwnerServer  
 SECURITY_CREATOR_OWNER_SERVER_RID SID를 반환합니다.  
```
CSid CreatorOwnerServer() throw(...);
```  
  
##  <a name="a-namedialupa--sidsdialup"></a><a name="dialup"></a>Sids::Dialup  
 SECURITY_DIALUP_RID SID를 반환합니다.  
```
CSid Dialup() throw(...);
```  
  
##  <a name="a-nameguestsa--sidsguests"></a><a name="guests"></a>Sids::Guests  
 DOMAIN_ALIAS_RID_GUESTS SID를 반환합니다.  
```
CSid Guests() throw(...);
```  
  
##  <a name="a-nameinteractivea--sidsinteractive"></a><a name="interactive"></a>Sids::Interactive  
 SECURITY_INTERACTIVE_RID SID를 반환합니다.  
```
CSid Interactive() throw(...);
```  
  
##  <a name="a-namelocala--sidslocal"></a><a name="local"></a>Sids::Local  
 SECURITY_LOCAL_RID SID를 반환합니다.  
```
CSid Local() throw(...);
```  
  
##  <a name="a-namenetworka--sidsnetwork"></a><a name="network"></a>Sids::Network  
 SECURITY_NETWORK_RID SID를 반환합니다.  
```
CSid Network() throw(...);
```  
  
##  <a name="a-namenetworkservicea--sidsnetworkservice"></a><a name="networkservice"></a>Sids::NetworkService  
 SECURITY_NETWORK_SERVICE_RID SID를 반환합니다.  
```
CSid NetworkService() throw(...);
```  
  
### <a name="remarks"></a>주의  
 NetworkService를 사용 하 여 NT AUTHORITY\NetworkService 사용자 CPerfMon 보안 개체를 읽을 수 있도록 합니다. NetworkService DLL에는 NetworkService 계정으로 로그인 할 수 있는 ATLServer 코드에는 SecurityAttribute 추가 [!INCLUDE[WinXpFamily](../../atl/reference/includes/winxpfamily_md.md)] 및 큰 운영 체제입니다.  
  
 사용자 지정 로그 카운터는 Perfmon mmc에서 ATLServer CPerfMon 클래스를 사용 하 여 만들어집니다, 실시간 보기에서 올바르게 표시 되도록 하지만 로그 파일을 볼 때 카운터 나타나지 않을 수 있습니다. CPerfMon 사용자 지정 성능 카운터에는 "성능 로그 및 경고" 서비스 (smlogsvc.exe)에서 실행 하는 데 필요한 권한이 없는 [!INCLUDE[WinXpFamily](../../atl/reference/includes/winxpfamily_md.md)] (이상) 운영 체제입니다. 이 서비스는 "NT AUTHORITY\NetworkService" 계정에서 실행 합니다.  
  
##  <a name="a-namenulla--sidsnull"></a><a name="null"></a>Sids::Null  
 SECURITY_NULL_RID SID를 반환합니다.  
```
CSid Null() throw(...);
```  
  
##  <a name="a-nameprew2kaccessa--sidsprew2kaccess"></a><a name="prew2kaccess"></a>Sids::PreW2KAccess  
 DOMAIN_ALIAS_RID_PREW2KCOMPACCESS SID를 반환합니다.  
```
CSid PreW2KAccess() throw(...);
```  
  
##  <a name="a-namepowerusersa--sidspowerusers"></a><a name="powerusers"></a>Sids::PowerUsers  
 DOMAIN_ALIAS_RID_POWER_USERS SID를 반환합니다.  
```
CSid PowerUsers() throw(...);
```  
  
##  <a name="a-nameprintopsa--sidsprintops"></a><a name="printops"></a>Sids::PrintOps  
 DOMAIN_ALIAS_RID_PRINT_OPS SID를 반환합니다.  
```
CSid PrintOps() throw(...);
```  
  
##  <a name="a-nameproxya--sidsproxy"></a><a name="proxy"></a>Sids::Proxy  
 SECURITY_PROXY_RID SID를 반환합니다.  
```
CSid Proxy() throw(...);
```  
  
##  <a name="a-namerasserversa--sidsrasservers"></a><a name="rasservers"></a>Sids::RasServers  
 DOMAIN_ALIAS_RID_RAS_SERVERS SID를 반환합니다.  
```
CSid RasServers() throw(...);
```  
  
##  <a name="a-namereplicatora--sidsreplicator"></a><a name="replicator"></a>Sids::Replicator  
 DOMAIN_ALIAS_RID_REPLICATOR SID를 반환합니다.  
```
CSid Replicator() throw(...);
```  
  
##  <a name="a-namerestrictedcodea--sidsrestrictedcode"></a><a name="restrictedcode"></a>Sids::RestrictedCode  
 SECURITY_RESTRICTED_CODE_RID SID를 반환합니다.  
```
CSid RestrictedCode() throw(...);
```  
  
##  <a name="a-nameselfa--sidsself"></a><a name="self"></a>Sids::Self  
 SECURITY_PRINCIPAL_SELF_RID SID를 반환합니다.  
```
CSid Self() throw(...);
```  
  
##  <a name="a-nameserverlogona--sidsserverlogon"></a><a name="serverlogon"></a>Sids::ServerLogon  
 SECURITY_SERVER_LOGON_RID SID를 반환합니다.  
```
CSid ServerLogon() throw(...);
```  
  
##  <a name="a-nameservicea--sidsservice"></a><a name="service"></a>Sids::Service  
 SECURITY_SERVICE_RID SID를 반환합니다.  
```
CSid Service() throw(...);
```  
  
##  <a name="a-namesystema--sidssystem"></a><a name="system"></a>Sids::System  
 SECURITY_LOCAL_SYSTEM_RID SID를 반환합니다.  
```
CSid System() throw(...);
```  
  
##  <a name="a-namesystemopsa--sidssystemops"></a><a name="systemops"></a>Sids::SystemOps  
 DOMAIN_ALIAS_RID_SYSTEM_OPS SID를 반환합니다.  
```
CSid SystemOps() throw(...);
```  
  
##  <a name="a-nameterminalservera--sidsterminalserver"></a><a name="terminalserver"></a>Sids::TerminalServer  
 SECURITY_TERMINAL_SERVER_RID SID를 반환합니다.  
```
CSid TerminalServer() throw(...);
```  
  
##  <a name="a-nameusersa--sidsusers"></a><a name="users"></a>Sids::Users  
 DOMAIN_ALIAS_RID_USERS SID를 반환합니다.  
```
CSid Users() throw(...);
```  
  
##  <a name="a-nameworlda--sidsworld"></a><a name="world"></a>Sids::World  
 SECURITY_WORLD_RID SID를 반환합니다.  
```
CSid World() throw(...);
```  
  
## <a name="see-also"></a>참고 항목  
 [함수](../../atl/reference/atl-functions.md)
