---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/start-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: 2f0b5cd19e0f21a416c9fd5f3a32462eea86cc4a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674637"
---
# <span data-ttu-id="fdc34-101">Start-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="fdc34-101">Start-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="fdc34-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fdc34-102">SYNOPSIS</span></span>
<span data-ttu-id="fdc34-103">Avvia la sincronizzazione per un abbonamento a una condivisione.</span><span class="sxs-lookup"><span data-stu-id="fdc34-103">Initiates synchronization for a share subscription.</span></span> <span data-ttu-id="fdc34-104">Un abbonamento A una condivisione può essere specificato tramite il relativo ID risorsa o il relativo nome.</span><span class="sxs-lookup"><span data-stu-id="fdc34-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="fdc34-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fdc34-105">SYNTAX</span></span>

### <span data-ttu-id="fdc34-106">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fdc34-106">ByFieldsParameterSet (Default)</span></span>
```
Start-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationMode <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdc34-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdc34-107">ByResourceIdParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -SynchronizationMode <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdc34-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdc34-108">ByObjectParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdc34-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fdc34-109">DESCRIPTION</span></span>
<span data-ttu-id="fdc34-110">Il cmdlet **Start-AzDataShareSubscriptionSynchronization** avvia la sincronizzazione per un abbonamento a una condivisione</span><span class="sxs-lookup"><span data-stu-id="fdc34-110">The **Start-AzDataShareSubscriptionSynchronization** cmdlet initiates synchronization for a share subscription</span></span>

## <span data-ttu-id="fdc34-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fdc34-111">EXAMPLES</span></span>

### <span data-ttu-id="fdc34-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fdc34-112">Example 1</span></span>
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

<span data-ttu-id="fdc34-113">Questo comando avvia la sincronizzazione per un sharesubscription denominato AdsShareSubscription nell'account WikiAds.</span><span class="sxs-lookup"><span data-stu-id="fdc34-113">This commands initiates synchronization for a sharesubscription named AdsShareSubscription in account WikiAds.</span></span> 

## <span data-ttu-id="fdc34-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fdc34-114">PARAMETERS</span></span>

### <span data-ttu-id="fdc34-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fdc34-115">-AccountName</span></span>
<span data-ttu-id="fdc34-116">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="fdc34-116">Azure data share account name</span></span>

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

### <span data-ttu-id="fdc34-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fdc34-117">-AsJob</span></span>
<span data-ttu-id="fdc34-118">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="fdc34-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="fdc34-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdc34-119">-DefaultProfile</span></span>
<span data-ttu-id="fdc34-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fdc34-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdc34-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdc34-121">-InputObject</span></span>
<span data-ttu-id="fdc34-122">Oggetto abbonamento a condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="fdc34-122">Azure data share subscription object</span></span>


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

### <span data-ttu-id="fdc34-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdc34-123">-ResourceGroupName</span></span>
<span data-ttu-id="fdc34-124">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="fdc34-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="fdc34-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdc34-125">-ResourceId</span></span>
<span data-ttu-id="fdc34-126">ID risorsa dell'abbonamento a una condivisione di Azure</span><span class="sxs-lookup"><span data-stu-id="fdc34-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="fdc34-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="fdc34-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="fdc34-128">Nome dell'abbonamento a condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="fdc34-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="fdc34-129">-SynchronizationMode</span><span class="sxs-lookup"><span data-stu-id="fdc34-129">-SynchronizationMode</span></span>
<span data-ttu-id="fdc34-130">Modalità di sincronizzazione (FullSync o incrementale)</span><span class="sxs-lookup"><span data-stu-id="fdc34-130">Synchronization mode (FullSync or Incremental)</span></span>

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

### <span data-ttu-id="fdc34-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fdc34-131">-Confirm</span></span>
<span data-ttu-id="fdc34-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdc34-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdc34-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdc34-133">-WhatIf</span></span>
<span data-ttu-id="fdc34-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fdc34-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdc34-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fdc34-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdc34-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdc34-136">CommonParameters</span></span>
<span data-ttu-id="fdc34-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdc34-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdc34-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdc34-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdc34-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fdc34-139">INPUTS</span></span>

### <span data-ttu-id="fdc34-140">System. String</span><span class="sxs-lookup"><span data-stu-id="fdc34-140">System.String</span></span>

### <span data-ttu-id="fdc34-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="fdc34-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="fdc34-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fdc34-142">OUTPUTS</span></span>

### <span data-ttu-id="fdc34-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="fdc34-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="fdc34-144">Note</span><span class="sxs-lookup"><span data-stu-id="fdc34-144">NOTES</span></span>

## <span data-ttu-id="fdc34-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fdc34-145">RELATED LINKS</span></span>
