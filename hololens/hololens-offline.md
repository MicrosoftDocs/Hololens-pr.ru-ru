---
title: Управление конечными точками подключения для HoloLens
description: Узнайте, как настроить HoloLens в сети Wi-Fi в процессе управления и настройки конечных точек подключения.
keywords: hololens, автономная работа, запуск при первом включении
audience: ITPro
ms.date: 07/01/2019
ms.assetid: b86f603c-d25f-409b-b055-4bbc6edcd301
author: Teresa-Motiv
ms.author: v-tea
ms.custom:
- CI 111456
- CSSTroubleshooting
manager: jarrettr
ms.topic: article
ms.prod: hololens
ms.sitesec: library
ms.localizationpriority: high
appliesto:
- HoloLens (1st gen)
- HoloLens 2
ms.openlocfilehash: 63c82e5b1a953ee2f69bf4c22a8442c7bca07f073cc13f1e5e573fde0ccc1976
ms.sourcegitcommit: f8e7cc2fbdcdf8962700fd50b9c017bd83d1ad65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "115662940"
---
# <a name="manage-connection-endpoints-for-hololens"></a>Управление конечными точками подключения для HoloLens

Некоторые компоненты, приложения и связанные службы HoloLens передают данные в конечные точки сети Microsoft. В этой статье перечислены различные конечные точки и URL-адреса, которые должны быть разрешены в конфигурации сети (например, прокси-сервер или брандмауэр), чтобы эти компоненты могли работать.    

## <a name="near-offline-setup"></a>Установка почти в автономном режиме

HoloLens поддерживает ограниченный набор автономных возможностей для клиентов, использующих ограничения в сетевой среде. Тем не менее, HoloLens требуется сетевое подключение для первоначальной настройки устройства, при этом необходимо включить указанные ниже URL-адреса.

