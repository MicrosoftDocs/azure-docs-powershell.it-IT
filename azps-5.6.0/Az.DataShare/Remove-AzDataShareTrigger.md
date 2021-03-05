---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
ms.openlocfilehash: 9ee4c8c25f6a9575283c8e5f077be7107756f701
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966526"
---
# <span data-ttu-id="d2dfc-101">Remove-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="d2dfc-101">Remove-AzDataShareTrigger</span></span>

## <span data-ttu-id="d2dfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="d2dfc-103">rimuove un trigger</span><span class="sxs-lookup"><span data-stu-id="d2dfc-103">removes a trigger</span></span>

## <span data-ttu-id="d2dfc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2dfc-104">SYNTAX</span></span>

### <span data-ttu-id="d2dfc-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d2dfc-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2dfc-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2dfc-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareTrigger -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2dfc-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2dfc-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareTrigger -InputObject <PSDataShareTrigger> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2dfc-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d2dfc-108">DESCRIPTION</span></span>
<span data-ttu-id="d2dfc-109">Il cmdlet **Remove-AzDataShareTrigger** rimuove un trigger di condivisione dati</span><span class="sxs-lookup"><span data-stu-id="d2dfc-109">The **Remove-AzDataShareTrigger** cmdlet removes a datashare trigger</span></span>

## <span data-ttu-id="d2dfc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2dfc-110">EXAMPLES</span></span>

### <span data-ttu-id="d2dfc-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d2dfc-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

Are you sure you want to remove trigger "AdsTrigger"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="d2dfc-112">Questo comando rimuove un trigger denominato AdsTrigger dalla sottoscrizione di condivisione AdsShareSubscription.</span><span class="sxs-lookup"><span data-stu-id="d2dfc-112">This commands removes a trigger named AdsTrigger from share subscription AdsShareSubscription.</span></span> 

## <span data-ttu-id="d2dfc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2dfc-113">PARAMETERS</span></span>

### <span data-ttu-id="d2dfc-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d2dfc-114">-AccountName</span></span>
<span data-ttu-id="d2dfc-115">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="d2dfc-115">Azure data share account name</span></span>

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

### <span data-ttu-id="d2dfc-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2dfc-116">-AsJob</span></span>
<span data-ttu-id="d2dfc-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="d2dfc-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="d2dfc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2dfc-118">-DefaultProfile</span></span>
<span data-ttu-id="d2dfc-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d2dfc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2dfc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2dfc-120">-InputObject</span></span>
<span data-ttu-id="d2dfc-121">Oggetto trigger condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="d2dfc-121">Azure data share trigger object</span></span>


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

### <span data-ttu-id="d2dfc-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d2dfc-122">-Name</span></span>
<span data-ttu-id="d2dfc-123">Nome trigger condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="d2dfc-123">Azure data share trigger name</span></span>

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

### <span data-ttu-id="d2dfc-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2dfc-124">-PassThru</span></span>
<span data-ttu-id="d2dfc-125">Oggetto restituito (se specificato).</span><span class="sxs-lookup"><span data-stu-id="d2dfc-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="d2dfc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2dfc-126">-ResourceGroupName</span></span>
<span data-ttu-id="d2dfc-127">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="d2dfc-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="d2dfc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2dfc-128">-ResourceId</span></span>
<span data-ttu-id="d2dfc-129">L'ID risorsa del trigger per la condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="d2dfc-129">The resource id of azure data share trigger</span></span>

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

### <span data-ttu-id="d2dfc-130">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="d2dfc-130">-ShareSubscriptionName</span></span>
<span data-ttu-id="d2dfc-131">Nome della sottoscrizione della condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="d2dfc-131">Azure data share subscription name</span></span>

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

### <span data-ttu-id="d2dfc-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2dfc-132">-Confirm</span></span>
<span data-ttu-id="d2dfc-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2dfc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2dfc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2dfc-134">-WhatIf</span></span>
<span data-ttu-id="d2dfc-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2dfc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2dfc-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2dfc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2dfc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2dfc-137">CommonParameters</span></span>
<span data-ttu-id="d2dfc-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2dfc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2dfc-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d2dfc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2dfc-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="d2dfc-140">INPUTS</span></span>

### <span data-ttu-id="d2dfc-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d2dfc-141">System.String</span></span>

### <span data-ttu-id="d2dfc-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="d2dfc-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="d2dfc-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2dfc-143">OUTPUTS</span></span>

### <span data-ttu-id="d2dfc-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d2dfc-144">System.Boolean</span></span>

## <span data-ttu-id="d2dfc-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="d2dfc-145">NOTES</span></span>

## <span data-ttu-id="d2dfc-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2dfc-146">RELATED LINKS</span></span>
