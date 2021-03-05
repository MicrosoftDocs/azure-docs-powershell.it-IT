---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 049e1667fec5aef4f12a9912a4b9669364095b0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997470"
---
# <span data-ttu-id="ece3a-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="ece3a-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="ece3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ece3a-102">SYNOPSIS</span></span>
<span data-ttu-id="ece3a-103">Configurare le impostazioni di notifica di Azure Site Recovery (notifica tramite posta elettronica) per il Vault.</span><span class="sxs-lookup"><span data-stu-id="ece3a-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="ece3a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ece3a-104">SYNTAX</span></span>

### <span data-ttu-id="ece3a-105">Imposta (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ece3a-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ece3a-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="ece3a-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ece3a-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="ece3a-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ece3a-108">Disabilita</span><span class="sxs-lookup"><span data-stu-id="ece3a-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ece3a-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ece3a-109">DESCRIPTION</span></span>
<span data-ttu-id="ece3a-110">Il cmdlet **Set-AzRecoveryServicesAsrNotificationSetting** configura le impostazioni di notifica di Azure Site Recovery (notifica tramite posta elettronica) per il vault.</span><span class="sxs-lookup"><span data-stu-id="ece3a-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="ece3a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ece3a-111">EXAMPLES</span></span>

### <span data-ttu-id="ece3a-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ece3a-112">Example 1</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="ece3a-113">Disabilita notifica.</span><span class="sxs-lookup"><span data-stu-id="ece3a-113">Disable notification.</span></span>

### <span data-ttu-id="ece3a-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ece3a-114">Example 2</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="ece3a-115">Impostare una notifica per gli indirizzi di posta elettronica personalizzati e per il proprietario dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ece3a-115">Set notification for custom email address(s) and for subscription owner.</span></span>

### <span data-ttu-id="ece3a-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="ece3a-116">Example 3</span></span>

<span data-ttu-id="ece3a-117">Configurare le impostazioni di notifica di Azure Site Recovery (notifica tramite posta elettronica) per il Vault.</span><span class="sxs-lookup"><span data-stu-id="ece3a-117">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span> <span data-ttu-id="ece3a-118">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="ece3a-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress 'abcxxxx@xxxx.com' -DisableEmailToSubscriptionOwner
```

## <span data-ttu-id="ece3a-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ece3a-119">PARAMETERS</span></span>

### <span data-ttu-id="ece3a-120">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="ece3a-120">-CustomEmailAddress</span></span>
<span data-ttu-id="ece3a-121">Avviso/Notifica inviata ai messaggi di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="ece3a-121">Alert / Notification sent to emails.</span></span>

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

### <span data-ttu-id="ece3a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ece3a-122">-DefaultProfile</span></span>
<span data-ttu-id="ece3a-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ece3a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ece3a-124">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="ece3a-124">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="ece3a-125">Il parametro switch specifica l'abilitazione della notifica al proprietario dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ece3a-125">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="ece3a-126">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="ece3a-126">-DisableNotification</span></span>
<span data-ttu-id="ece3a-127">Contrassegna per disabilitare tutte le notifiche.</span><span class="sxs-lookup"><span data-stu-id="ece3a-127">Flag to disable all notification.</span></span>

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

### <span data-ttu-id="ece3a-128">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="ece3a-128">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="ece3a-129">Il parametro switch specifica l'abilitazione della notifica al proprietario dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ece3a-129">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="ece3a-130">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="ece3a-130">-LocaleID</span></span>
<span data-ttu-id="ece3a-131">Lingua di posta elettronica dell'avviso/notifica all'utente (codici delle impostazioni cultura supportati da Microsoft).</span><span class="sxs-lookup"><span data-stu-id="ece3a-131">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

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

### <span data-ttu-id="ece3a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ece3a-132">-Confirm</span></span>
<span data-ttu-id="ece3a-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ece3a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ece3a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ece3a-134">-WhatIf</span></span>
<span data-ttu-id="ece3a-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ece3a-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ece3a-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ece3a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ece3a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece3a-137">CommonParameters</span></span>
<span data-ttu-id="ece3a-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ece3a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece3a-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ece3a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece3a-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="ece3a-140">INPUTS</span></span>

### <span data-ttu-id="ece3a-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ece3a-141">None</span></span>

## <span data-ttu-id="ece3a-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ece3a-142">OUTPUTS</span></span>

### <span data-ttu-id="ece3a-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="ece3a-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="ece3a-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="ece3a-144">NOTES</span></span>

## <span data-ttu-id="ece3a-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ece3a-145">RELATED LINKS</span></span>