| Назначение | URL-адрес |
|------|------|
| IDPS | https://sdx.microsoft.com/frx/idps |
| [NCSI](/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services#bkmk-ncsi) |  http://www.msftconnecttest.com/connecttest.txt  |
| AADv9 | https://login.microsoftonline.com/WebApp/CloudDomainJoin/9 |
| AADv10 | https://login.microsoftonline.com/WebApp/CloudDomainJoin/10 |
| ПИН-код AAD | https://account.live.com/aadngc?uiflavor=win10&showSuccess=1 |
| MSA | https://login.live.com/ppsecure/inlineconnect.srf?id=80600 |
| ПИН-код MSA | https://account.live.com/msangc?fl=enroll |

## <a name="endpoint-configuration"></a>Конфигурация конечной точки

В дополнение к списку выше, чтобы использовать возможности HoloLens, в конфигурацию сети необходимо включить следующие конечные точки.


| Назначение | URL-адрес |
|------|------|
| Azure                                               | wd-prod-fe.cloudapp.azure.com                                       |
|                                                     | ris-prod-atm.trafficmanager.net                                     |
|                                                     | validation-v2.sls.trafficmanager.net                                |
| Многофакторная идентификация Azure AD                | https://secure.aadcdn.microsoftonline-p.com                         |
| Конфигурации Intune и MDM                       | activation-v2.sls.microsoft.com/*                                   |
|                                                     | cdn.onenote.net                                                     |
|                                                     | client.wns.windows.com                                              |
|                                                     | crl.microsoft.com/pki/crl/*                                         |
|                                                     | ctldl.windowsupdate.com                                             |
|                                                     | *displaycatalog.mp.microsoft.com                                    |
|                                                     | dm3p.wns.windows.com                                                |
|                                                     | *microsoft.com/pkiops/*                                             |
|                                                     | ocsp.digicert.com/*                                                 |
|                                                     | r.manage.microsoft.com                                              |
|                                                     | tile-service.weather.microsoft.com                                  |
|                                                     | settings-win.data.microsoft.com                                     |
| Сертификаты                                        | activation-v2.sls.microsoft.com/*                                   |
|                                                     | crl.microsoft.com/pki/crl/*                                         |
|                                                     | ocsp.digicert.com/*                                                 |
|                                                     | https://www.microsoft.com/pkiops/*                                          |
| Кортана и поиск                                  | store-images.*microsoft.com                                         |
|                                                     | www.bing.com/client                                                 |
|                                                     | www.bing.com                                                        |
|                                                     | www.bing.com/proactive                                              |
|                                                     | www.bing.com/threshold/xls.aspx                                     |
|                                                     | exo-ring.msedge.net                                                 |
|                                                     | fp.msedge.net                                                       |
|                                                     | fp-vp.azureedge.net                                                 |
|                                                     | odinvzc.azureedge.net                                               |
|                                                     | spo-ring.msedge.net                                                 |
| Проверка подлинности устройств                               | login.live.com*                                                     |
| Метаданные устройства                                     | dmd.metaservices.microsoft.com                                      |
| Расположение                                            | inference.location.live.net                                         |
|                                                     | location-inference-westus.cloudapp.net                              |
| Диагностические данные                                     | v10.events.data.microsoft.com                                       |
|                                                     | v10.vortex-win.data.microsoft.com/collect/v1                        |
|                                                     | https://www.microsoft.com                                                   |
|                                                     | co4.telecommand.telemetry.microsoft.com                             |
|                                                     | cs11.wpc.v0cdn.net                                                  |
|                                                     | cs1137.wpc.gammacdn.net                                             |
|                                                     | modern.watson.data.microsoft.com*                                   |
|                                                     | watson.telemetry.microsoft.com                                      |
| Лицензирование                                           | licensing.mp.microsoft.com                                          |
| Учетная запись Майкрософт                                   | login.msa.akadns6.net                                               |
|                                                     | us.configsvc1.live.com.akadns.net                                   |
| Microsoft Edge                                      | iecvlist.microsoft.com                                              |
| Служба перенаправления ссылок Microsoft (FWLink) | go.microsoft.com                                                    |
| Microsoft Store                                     | *.wns.windows.com                                                   |
|                                                     | storecatalogrevocation.storequality.microsoft.com                   |
|                                                     | img-prod-cms-rt-microsoft-com*                                      |
|                                                     | store-images.microsoft.com                                          |
|                                                     | .md.mp.microsoft.com                                                |
|                                                     | *displaycatalog.mp.microsoft.com                                    |
|                                                     | pti.store.microsoft.com                                             |
|                                                     | storeedgefd.dsx.mp.microsoft.com                                    |
|                                                     | markets.books.microsoft.com                                         |
|                                                     | share.microsoft.com                                                 |
| Индикатор работоспособности сетевых подключений (NCSI)          | www.msftconnecttest.com*                                            |
| Office                                              | *.c-msedge.net                                                      |
|                                                     | *.e-msedge.net                                                      |
|                                                     | *.s-msedge.net                                                      |
|                                                     | nexusrules.officeapps.live.com                                      |
|                                                     | ocos-office365-s2s.msedge.net                                       |
|                                                     | officeclient.microsoft.com                                          |
|                                                     | outlook.office365.com                                               |
|                                                     | client-office365-tas.msedge.net                                     |
|                                                     | https://www.office.com                                                      |
|                                                     | onecollector.cloudapp.aria                                          |
|                                                     | v10.events.data.microsoft.com/onecollector/1.0/                     |
|                                                     | self.events.data.microsoft.com                                      |
|                                                     | to-do.microsoft.com                                                 |
| OneDrive                                            | g.live.com/1rewlive5skydrive/*                                      |
|                                                     | msagfx.live.com                                                     |
|                                                     | oneclient.sfx.ms                                                    |
| Приложение "Фотографии"                                          | evoke-windowsservices-tas.msedge.net                                |
| Параметры                                            | cy2.settings.data.microsoft.com.akadns.net                          |
|                                                     | settings.data.microsoft.com                                         |
|                                                     | settings-win.data.microsoft.com                                     |
| Защитник Windows                                    | wdcp.microsoft.com                                                  |
|                                                     | definitionupdates.microsoft.com                                     |
|                                                     | go.microsoft.com                                                    |
|                                                     | *smartscreen.microsoft.com                                          |
|                                                     | smartscreen-sn3p.smartscreen.microsoft.com                          |
|                                                     | unitedstates.smartscreen-prod.microsoft.com                         |
| Windows: интересное                                   | *.search.msn.com                                                    |
|                                                     | arc.msn.com                                                         |
|                                                     | g.msn.com*                                                          |
|                                                     | query.prod.cms.rt.microsoft.com                                     |
|                                                     | ris.api.iris.microsoft.com                                          |
| Центр обновления Windows                                      | *.prod.do.dsp.mp.microsoft.com                                      |
|                                                     | cs9.wac.phicdn.net                                                  |
|                                                     | emdl.ws.microsoft.com                                               |
|                                                     | *.dl.delivery.mp.microsoft.com                                      |
|                                                     | *.windowsupdate.com                                                 |
|                                                     | *.delivery.mp.microsoft.com                                         |
|                                                     | *.update.microsoft.com                                              |



## <a name="references"></a>Ссылки

> [!NOTE]
> При развертывании Dynamics 365 Remote Assist необходимо включить конечные точки, перечисленные для SharePoint Online и OneDrive для бизнеса в списке [URL-адреса и диапазонов IP-адресов для Office 365](/office365/enterprise/urls-and-ip-address-ranges#skype-for-business-online-and-microsoft-teams).

- [Настройка диагностических сведений Windows в вашей организации](/windows/privacy/configure-windows-diagnostic-data-in-your-organization)
- [Управление конечными точками подключений для Windows 10 Корпоративная, версии 1903](/windows/privacy/manage-windows-1903-endpoints)
- [Управление подключениями компонентов операционной системы Windows 10 к службам Майкрософт](/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services)
- [Управление подключениями компонентов операционной системы Windows 10 к службам Майкрософт с помощью Microsoft Intune MDM Server](/windows/privacy/manage-connections-from-windows-operating-system-components-to-microsoft-services-using-mdm)
- [Требования к конфигурации сети Intune и ее пропускная способность](/intune/fundamentals/network-bandwidth-use#network-communication-requirements).
- [Конечные точки сети для Microsoft Intune](/intune/fundamentals/intune-endpoints)
- [URL-адреса и диапазоны IP-адресов Office 365](/office365/enterprise/urls-and-ip-address-ranges).
- [Необходимые условия для Azure AD Connect](/azure/active-directory/hybrid/how-to-connect-install-prerequisites)


## <a name="hololens-limitations"></a>Ограничения для HoloLens

После настройки HoloLens вы можете использовать это устройство без подключения к сети Wi-Fi, но приложения, использующие подключения к Интернету, будут работать с ограниченными возможностями при использовании HoloLens в автономном режиме.
