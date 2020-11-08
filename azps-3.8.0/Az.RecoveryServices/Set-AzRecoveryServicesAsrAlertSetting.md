---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: bd470a027285f66f15c831950639edaeb750c302
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021490"
---
# <span data-ttu-id="99cd4-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="99cd4-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="99cd4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="99cd4-102">SYNOPSIS</span></span>
<span data-ttu-id="99cd4-103">Configurare le impostazioni di notifica di ripristino del sito di Azure (notifica tramite posta elettronica) per il Vault.</span><span class="sxs-lookup"><span data-stu-id="99cd4-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="99cd4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99cd4-104">SYNTAX</span></span>

### <span data-ttu-id="99cd4-105">Set (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="99cd4-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99cd4-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="99cd4-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99cd4-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="99cd4-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99cd4-108">Disabilitare</span><span class="sxs-lookup"><span data-stu-id="99cd4-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99cd4-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99cd4-109">DESCRIPTION</span></span>
<span data-ttu-id="99cd4-110">Il cmdlet **set-AzRecoveryServicesAsrNotificationSetting** configura le impostazioni di notifica di ripristino di Azure sito (notifica tramite posta elettronica) per il Vault.</span><span class="sxs-lookup"><span data-stu-id="99cd4-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="99cd4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99cd4-111">EXAMPLES</span></span>

### <span data-ttu-id="99cd4-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="99cd4-112">Example 1</span></span>
```
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="99cd4-113">Disabilitare la notifica.</span><span class="sxs-lookup"><span data-stu-id="99cd4-113">Disable notification.</span></span>

### <span data-ttu-id="99cd4-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="99cd4-114">Example 2</span></span>
```
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="99cd4-115">Impostare la notifica per gli indirizzi di posta elettronica personalizzati e per il proprietario dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="99cd4-115">Set notification for custom email address(s) and for subscription owner.</span></span>

## <span data-ttu-id="99cd4-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99cd4-116">PARAMETERS</span></span>

### <span data-ttu-id="99cd4-117">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="99cd4-117">-CustomEmailAddress</span></span>
<span data-ttu-id="99cd4-118">Avviso/notifica inviato ai messaggi di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="99cd4-118">Alert / Notification sent to emails.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99cd4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99cd4-119">-DefaultProfile</span></span>
<span data-ttu-id="99cd4-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="99cd4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99cd4-121">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="99cd4-121">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="99cd4-122">Parametro switch specifica Enable per la notifica al proprietario dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="99cd4-122">Switch parameter specifies enable notification to subscription owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableEmailToSubcriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99cd4-123">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="99cd4-123">-DisableNotification</span></span>
<span data-ttu-id="99cd4-124">Contrassegna per disabilitare tutte le notifiche.</span><span class="sxs-lookup"><span data-stu-id="99cd4-124">Flag to disable all notification.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99cd4-125">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="99cd4-125">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="99cd4-126">Parametro switch specifica Enable per la notifica al proprietario dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="99cd4-126">Switch parameter specifies enable notification to subscription owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EmailToSubscriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99cd4-127">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="99cd4-127">-LocaleID</span></span>
<span data-ttu-id="99cd4-128">Lingua di posta elettronica di Alert/Notification to User (codici di lingua supportati da Microsoft).</span><span class="sxs-lookup"><span data-stu-id="99cd4-128">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

```yaml
Type: System.String
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99cd4-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="99cd4-129">-Confirm</span></span>
<span data-ttu-id="99cd4-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99cd4-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99cd4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99cd4-131">-WhatIf</span></span>
<span data-ttu-id="99cd4-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99cd4-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="99cd4-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99cd4-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99cd4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99cd4-134">CommonParameters</span></span>
<span data-ttu-id="99cd4-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99cd4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99cd4-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99cd4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99cd4-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="99cd4-137">INPUTS</span></span>

### <span data-ttu-id="99cd4-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="99cd4-138">None</span></span>

## <span data-ttu-id="99cd4-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99cd4-139">OUTPUTS</span></span>

### <span data-ttu-id="99cd4-140">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="99cd4-140">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="99cd4-141">Note</span><span class="sxs-lookup"><span data-stu-id="99cd4-141">NOTES</span></span>

## <span data-ttu-id="99cd4-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99cd4-142">RELATED LINKS</span></span>
