---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
ms.openlocfilehash: f4eff969d93f1c243b9dc15652249bc9800bfd45
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204322"
---
# <span data-ttu-id="018ce-101">Remove-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="018ce-101">Remove-AzDataShareTrigger</span></span>

## <span data-ttu-id="018ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="018ce-102">SYNOPSIS</span></span>
<span data-ttu-id="018ce-103">rimuove un trigger</span><span class="sxs-lookup"><span data-stu-id="018ce-103">removes a trigger</span></span>

## <span data-ttu-id="018ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="018ce-104">SYNTAX</span></span>

### <span data-ttu-id="018ce-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="018ce-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="018ce-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="018ce-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareTrigger -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="018ce-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="018ce-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareTrigger -InputObject <PSDataShareTrigger> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="018ce-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="018ce-108">DESCRIPTION</span></span>
<span data-ttu-id="018ce-109">Il cmdlet **Remove-AzDataShareTrigger** rimuove un trigger di condivisione dati</span><span class="sxs-lookup"><span data-stu-id="018ce-109">The **Remove-AzDataShareTrigger** cmdlet removes a datashare trigger</span></span>

## <span data-ttu-id="018ce-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="018ce-110">EXAMPLES</span></span>

### <span data-ttu-id="018ce-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="018ce-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

Are you sure you want to remove trigger "AdsTrigger"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="018ce-112">Questo comando rimuove un trigger denominato AdsTrigger dalla sottoscrizione di condivisione AdsShareSubscription.</span><span class="sxs-lookup"><span data-stu-id="018ce-112">This commands removes a trigger named AdsTrigger from share subscription AdsShareSubscription.</span></span> 

## <span data-ttu-id="018ce-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="018ce-113">PARAMETERS</span></span>

### <span data-ttu-id="018ce-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="018ce-114">-AccountName</span></span>
<span data-ttu-id="018ce-115">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="018ce-115">Azure data share account name</span></span>

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

### <span data-ttu-id="018ce-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="018ce-116">-AsJob</span></span>
<span data-ttu-id="018ce-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="018ce-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="018ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="018ce-118">-DefaultProfile</span></span>
<span data-ttu-id="018ce-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="018ce-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="018ce-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="018ce-120">-InputObject</span></span>
<span data-ttu-id="018ce-121">Oggetto trigger condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="018ce-121">Azure data share trigger object</span></span>


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

### <span data-ttu-id="018ce-122">-Name</span><span class="sxs-lookup"><span data-stu-id="018ce-122">-Name</span></span>
<span data-ttu-id="018ce-123">Nome trigger condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="018ce-123">Azure data share trigger name</span></span>

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

### <span data-ttu-id="018ce-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="018ce-124">-PassThru</span></span>
<span data-ttu-id="018ce-125">Oggetto restituito (se specificato).</span><span class="sxs-lookup"><span data-stu-id="018ce-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="018ce-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="018ce-126">-ResourceGroupName</span></span>
<span data-ttu-id="018ce-127">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="018ce-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="018ce-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="018ce-128">-ResourceId</span></span>
<span data-ttu-id="018ce-129">Trigger per l'ID risorsa della condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="018ce-129">The resource id of azure data share trigger</span></span>

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

### <span data-ttu-id="018ce-130">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="018ce-130">-ShareSubscriptionName</span></span>
<span data-ttu-id="018ce-131">Nome della sottoscrizione per la condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="018ce-131">Azure data share subscription name</span></span>

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

### <span data-ttu-id="018ce-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="018ce-132">-Confirm</span></span>
<span data-ttu-id="018ce-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="018ce-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="018ce-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="018ce-134">-WhatIf</span></span>
<span data-ttu-id="018ce-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="018ce-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="018ce-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="018ce-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="018ce-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="018ce-137">CommonParameters</span></span>
<span data-ttu-id="018ce-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="018ce-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="018ce-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="018ce-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="018ce-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="018ce-140">INPUTS</span></span>

### <span data-ttu-id="018ce-141">System.String</span><span class="sxs-lookup"><span data-stu-id="018ce-141">System.String</span></span>

### <span data-ttu-id="018ce-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="018ce-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="018ce-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="018ce-143">OUTPUTS</span></span>

### <span data-ttu-id="018ce-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="018ce-144">System.Boolean</span></span>

## <span data-ttu-id="018ce-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="018ce-145">NOTES</span></span>

## <span data-ttu-id="018ce-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="018ce-146">RELATED LINKS</span></span>
