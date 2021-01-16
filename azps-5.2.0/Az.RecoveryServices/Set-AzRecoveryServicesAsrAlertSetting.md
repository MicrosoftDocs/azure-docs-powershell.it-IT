---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: c7821ddfd07b17a77c482a770b28672ccd664cb4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360720"
---
# <span data-ttu-id="f4e03-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="f4e03-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="f4e03-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4e03-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e03-103">Configurare le impostazioni di notifica di ripristino del sito di Azure (notifica tramite posta elettronica) per il Vault.</span><span class="sxs-lookup"><span data-stu-id="f4e03-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="f4e03-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4e03-104">SYNTAX</span></span>

### <span data-ttu-id="f4e03-105">Set (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f4e03-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4e03-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="f4e03-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4e03-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="f4e03-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4e03-108">Disabilitare</span><span class="sxs-lookup"><span data-stu-id="f4e03-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4e03-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4e03-109">DESCRIPTION</span></span>
<span data-ttu-id="f4e03-110">Il cmdlet **set-AzRecoveryServicesAsrNotificationSetting** configura le impostazioni di notifica di ripristino di Azure sito (notifica tramite posta elettronica) per il Vault.</span><span class="sxs-lookup"><span data-stu-id="f4e03-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="f4e03-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4e03-111">EXAMPLES</span></span>

### <span data-ttu-id="f4e03-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f4e03-112">Example 1</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="f4e03-113">Disabilitare la notifica.</span><span class="sxs-lookup"><span data-stu-id="f4e03-113">Disable notification.</span></span>

### <span data-ttu-id="f4e03-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f4e03-114">Example 2</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="f4e03-115">Impostare la notifica per gli indirizzi di posta elettronica personalizzati e per il proprietario dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f4e03-115">Set notification for custom email address(s) and for subscription owner.</span></span>

### <span data-ttu-id="f4e03-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="f4e03-116">Example 3</span></span>

<span data-ttu-id="f4e03-117">Configurare le impostazioni di notifica di ripristino del sito di Azure (notifica tramite posta elettronica) per il Vault.</span><span class="sxs-lookup"><span data-stu-id="f4e03-117">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span> <span data-ttu-id="f4e03-118">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="f4e03-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress 'abcxxxx@xxxx.com' -DisableEmailToSubscriptionOwner
```

## <span data-ttu-id="f4e03-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4e03-119">PARAMETERS</span></span>

### <span data-ttu-id="f4e03-120">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="f4e03-120">-CustomEmailAddress</span></span>
<span data-ttu-id="f4e03-121">Avviso/notifica inviato ai messaggi di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="f4e03-121">Alert / Notification sent to emails.</span></span>

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

### <span data-ttu-id="f4e03-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4e03-122">-DefaultProfile</span></span>
<span data-ttu-id="f4e03-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4e03-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4e03-124">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="f4e03-124">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="f4e03-125">Parametro switch specifica Enable per la notifica al proprietario dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f4e03-125">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="f4e03-126">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="f4e03-126">-DisableNotification</span></span>
<span data-ttu-id="f4e03-127">Contrassegna per disabilitare tutte le notifiche.</span><span class="sxs-lookup"><span data-stu-id="f4e03-127">Flag to disable all notification.</span></span>

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

### <span data-ttu-id="f4e03-128">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="f4e03-128">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="f4e03-129">Parametro switch specifica Enable per la notifica al proprietario dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f4e03-129">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="f4e03-130">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="f4e03-130">-LocaleID</span></span>
<span data-ttu-id="f4e03-131">Lingua di posta elettronica di Alert/Notification to User (codici di lingua supportati da Microsoft).</span><span class="sxs-lookup"><span data-stu-id="f4e03-131">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

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

### <span data-ttu-id="f4e03-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f4e03-132">-Confirm</span></span>
<span data-ttu-id="f4e03-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4e03-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4e03-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4e03-134">-WhatIf</span></span>
<span data-ttu-id="f4e03-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4e03-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4e03-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4e03-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4e03-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e03-137">CommonParameters</span></span>
<span data-ttu-id="f4e03-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4e03-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e03-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4e03-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e03-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4e03-140">INPUTS</span></span>

### <span data-ttu-id="f4e03-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f4e03-141">None</span></span>

## <span data-ttu-id="f4e03-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4e03-142">OUTPUTS</span></span>

### <span data-ttu-id="f4e03-143">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="f4e03-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="f4e03-144">Note</span><span class="sxs-lookup"><span data-stu-id="f4e03-144">NOTES</span></span>

## <span data-ttu-id="f4e03-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4e03-145">RELATED LINKS</span></span>
