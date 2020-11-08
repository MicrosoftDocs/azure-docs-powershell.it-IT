---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
ms.openlocfilehash: a0f8651bab30cf5a439b6e16110b34e7d256aa3a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019785"
---
# <span data-ttu-id="7febf-101">New-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="7febf-101">New-AzDataShareTrigger</span></span>

## <span data-ttu-id="7febf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7febf-102">SYNOPSIS</span></span>
<span data-ttu-id="7febf-103">Crea un trigger per l'abbonamento alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="7febf-103">Creates a trigger for share subscription.</span></span>

## <span data-ttu-id="7febf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7febf-104">SYNTAX</span></span>

```
New-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7febf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7febf-105">DESCRIPTION</span></span>
<span data-ttu-id="7febf-106">Il cmdlet **New-AzDataShareTrigger** crea un trigger per l'abbonamento alla condivisione per l'intervallo di ricorrenza e il tempo di sincronizzazione specificati in Azure Data Share account.</span><span class="sxs-lookup"><span data-stu-id="7febf-106">The **New-AzDataShareTrigger** cmdlet creates a trigger for share subscription for the specified recurrence interval and synchronization time under azure data share account.</span></span>

## <span data-ttu-id="7febf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7febf-107">EXAMPLES</span></span>

### <span data-ttu-id="7febf-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7febf-108">Example 1</span></span>
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

<span data-ttu-id="7febf-109">Questo comando crea un nuovo trigger AdsTrigger per la AdsShareSubscription della sottoscrizione di condivisione con un intervallo di ricorrenza giornaliera di 9 am.</span><span class="sxs-lookup"><span data-stu-id="7febf-109">This command creates a new trigger AdsTrigger for share subscription AdsShareSubscription with a daily recurrence interval of 9 am.</span></span>

## <span data-ttu-id="7febf-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7febf-110">PARAMETERS</span></span>

### <span data-ttu-id="7febf-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7febf-111">-AccountName</span></span>
<span data-ttu-id="7febf-112">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="7febf-112">Azure data share account name</span></span>

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

### <span data-ttu-id="7febf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7febf-113">-AsJob</span></span>
<span data-ttu-id="7febf-114">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="7febf-114">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="7febf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7febf-115">-DefaultProfile</span></span>
<span data-ttu-id="7febf-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7febf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7febf-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7febf-117">-Name</span></span>
<span data-ttu-id="7febf-118">Nome del trigger di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="7febf-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="7febf-119">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="7febf-119">-RecurrenceInterval</span></span>
<span data-ttu-id="7febf-120">Intervallo di ricorrenza per il trigger (giorno o ora)</span><span class="sxs-lookup"><span data-stu-id="7febf-120">The recurrence interval for the trigger (Day or Hour)</span></span>

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

### <span data-ttu-id="7febf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7febf-121">-ResourceGroupName</span></span>
<span data-ttu-id="7febf-122">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="7febf-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="7febf-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="7febf-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="7febf-124">Nome dell'abbonamento a condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="7febf-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="7febf-125">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="7febf-125">-SynchronizationTime</span></span>
<span data-ttu-id="7febf-126">Ora di inizio della sincronizzazione pianificata per il trigger</span><span class="sxs-lookup"><span data-stu-id="7febf-126">The start time of the scheduled synchronization for the trigger</span></span>

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

### <span data-ttu-id="7febf-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7febf-127">-Confirm</span></span>
<span data-ttu-id="7febf-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7febf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7febf-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7febf-129">-WhatIf</span></span>
<span data-ttu-id="7febf-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7febf-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7febf-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7febf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7febf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7febf-132">CommonParameters</span></span>
<span data-ttu-id="7febf-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7febf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7febf-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7febf-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7febf-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7febf-135">INPUTS</span></span>

### <span data-ttu-id="7febf-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7febf-136">None</span></span>

## <span data-ttu-id="7febf-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7febf-137">OUTPUTS</span></span>

### <span data-ttu-id="7febf-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="7febf-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="7febf-139">Note</span><span class="sxs-lookup"><span data-stu-id="7febf-139">NOTES</span></span>

## <span data-ttu-id="7febf-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7febf-140">RELATED LINKS</span></span>
