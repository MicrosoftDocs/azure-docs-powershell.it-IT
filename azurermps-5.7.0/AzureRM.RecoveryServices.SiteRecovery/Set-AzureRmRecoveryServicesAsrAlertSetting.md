---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 4e51cd90e490442c36b5864e53b4bb7a36e41e80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514199"
---
# <span data-ttu-id="eeace-101">Set-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="eeace-101">Set-AzureRmRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="eeace-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eeace-102">SYNOPSIS</span></span>
<span data-ttu-id="eeace-103">Configurare le impostazioni di notifica di ripristino del sito di Azure (notifica tramite posta elettronica) per il Vault.</span><span class="sxs-lookup"><span data-stu-id="eeace-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eeace-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eeace-104">SYNTAX</span></span>

### <span data-ttu-id="eeace-105">Set (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eeace-105">Set (Default)</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeace-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="eeace-106">EmailToSubscriptionOwner</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeace-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="eeace-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeace-108">Disabilitare</span><span class="sxs-lookup"><span data-stu-id="eeace-108">Disable</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eeace-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eeace-109">DESCRIPTION</span></span>
<span data-ttu-id="eeace-110">Il cmdlet **set-AzureRmRecoveryServicesAsrNotificationSetting** configura le impostazioni di notifica di ripristino di Azure sito (notifica tramite posta elettronica) per il Vault.</span><span class="sxs-lookup"><span data-stu-id="eeace-110">The **Set-AzureRmRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="eeace-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eeace-111">EXAMPLES</span></span>

### <span data-ttu-id="eeace-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="eeace-112">Example 1</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="eeace-113">Disabilitare la notifica.</span><span class="sxs-lookup"><span data-stu-id="eeace-113">Disable notification.</span></span>

### <span data-ttu-id="eeace-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="eeace-114">Example 2</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="eeace-115">Impostare la notifica per gli indirizzi di posta elettronica personalizzati e per il proprietario dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="eeace-115">Set notification for custom email address(s) and for subscription owner.</span></span>

## <span data-ttu-id="eeace-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eeace-116">PARAMETERS</span></span>

### <span data-ttu-id="eeace-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="eeace-117">-Confirm</span></span>
<span data-ttu-id="eeace-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeace-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeace-119">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="eeace-119">-CustomEmailAddress</span></span>
<span data-ttu-id="eeace-120">Avviso/notifica inviato ai messaggi di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="eeace-120">Alert / Notification sent to emails.</span></span>

```yaml
Type: String[]
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeace-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeace-121">-DefaultProfile</span></span>
<span data-ttu-id="eeace-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eeace-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeace-123">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="eeace-123">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="eeace-124">Parametro switch specifica Enable per la notifica al proprietario dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="eeace-124">Switch parameter specifies enable notification to subscription owner.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableEmailToSubcriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeace-125">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="eeace-125">-DisableNotification</span></span>
<span data-ttu-id="eeace-126">Contrassegna per disabilitare tutte le notifiche.</span><span class="sxs-lookup"><span data-stu-id="eeace-126">Flag to disable all notification.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeace-127">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="eeace-127">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="eeace-128">Switch parametro specifica Enable per la notifica al proprietario dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="eeace-128">Switch paramter specifies enable notification to subscription owner.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EmailToSubscriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeace-129">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="eeace-129">-LocaleID</span></span>
<span data-ttu-id="eeace-130">Lingua di posta elettronica di Alert/notifcation to User (codici di lingua supportati da Microsoft).</span><span class="sxs-lookup"><span data-stu-id="eeace-130">Email language of alert /notifcation to user(supported culture codes from microsoft).</span></span> 

```yaml
Type: String
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeace-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeace-131">-WhatIf</span></span>
<span data-ttu-id="eeace-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eeace-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eeace-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eeace-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeace-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeace-134">CommonParameters</span></span>
<span data-ttu-id="eeace-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeace-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeace-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeace-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeace-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eeace-137">INPUTS</span></span>

### <span data-ttu-id="eeace-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="eeace-138">None</span></span>

## <span data-ttu-id="eeace-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eeace-139">OUTPUTS</span></span>

### <span data-ttu-id="eeace-140">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="eeace-140">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="eeace-141">Note</span><span class="sxs-lookup"><span data-stu-id="eeace-141">NOTES</span></span>

## <span data-ttu-id="eeace-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eeace-142">RELATED LINKS</span></span>
