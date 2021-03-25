---
title: Руководство по развертыванию — Корпоративные подключенные HoloLens 2 с руководствами dynamics 365 — подготовка
description: Узнайте, как подготовиться к регистрации устройств HoloLens 2 в корпоративной сети, подключенной к динамическим руководствам 365.
keywords: HoloLens, управление, корпоративное подключение, Руководство по динамике 365, AAD, Azure AD, MDM, Управление мобильными устройствами
author: joyjaz
ms.author: v-jjaswinski
ms.reviewer: aboeger
ms.date: 03/24/2021
ms.prod: hololens
ms.topic: article
ms.sitesec: library
ms.localizationpriority: medium
audience: HoloLens
manager: yannisle
appliesto:
- HoloLens 2
ms.openlocfilehash: 2ab24aeac371b8d4a17d6121c3adf317cac7daf1
ms.sourcegitcommit: d7c86ccad7be32f7223d4b801083798454fda740
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/25/2021
ms.locfileid: "11448611"
---
# <a name="prepare---corporate-connected-guide"></a>Подготовка — руководство по корпоративным подключениям
## <a name="infrastructure-essentials"></a>Основные объекты инфраструктуры
Для личных и корпоративных сценариев развертывания система управления мобильными устройствами (MDM) является необходимой инфраструктурой, необходимой для развертывания и управления устройствами Windows 10, особенно HoloLens 2. Подписка [Azure AD Premium](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-get-started-premium) рекомендуется в **** качестве поставщика удостоверений и необходима для поддержки определенных возможностей.

> [!NOTE]
> Несмотря на то, что HoloLens 2 развертывается и управляется как мобильное устройство, оно обычно используется в качестве общего устройства между многими пользователями.

