---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/stop-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: e865098b0c85227baf1f537fb22c40ee351902fd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191599"
---
# <span data-ttu-id="8a253-101">Stop-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="8a253-101">Stop-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="8a253-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a253-102">SYNOPSIS</span></span>
<span data-ttu-id="8a253-103">Interrompe la sincronizzazione in corso per un abbonamento a una condivisione.</span><span class="sxs-lookup"><span data-stu-id="8a253-103">Stops ongoing synchronization for a share subscription.</span></span> <span data-ttu-id="8a253-104">Un abbonamento A una condivisione può essere specificato tramite il relativo ID risorsa o il relativo nome.</span><span class="sxs-lookup"><span data-stu-id="8a253-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="8a253-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a253-105">SYNTAX</span></span>

### <span data-ttu-id="8a253-106">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8a253-106">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a253-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a253-107">ByResourceIdParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -SynchronizationId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a253-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a253-108">ByObjectParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a253-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a253-109">DESCRIPTION</span></span>
<span data-ttu-id="8a253-110">Il cmdlet **Stop-AzDataShareSubscriptionSynchronization** interrompe la sincronizzazione in corso per un abbonamento a una condivisione</span><span class="sxs-lookup"><span data-stu-id="8a253-110">The **Stop-AzDataShareSubscriptionSynchronization** cmdlet stops ongoing synchronization for a share subscription</span></span>

## <span data-ttu-id="8a253-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a253-111">EXAMPLES</span></span>

### <span data-ttu-id="8a253-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8a253-112">Example 1</span></span>
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

<span data-ttu-id="8a253-113">Interrompe la sincronizzazione in corso identificata da ID-20a4416b-b33b-4539-A908-71dc8ef698fb</span><span class="sxs-lookup"><span data-stu-id="8a253-113">Stops ongoing synchronization identified by id - 20a4416b-b33b-4539-a908-71dc8ef698fb</span></span>

## <span data-ttu-id="8a253-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a253-114">PARAMETERS</span></span>

### <span data-ttu-id="8a253-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8a253-115">-AccountName</span></span>
<span data-ttu-id="8a253-116">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="8a253-116">Azure data share account name</span></span>

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

### <span data-ttu-id="8a253-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a253-117">-AsJob</span></span>
<span data-ttu-id="8a253-118">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="8a253-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="8a253-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a253-119">-DefaultProfile</span></span>
<span data-ttu-id="8a253-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8a253-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a253-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a253-121">-InputObject</span></span>
<span data-ttu-id="8a253-122">Oggetto abbonamento a condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="8a253-122">Azure data share subscription object</span></span>


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

### <span data-ttu-id="8a253-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a253-123">-ResourceGroupName</span></span>
<span data-ttu-id="8a253-124">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="8a253-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="8a253-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a253-125">-ResourceId</span></span>
<span data-ttu-id="8a253-126">ID risorsa dell'abbonamento a una condivisione di Azure</span><span class="sxs-lookup"><span data-stu-id="8a253-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="8a253-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="8a253-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="8a253-128">Nome dell'abbonamento a condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="8a253-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="8a253-129">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="8a253-129">-SynchronizationId</span></span>
<span data-ttu-id="8a253-130">ID sincronizzazione che deve essere interrotto</span><span class="sxs-lookup"><span data-stu-id="8a253-130">Synchronization id that needs to be stopped</span></span>

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

### <span data-ttu-id="8a253-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8a253-131">-Confirm</span></span>
<span data-ttu-id="8a253-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a253-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a253-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a253-133">-WhatIf</span></span>
<span data-ttu-id="8a253-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a253-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a253-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a253-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a253-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a253-136">CommonParameters</span></span>
<span data-ttu-id="8a253-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a253-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a253-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a253-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a253-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a253-139">INPUTS</span></span>

### <span data-ttu-id="8a253-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8a253-140">System.String</span></span>

### <span data-ttu-id="8a253-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="8a253-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="8a253-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a253-142">OUTPUTS</span></span>

### <span data-ttu-id="8a253-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="8a253-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="8a253-144">Note</span><span class="sxs-lookup"><span data-stu-id="8a253-144">NOTES</span></span>

## <span data-ttu-id="8a253-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a253-145">RELATED LINKS</span></span>
