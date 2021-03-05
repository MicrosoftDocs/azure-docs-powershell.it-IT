---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
ms.openlocfilehash: fe082dc38f8a16dcca897623c4817d728fdaf3c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964734"
---
# <span data-ttu-id="180dc-101">New-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="180dc-101">New-AzDataShareTrigger</span></span>

## <span data-ttu-id="180dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="180dc-102">SYNOPSIS</span></span>
<span data-ttu-id="180dc-103">Crea un trigger per la condivisione della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="180dc-103">Creates a trigger for share subscription.</span></span>

## <span data-ttu-id="180dc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="180dc-104">SYNTAX</span></span>

```
New-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="180dc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="180dc-105">DESCRIPTION</span></span>
<span data-ttu-id="180dc-106">Il cmdlet **New-AzDataShareTrigger** crea un trigger per la sottoscrizione di condivisione per l'intervallo di ricorrenza e l'ora di sincronizzazione specificati nell'account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="180dc-106">The **New-AzDataShareTrigger** cmdlet creates a trigger for share subscription for the specified recurrence interval and synchronization time under azure data share account.</span></span>

## <span data-ttu-id="180dc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="180dc-107">EXAMPLES</span></span>

### <span data-ttu-id="180dc-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="180dc-108">Example 1</span></span>
```
PS C:\> New-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger" -RecurrenceInterval "Day" -SynchronizationTime "9:00"
CreatedAt           : 7/10/2019 12:16:34 AM
CreatedBy           : Ads test
ProvisioningState   : Succeeded
RecurrenceInterval  : Day
SynchronizationMode : Incremental
SynchronizationTime : 7/9/2019 9:00:00 AM
TriggerStatus       : Active
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/triggers/AdsTrigger
Name                : AdsTrigger
Type                : Microsoft.DataShare/Triggers
```

<span data-ttu-id="180dc-109">Questo comando crea un nuovo trigger AdsTrigger per condividere l'abbonamento AdsShareSubscription con un intervallo di ricorrenza giornaliero di 9 am.</span><span class="sxs-lookup"><span data-stu-id="180dc-109">This command creates a new trigger AdsTrigger for share subscription AdsShareSubscription with a daily recurrence interval of 9 am.</span></span>

## <span data-ttu-id="180dc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="180dc-110">PARAMETERS</span></span>

### <span data-ttu-id="180dc-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="180dc-111">-AccountName</span></span>
<span data-ttu-id="180dc-112">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="180dc-112">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180dc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="180dc-113">-AsJob</span></span>
<span data-ttu-id="180dc-114">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="180dc-114">{{Fill AsJob Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="180dc-115">-DefaultProfile</span></span>
<span data-ttu-id="180dc-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="180dc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="180dc-117">-Name</span><span class="sxs-lookup"><span data-stu-id="180dc-117">-Name</span></span>
<span data-ttu-id="180dc-118">Nome trigger condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="180dc-118">Azure data share trigger name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180dc-119">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="180dc-119">-RecurrenceInterval</span></span>
<span data-ttu-id="180dc-120">Intervallo di ricorrenza per il trigger (giorno o ora)</span><span class="sxs-lookup"><span data-stu-id="180dc-120">The recurrence interval for the trigger (Day or Hour)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180dc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="180dc-121">-ResourceGroupName</span></span>
<span data-ttu-id="180dc-122">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="180dc-122">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180dc-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="180dc-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="180dc-124">Nome della sottoscrizione per la condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="180dc-124">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180dc-125">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="180dc-125">-SynchronizationTime</span></span>
<span data-ttu-id="180dc-126">Ora di inizio della sincronizzazione pianificata per il trigger</span><span class="sxs-lookup"><span data-stu-id="180dc-126">The start time of the scheduled synchronization for the trigger</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="180dc-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="180dc-127">-Confirm</span></span>
<span data-ttu-id="180dc-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="180dc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="180dc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="180dc-129">-WhatIf</span></span>
<span data-ttu-id="180dc-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="180dc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="180dc-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="180dc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="180dc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="180dc-132">CommonParameters</span></span>
<span data-ttu-id="180dc-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="180dc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="180dc-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="180dc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="180dc-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="180dc-135">INPUTS</span></span>

### <span data-ttu-id="180dc-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="180dc-136">None</span></span>

## <span data-ttu-id="180dc-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="180dc-137">OUTPUTS</span></span>

### <span data-ttu-id="180dc-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="180dc-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="180dc-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="180dc-139">NOTES</span></span>

## <span data-ttu-id="180dc-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="180dc-140">RELATED LINKS</span></span>
