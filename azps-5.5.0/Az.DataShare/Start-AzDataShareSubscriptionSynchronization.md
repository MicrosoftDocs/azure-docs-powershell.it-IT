---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/start-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: bbbcab1e4355667681acf1cc09a51ec6d6174103
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186087"
---
# <span data-ttu-id="67842-101">Start-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="67842-101">Start-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="67842-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67842-102">SYNOPSIS</span></span>
<span data-ttu-id="67842-103">Avvia la sincronizzazione per una sottoscrizione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="67842-103">Initiates synchronization for a share subscription.</span></span> <span data-ttu-id="67842-104">È possibile specificare una sottoscrizione di condivisione tramite il relativo ID risorsa o il relativo nome.</span><span class="sxs-lookup"><span data-stu-id="67842-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="67842-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67842-105">SYNTAX</span></span>

### <span data-ttu-id="67842-106">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="67842-106">ByFieldsParameterSet (Default)</span></span>
```
Start-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationMode <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67842-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67842-107">ByResourceIdParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -SynchronizationMode <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67842-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="67842-108">ByObjectParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67842-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="67842-109">DESCRIPTION</span></span>
<span data-ttu-id="67842-110">Il cmdlet **Start-AzDataShareSubscriptionSynchronization** avvia la sincronizzazione per una sottoscrizione di condivisione</span><span class="sxs-lookup"><span data-stu-id="67842-110">The **Start-AzDataShareSubscriptionSynchronization** cmdlet initiates synchronization for a share subscription</span></span>

## <span data-ttu-id="67842-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67842-111">EXAMPLES</span></span>

### <span data-ttu-id="67842-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="67842-112">Example 1</span></span>
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

<span data-ttu-id="67842-113">Questo comando avvia la sincronizzazione per una sottoscrizione di condivisione denominata AdsShareSubscription nell'account WikiAds.</span><span class="sxs-lookup"><span data-stu-id="67842-113">This commands initiates synchronization for a sharesubscription named AdsShareSubscription in account WikiAds.</span></span> 

## <span data-ttu-id="67842-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67842-114">PARAMETERS</span></span>

### <span data-ttu-id="67842-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="67842-115">-AccountName</span></span>
<span data-ttu-id="67842-116">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="67842-116">Azure data share account name</span></span>

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

### <span data-ttu-id="67842-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67842-117">-AsJob</span></span>
<span data-ttu-id="67842-118">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="67842-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="67842-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67842-119">-DefaultProfile</span></span>
<span data-ttu-id="67842-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67842-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67842-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67842-121">-InputObject</span></span>
<span data-ttu-id="67842-122">Oggetto sottoscrizione della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="67842-122">Azure data share subscription object</span></span>


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

### <span data-ttu-id="67842-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67842-123">-ResourceGroupName</span></span>
<span data-ttu-id="67842-124">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="67842-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="67842-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67842-125">-ResourceId</span></span>
<span data-ttu-id="67842-126">ID risorsa della sottoscrizione di condivisione di Azure</span><span class="sxs-lookup"><span data-stu-id="67842-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="67842-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="67842-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="67842-128">Nome della sottoscrizione per la condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="67842-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="67842-129">-SynchronizationMode</span><span class="sxs-lookup"><span data-stu-id="67842-129">-SynchronizationMode</span></span>
<span data-ttu-id="67842-130">Modalità di sincronizzazione (FullSync o Incrementale)</span><span class="sxs-lookup"><span data-stu-id="67842-130">Synchronization mode (FullSync or Incremental)</span></span>

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

### <span data-ttu-id="67842-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67842-131">-Confirm</span></span>
<span data-ttu-id="67842-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67842-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67842-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67842-133">-WhatIf</span></span>
<span data-ttu-id="67842-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67842-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67842-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67842-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67842-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67842-136">CommonParameters</span></span>
<span data-ttu-id="67842-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67842-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67842-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="67842-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67842-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="67842-139">INPUTS</span></span>

### <span data-ttu-id="67842-140">System.String</span><span class="sxs-lookup"><span data-stu-id="67842-140">System.String</span></span>

### <span data-ttu-id="67842-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="67842-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="67842-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67842-142">OUTPUTS</span></span>

### <span data-ttu-id="67842-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="67842-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="67842-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="67842-144">NOTES</span></span>

## <span data-ttu-id="67842-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67842-145">RELATED LINKS</span></span>
