---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
ms.openlocfilehash: f7342ec33e712407987da28b232670d56bdcab66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674656"
---
# <span data-ttu-id="3a284-101">New-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="3a284-101">New-AzDataShareTrigger</span></span>

## <span data-ttu-id="3a284-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3a284-102">SYNOPSIS</span></span>
<span data-ttu-id="3a284-103">Crea un trigger per l'abbonamento alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="3a284-103">Creates a trigger for share subscription.</span></span>

## <span data-ttu-id="3a284-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a284-104">SYNTAX</span></span>

```
New-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a284-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a284-105">DESCRIPTION</span></span>
<span data-ttu-id="3a284-106">Il cmdlet **New-AzDataShareTrigger** crea un trigger per l'abbonamento alla condivisione per l'intervallo di ricorrenza e il tempo di sincronizzazione specificati in Azure Data Share account.</span><span class="sxs-lookup"><span data-stu-id="3a284-106">The **New-AzDataShareTrigger** cmdlet creates a trigger for share subscription for the specified recurrence interval and synchronization time under azure data share account.</span></span>

## <span data-ttu-id="3a284-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a284-107">EXAMPLES</span></span>

### <span data-ttu-id="3a284-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3a284-108">Example 1</span></span>
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

<span data-ttu-id="3a284-109">Questo comando crea un nuovo trigger AdsTrigger per la AdsShareSubscription della sottoscrizione di condivisione con un intervallo di ricorrenza giornaliera di 9 am.</span><span class="sxs-lookup"><span data-stu-id="3a284-109">This command creates a new trigger AdsTrigger for share subscription AdsShareSubscription with a daily recurrence interval of 9 am.</span></span>

## <span data-ttu-id="3a284-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3a284-110">PARAMETERS</span></span>

### <span data-ttu-id="3a284-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3a284-111">-AccountName</span></span>
<span data-ttu-id="3a284-112">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="3a284-112">Azure data share account name</span></span>

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

### <span data-ttu-id="3a284-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a284-113">-AsJob</span></span>
<span data-ttu-id="3a284-114">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="3a284-114">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="3a284-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a284-115">-DefaultProfile</span></span>
<span data-ttu-id="3a284-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3a284-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a284-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a284-117">-Name</span></span>
<span data-ttu-id="3a284-118">Nome del trigger di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="3a284-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="3a284-119">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="3a284-119">-RecurrenceInterval</span></span>
<span data-ttu-id="3a284-120">Intervallo di ricorrenza per il trigger (giorno o ora)</span><span class="sxs-lookup"><span data-stu-id="3a284-120">The recurrence interval for the trigger (Day or Hour)</span></span>

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

### <span data-ttu-id="3a284-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a284-121">-ResourceGroupName</span></span>
<span data-ttu-id="3a284-122">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="3a284-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="3a284-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="3a284-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="3a284-124">Nome dell'abbonamento a condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="3a284-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="3a284-125">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="3a284-125">-SynchronizationTime</span></span>
<span data-ttu-id="3a284-126">Ora di inizio della sincronizzazione pianificata per il trigger</span><span class="sxs-lookup"><span data-stu-id="3a284-126">The start time of the scheduled synchronization for the trigger</span></span>

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

### <span data-ttu-id="3a284-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3a284-127">-Confirm</span></span>
<span data-ttu-id="3a284-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a284-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a284-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a284-129">-WhatIf</span></span>
<span data-ttu-id="3a284-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a284-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a284-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a284-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a284-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a284-132">CommonParameters</span></span>
<span data-ttu-id="3a284-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a284-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a284-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a284-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a284-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3a284-135">INPUTS</span></span>

### <span data-ttu-id="3a284-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3a284-136">None</span></span>

## <span data-ttu-id="3a284-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a284-137">OUTPUTS</span></span>

### <span data-ttu-id="3a284-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="3a284-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="3a284-139">Note</span><span class="sxs-lookup"><span data-stu-id="3a284-139">NOTES</span></span>

## <span data-ttu-id="3a284-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a284-140">RELATED LINKS</span></span>