## <a name="azure-active-directory"></a>Azure Active Directory
Azure AD— это облачная служба каталогов, обеспечивающая управление удостоверениями и доступом. Организации, использующие Microsoft Office 365 или Intune, уже используют Azure AD, которая имеет три выпуска: Free, Premium P1 и Premium P2 (см. в выпуске [Azure Active Directory).](https://azure.microsoft.com/documentation/articles/active-directory-editions) Все выпуски поддерживают регистрацию устройств Azure AD, но premium P1 необходим для автоматической регистрации MDM, которую мы будем использовать в этом руководстве позже.
> [!Important]
> Важно иметь Azure AD, так как устройства HoloLens не поддерживают локальное участие в AD. Если у вас еще нет настройка Azure AD, следуйте инструкциям по началу работы и создайте нового клиента [в Azure Active Directory.](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-access-create-new-tenant)

## <a name="identity-management"></a>Управление удостоверением
В этом руководстве [идентификатором](https://docs.microsoft.com/hololens/hololens-identity) будут использоваться учетные записи Azure AD. Учетные записи Azure AD имеют несколько преимуществ, например:
- Сотрудники используют свою учетную запись Azure AD для регистрации устройства в Azure AD и могут автоматически регистрировать его с помощью решения MDM организации (Azure AD+MDM — требуется подписка [Azure AD Premium).](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-get-started-premium)
- Учетные записи Azure AD имеют [дополнительные](https://docs.microsoft.com/hololens/hololens-identity) параметры проверки подлинности с [помощью Windows Hello для бизнеса.](https://docs.microsoft.com/windows/security/identity-protection/hello-for-business/hello-identity-verification) Помимо входа в систему Iris пользователи могут войти с другого устройства или использовать ключи безопасности FIDO.

> [!WARNING] 
> Сотрудники могут использовать только одну учетную запись для инициализации устройства, поэтому необходимо сначала контролировать, какая учетная **запись включена.** Выбранная учетная запись определяет, кто контролирует устройство, и влияет на возможности управления.

## <a name="mobile-device-management"></a>Управление мобильными устройствами
Microsoft Intune, часть корпоративной мобильности и безопасности, является облачной системой MDM, которая управляет устройствами, подключенными к вашему клиенту. Как и Office 365, Intune использует Azure AD для управления удостоверениями, поэтому сотрудники используют те же учетные данные для регистрации устройств в Intune, что и для входа в Office 365. Intune также поддерживает устройства с другими операционными системами, такими как iOS и Android, для предоставления полного решения MDM. В этом руководстве мы сосредоточимся на использовании Intune для включения развертывания во внутреннюю сеть с помощью HoloLens 2.
> [!Important] 
> Важно иметь управление мобильными устройствами. Если она еще не настроена, следуйте этому руководству и привнося в Intune.

> [!Important]
> Для использования руководств требуется учетная запись Azure AD.

> [!Note] 
> Windows 10 поддерживается несколькими системами MDM, и большинство из них поддерживает сценарии развертывания как персональных, так и корпоративных устройств. Поставщики MDM, поддерживают Windows 10 Holographic, включают: AirWatch, MobileIron и другие. Большинство ведущих поставщиков решений MDM в отрасли уже обеспечивают поддержку интеграции с Azure AD. Вы можете найти самый текущий список поставщиков MDM, которые поддерживают Azure AD в [Azure Marketplace.](https://azuremarketplace.microsoft.com/marketplace/apps/category/azure-active-directory-apps)

## <a name="network-access"></a>Доступ к сети 
Dynamics 365 Guides — это облачное приложение. Если у администратора сети есть список утверждений, им может потребоваться добавить IP-адреса и/или конечные точки, необходимые для подключения к серверам Dynamics 365. [Узнайте больше о разблокирования IP-адресов и URL-адресов.](https://docs.microsoft.com/power-platform/admin/online-requirements#ip-addresses-and-urls)

## <a name="certificates"></a>Сертификаты
Сертификаты помогают повысить безопасность, предоставляя проверку подлинности учетных записей, Wi-Fi проверку подлинности, шифрование VPN и SSL-шифрование веб-контента. Несмотря на то, что администраторы могут управлять сертификатами на устройствах вручную с помощью пакетов подготовка, лучше всего использовать систему MDM для управления этими сертификатами на протяжении всего жизненного цикла — от регистрации до обновления и отзыва. 

Ваша система MDM может автоматически развертывать эти сертификаты в хранилищах сертификатов устройств после их регистрации (если ваша система MDM поддерживает простой протокол регистрации сертификатов **(SCEP)** или стандарты шифрования общедоступных ключей **#12 (PKCS#12)**). [Узнайте о типах и профилях сертификатов, которые вы используете в Microsoft Intune.](https://docs.microsoft.com/mem/intune/protect/certificates-configure) MDM также может запрашивать и удалять зарегистрированные клиентские сертификаты или запускать новый запрос на регистрацию до истечения срока действия текущего сертификата.
 
Если ваши системы MDM уже настроены для сертификатов, перенастройте справки Подготовка сертификатов и сетевых профилей [для HoloLens 2,](https://docs.microsoft.com/hololens/hololens-certificates-network) чтобы приступить к развертыванию сертификатов и профилей для устройств HoloLens 2.

## <a name="scep"></a>SCEP

Для развертывания SCEP необходимы следующие службы, за исключением прокси-сервера веб-приложения.
- [Управление сертификацией](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj125375(v=ws.11))
- [Роль сервера NDES](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831498(v=ws.11))
- [Соединитель Microsoft Intune](https://docs.microsoft.com/mem/intune/protect/certificates-scep-configure#install-the-microsoft-intune-connector)

Вы также должны опубликовать URL-адрес NDES вне корпоративной сети с помощью прокси-сервера приложения [Azure AD или прокси-сервера веб-доступа.](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy-add-on-premises-application) Вы также можете использовать другой обратный прокси по вашему выбору.

![Поток данных SCEP](./images/hololens2-scep-info-flow.png)

Если ваша сеть еще не поддерживает SCEP или вы не уверены, правильно ли настроена ваша сеть для SCEP с помощью Intune, направите ссылку Настройте инфраструктуру для поддержки SCEP с  [помощью Intune](https://docs.microsoft.com/mem/intune/protect/certificates-scep-configure).

Если ваша инфраструктура уже поддерживает SCEP, [](https://docs.microsoft.com/mem/intune/protect/certificates-profile-scep) необходимо [](https://docs.microsoft.com/mem/configmgr/protect/deploy-use/create-certificate-profiles) создать профиль для каждого сертификата SCEP, который будет использовать HoloLens 2. Если у вас возникли проблемы с SCEP, используйте использование профилей сертификатов SCEP для предоставления сертификатов [в Microsoft Intune.](https://docs.microsoft.com/troubleshoot/mem/intune/troubleshoot-scep-certificate-profiles)

## <a name="pkcs"></a>PKCS
Intune также поддерживает использование частных и общедоступных сертификатов пары ключей (PKCS). Дополнительные сведения используйте частные и общедоступные сертификаты [ключей в Microsoft Intune.](https://docs.microsoft.com/mem/intune/protect/certificates-pfx-configure)

## <a name="proxy"></a>Прокси-сервер
Большинство корпоративных сетей интрасети используют прокси для управления внешним трафиком. С помощью HoloLens 2 можно настроить прокси-сервер для подключений к ethernet, Wi-Fi и VPN.

Существует несколько различных типов прокси и способов настройки прокси. Для целей этого руководства мы выбираем **прокси-сервер Wi-Fi,** задающийся по URL-адресу PAC и развернутый с помощью MDM. Это связано с преимуществами автоматического развертывания с помощью MDM, возможности обновлять файл PAC вместо конфигурации сервера:порт и, наконец, с помощью проксиWi-Fi для настройки прокси-сервера, чтобы применяться только к одному подключению Wi-Fi, что позволяет использовать устройства по-прежнему, если подключены в другом расположении. 


Дополнительные сведения о параметрах прокси для Windows 10 см. в Wi-Fi профиле для устройств [в Microsoft Intune - Azure.](https://docs.microsoft.com/mem/intune/configuration/wi-fi-settings-configure)

## <a name="line-of-business-apps"></a>Линия бизнес-приложений 
Хотя несколько приложений можно установить через Microsoft Store, скорее всего, у вас есть собственное настраиваемое приложение, созданное специально для использования в смешанной реальности. Эти настраиваемые приложения, распространяемые по всей организации для вашего бизнеса, называются приложениями Line of Business (LOB).
  
Существует несколько способов развертывания приложений на устройствах HoloLens 2. Приложения можно развертывать непосредственно через MDM, Microsoft Store для бизнеса (MSfB) или в пакете предварительной загрузки. Для этого руководства мы будем развертывать приложения через MDM с помощью обязательной установки приложения. Это позволит автоматически загружать приложения LOB на устройства HoloLens после завершения регистрации.

Для тех из вас, у кого нет собственного LOB, мы предокаст пример приложения для проверки этого потока развертывания. Это приложение будет [приложением примеры MRTK,](https://aka.ms/HoloLensDocs-Sample-MRTK-Examples-App) и уже было предварительно отстроено и упаковано для проверки на доказательство концепции.
 
Дополнительные сведения о развертывании приложений можно найти в [app Management: Обзор](https://docs.microsoft.com/hololens/app-deploy-overview).

> [!NOTE]
> HoloLens 2 поддерживает запуск только приложений ARM64 UWP.

## <a name="guides-playbook"></a>Руководство Playbook
Руководство использует среду Microsoft Dataverse в качестве магазина данных для приложений Guides. Важно понимать более масштабную картину взаимодействия среды Dataverse с приложениями Guides и клиентом. В этом руководстве мы не будем освещать управление вашей обратной стороной данных, но просмотрите основные концепции развертывания [руководств Dynamics 365 - Dynamics 365 Mixed Reality](https://docs.microsoft.com/dynamics365/mixed-reality/guides/admin-deployment-playbook).

## <a name="next-step"></a>Дальнейшие действия 
> [!div class="nextstepaction"]
> [Развертывание подключенных к корпоративной связи — настройка](hololens2-corp-connected-configure.md)