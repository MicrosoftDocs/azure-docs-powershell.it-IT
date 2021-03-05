---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/start-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: b2fe61d4493fea64f4ee7b07bdd14905fb7661db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966510"
---
# <span data-ttu-id="a4d87-101">Start-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="a4d87-101">Start-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="a4d87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4d87-102">SYNOPSIS</span></span>
<span data-ttu-id="a4d87-103">Avvia la sincronizzazione per una sottoscrizione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="a4d87-103">Initiates synchronization for a share subscription.</span></span> <span data-ttu-id="a4d87-104">È possibile specificare una sottoscrizione di condivisione tramite il relativo ID risorsa o il relativo nome.</span><span class="sxs-lookup"><span data-stu-id="a4d87-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="a4d87-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4d87-105">SYNTAX</span></span>

### <span data-ttu-id="a4d87-106">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a4d87-106">ByFieldsParameterSet (Default)</span></span>
```
Start-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationMode <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4d87-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4d87-107">ByResourceIdParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -SynchronizationMode <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4d87-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4d87-108">ByObjectParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4d87-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a4d87-109">DESCRIPTION</span></span>
<span data-ttu-id="a4d87-110">Il cmdlet **Start-AzDataShareSubscriptionSynchronization** avvia la sincronizzazione per una sottoscrizione di condivisione</span><span class="sxs-lookup"><span data-stu-id="a4d87-110">The **Start-AzDataShareSubscriptionSynchronization** cmdlet initiates synchronization for a share subscription</span></span>

## <span data-ttu-id="a4d87-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4d87-111">EXAMPLES</span></span>

### <span data-ttu-id="a4d87-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a4d87-112">Example 1</span></span>
```
PS C:\> Start-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationMode Incremental

Confirm
AdsShareSubscription
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

durationMs        : 231869
endTime           : 7/9/2019 11:44:41 PM
message           :
startTime         : 7/9/2019 11:40:53 PM
status            : Succeeded
synchronizationId : 20a4416b-b33b-4539-a908-71dc8ef698fb
```

<span data-ttu-id="a4d87-113">Questo comando avvia la sincronizzazione per una sottoscrizione di condivisione denominata AdsShareSubscription nell'account WikiAds.</span><span class="sxs-lookup"><span data-stu-id="a4d87-113">This commands initiates synchronization for a sharesubscription named AdsShareSubscription in account WikiAds.</span></span> 

## <span data-ttu-id="a4d87-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4d87-114">PARAMETERS</span></span>

### <span data-ttu-id="a4d87-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a4d87-115">-AccountName</span></span>
<span data-ttu-id="a4d87-116">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="a4d87-116">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4d87-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4d87-117">-AsJob</span></span>
<span data-ttu-id="a4d87-118">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="a4d87-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="a4d87-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4d87-119">-DefaultProfile</span></span>
<span data-ttu-id="a4d87-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a4d87-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4d87-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4d87-121">-InputObject</span></span>
<span data-ttu-id="a4d87-122">Oggetto sottoscrizione della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="a4d87-122">Azure data share subscription object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4d87-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4d87-123">-ResourceGroupName</span></span>
<span data-ttu-id="a4d87-124">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="a4d87-124">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4d87-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4d87-125">-ResourceId</span></span>
<span data-ttu-id="a4d87-126">ID risorsa della sottoscrizione di condivisione di Azure</span><span class="sxs-lookup"><span data-stu-id="a4d87-126">The resource id of the azure share subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4d87-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a4d87-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="a4d87-128">Nome della sottoscrizione per la condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="a4d87-128">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4d87-129">-SynchronizationMode</span><span class="sxs-lookup"><span data-stu-id="a4d87-129">-SynchronizationMode</span></span>
<span data-ttu-id="a4d87-130">Modalità di sincronizzazione (FullSync o Incrementale)</span><span class="sxs-lookup"><span data-stu-id="a4d87-130">Synchronization mode (FullSync or Incremental)</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4d87-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4d87-131">-Confirm</span></span>
<span data-ttu-id="a4d87-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4d87-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4d87-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4d87-133">-WhatIf</span></span>
<span data-ttu-id="a4d87-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4d87-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4d87-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4d87-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4d87-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4d87-136">CommonParameters</span></span>
<span data-ttu-id="a4d87-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4d87-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4d87-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a4d87-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4d87-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="a4d87-139">INPUTS</span></span>

### <span data-ttu-id="a4d87-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a4d87-140">System.String</span></span>

### <span data-ttu-id="a4d87-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="a4d87-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="a4d87-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4d87-142">OUTPUTS</span></span>

### <span data-ttu-id="a4d87-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="a4d87-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="a4d87-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="a4d87-144">NOTES</span></span>

## <span data-ttu-id="a4d87-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4d87-145">RELATED LINKS</span></span>
