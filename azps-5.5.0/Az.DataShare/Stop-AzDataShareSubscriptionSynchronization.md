---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/stop-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: e865098b0c85227baf1f537fb22c40ee351902fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204315"
---
# <span data-ttu-id="b6aab-101">Stop-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="b6aab-101">Stop-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="b6aab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6aab-102">SYNOPSIS</span></span>
<span data-ttu-id="b6aab-103">Interrompe la sincronizzazione continua per una sottoscrizione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="b6aab-103">Stops ongoing synchronization for a share subscription.</span></span> <span data-ttu-id="b6aab-104">È possibile specificare una sottoscrizione di condivisione tramite il relativo ID risorsa o il relativo nome.</span><span class="sxs-lookup"><span data-stu-id="b6aab-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="b6aab-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6aab-105">SYNTAX</span></span>

### <span data-ttu-id="b6aab-106">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b6aab-106">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6aab-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6aab-107">ByResourceIdParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -SynchronizationId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6aab-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6aab-108">ByObjectParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6aab-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b6aab-109">DESCRIPTION</span></span>
<span data-ttu-id="b6aab-110">Il cmdlet **Stop-AzDataShareSubscriptionSynchronization** interrompe la sincronizzazione continua per una sottoscrizione di condivisione</span><span class="sxs-lookup"><span data-stu-id="b6aab-110">The **Stop-AzDataShareSubscriptionSynchronization** cmdlet stops ongoing synchronization for a share subscription</span></span>

## <span data-ttu-id="b6aab-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6aab-111">EXAMPLES</span></span>

### <span data-ttu-id="b6aab-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b6aab-112">Example 1</span></span>
```
PS C:\> Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationId 20a4416b-b33b-4539-a908-71dc8ef698fb

Confirm
AdsShareSubscription
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

durationMs        : 231869
endTime           : 
message           :
startTime         : 7/9/2019 11:40:53 PM
status            : Canceled
synchronizationId : 20a4416b-b33b-4539-a908-71dc8ef698fb
```

<span data-ttu-id="b6aab-113">Interrompe la sincronizzazione continua identificata da id - 20a4416b-b33b-4539-a908-71dc8ef698fb</span><span class="sxs-lookup"><span data-stu-id="b6aab-113">Stops ongoing synchronization identified by id - 20a4416b-b33b-4539-a908-71dc8ef698fb</span></span>

## <span data-ttu-id="b6aab-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6aab-114">PARAMETERS</span></span>

### <span data-ttu-id="b6aab-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b6aab-115">-AccountName</span></span>
<span data-ttu-id="b6aab-116">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="b6aab-116">Azure data share account name</span></span>

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

### <span data-ttu-id="b6aab-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6aab-117">-AsJob</span></span>
<span data-ttu-id="b6aab-118">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="b6aab-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="b6aab-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6aab-119">-DefaultProfile</span></span>
<span data-ttu-id="b6aab-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6aab-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6aab-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6aab-121">-InputObject</span></span>
<span data-ttu-id="b6aab-122">Oggetto sottoscrizione della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="b6aab-122">Azure data share subscription object</span></span>


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

### <span data-ttu-id="b6aab-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6aab-123">-ResourceGroupName</span></span>
<span data-ttu-id="b6aab-124">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="b6aab-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="b6aab-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6aab-125">-ResourceId</span></span>
<span data-ttu-id="b6aab-126">ID risorsa della sottoscrizione di condivisione di Azure</span><span class="sxs-lookup"><span data-stu-id="b6aab-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="b6aab-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b6aab-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="b6aab-128">Nome della sottoscrizione per la condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="b6aab-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="b6aab-129">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="b6aab-129">-SynchronizationId</span></span>
<span data-ttu-id="b6aab-130">ID sincronizzazione che deve essere interrotto</span><span class="sxs-lookup"><span data-stu-id="b6aab-130">Synchronization id that needs to be stopped</span></span>

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

### <span data-ttu-id="b6aab-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6aab-131">-Confirm</span></span>
<span data-ttu-id="b6aab-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6aab-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6aab-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6aab-133">-WhatIf</span></span>
<span data-ttu-id="b6aab-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6aab-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6aab-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6aab-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6aab-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6aab-136">CommonParameters</span></span>
<span data-ttu-id="b6aab-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6aab-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6aab-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b6aab-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6aab-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="b6aab-139">INPUTS</span></span>

### <span data-ttu-id="b6aab-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b6aab-140">System.String</span></span>

### <span data-ttu-id="b6aab-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="b6aab-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="b6aab-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6aab-142">OUTPUTS</span></span>

### <span data-ttu-id="b6aab-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="b6aab-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="b6aab-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="b6aab-144">NOTES</span></span>

## <span data-ttu-id="b6aab-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6aab-145">RELATED LINKS</span></span>
