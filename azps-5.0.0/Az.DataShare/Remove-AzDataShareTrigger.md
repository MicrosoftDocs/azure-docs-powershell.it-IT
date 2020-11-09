---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
ms.openlocfilehash: f4eff969d93f1c243b9dc15652249bc9800bfd45
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297367"
---
# <span data-ttu-id="eefaf-101">Remove-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="eefaf-101">Remove-AzDataShareTrigger</span></span>

## <span data-ttu-id="eefaf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eefaf-102">SYNOPSIS</span></span>
<span data-ttu-id="eefaf-103">Rimuove un trigger</span><span class="sxs-lookup"><span data-stu-id="eefaf-103">removes a trigger</span></span>

## <span data-ttu-id="eefaf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eefaf-104">SYNTAX</span></span>

### <span data-ttu-id="eefaf-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eefaf-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eefaf-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eefaf-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareTrigger -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eefaf-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eefaf-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareTrigger -InputObject <PSDataShareTrigger> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eefaf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eefaf-108">DESCRIPTION</span></span>
<span data-ttu-id="eefaf-109">Il cmdlet **Remove-AzDataShareTrigger** rimuove un trigger DataShare</span><span class="sxs-lookup"><span data-stu-id="eefaf-109">The **Remove-AzDataShareTrigger** cmdlet removes a datashare trigger</span></span>

## <span data-ttu-id="eefaf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eefaf-110">EXAMPLES</span></span>

### <span data-ttu-id="eefaf-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="eefaf-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

Are you sure you want to remove trigger "AdsTrigger"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="eefaf-112">Questo comando rimuove un trigger denominato AdsTrigger da Share Subscription AdsShareSubscription.</span><span class="sxs-lookup"><span data-stu-id="eefaf-112">This commands removes a trigger named AdsTrigger from share subscription AdsShareSubscription.</span></span> 

## <span data-ttu-id="eefaf-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eefaf-113">PARAMETERS</span></span>

### <span data-ttu-id="eefaf-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eefaf-114">-AccountName</span></span>
<span data-ttu-id="eefaf-115">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="eefaf-115">Azure data share account name</span></span>

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

### <span data-ttu-id="eefaf-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eefaf-116">-AsJob</span></span>
<span data-ttu-id="eefaf-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="eefaf-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="eefaf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eefaf-118">-DefaultProfile</span></span>
<span data-ttu-id="eefaf-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eefaf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eefaf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eefaf-120">-InputObject</span></span>
<span data-ttu-id="eefaf-121">Oggetto trigger di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="eefaf-121">Azure data share trigger object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eefaf-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="eefaf-122">-Name</span></span>
<span data-ttu-id="eefaf-123">Nome del trigger di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="eefaf-123">Azure data share trigger name</span></span>

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

### <span data-ttu-id="eefaf-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eefaf-124">-PassThru</span></span>
<span data-ttu-id="eefaf-125">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="eefaf-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="eefaf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eefaf-126">-ResourceGroupName</span></span>
<span data-ttu-id="eefaf-127">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="eefaf-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="eefaf-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eefaf-128">-ResourceId</span></span>
<span data-ttu-id="eefaf-129">ID risorsa del trigger di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="eefaf-129">The resource id of azure data share trigger</span></span>

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

### <span data-ttu-id="eefaf-130">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="eefaf-130">-ShareSubscriptionName</span></span>
<span data-ttu-id="eefaf-131">Nome dell'abbonamento a condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="eefaf-131">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eefaf-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="eefaf-132">-Confirm</span></span>
<span data-ttu-id="eefaf-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eefaf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eefaf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eefaf-134">-WhatIf</span></span>
<span data-ttu-id="eefaf-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eefaf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eefaf-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eefaf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eefaf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eefaf-137">CommonParameters</span></span>
<span data-ttu-id="eefaf-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eefaf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eefaf-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eefaf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eefaf-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eefaf-140">INPUTS</span></span>

### <span data-ttu-id="eefaf-141">System. String</span><span class="sxs-lookup"><span data-stu-id="eefaf-141">System.String</span></span>

### <span data-ttu-id="eefaf-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="eefaf-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="eefaf-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eefaf-143">OUTPUTS</span></span>

### <span data-ttu-id="eefaf-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eefaf-144">System.Boolean</span></span>

## <span data-ttu-id="eefaf-145">Note</span><span class="sxs-lookup"><span data-stu-id="eefaf-145">NOTES</span></span>

## <span data-ttu-id="eefaf-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eefaf-146">RELATED LINKS</span></span>
