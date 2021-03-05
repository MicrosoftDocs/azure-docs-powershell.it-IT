---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 8e3513621b94a7fc98a00b7eb443bef18d2a8141
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988230"
---
# <span data-ttu-id="2ffb8-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="2ffb8-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="2ffb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ffb8-102">SYNOPSIS</span></span>
<span data-ttu-id="2ffb8-103">Rimuove un mapping del set di dati</span><span class="sxs-lookup"><span data-stu-id="2ffb8-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="2ffb8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ffb8-104">SYNTAX</span></span>

### <span data-ttu-id="2ffb8-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2ffb8-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ffb8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ffb8-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ffb8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ffb8-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ffb8-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2ffb8-108">DESCRIPTION</span></span>
<span data-ttu-id="2ffb8-109">Il cmdlet **Remove-AzDataShareDataSetMapping** rimuove i mapping di un set di dati.</span><span class="sxs-lookup"><span data-stu-id="2ffb8-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="2ffb8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ffb8-110">EXAMPLES</span></span>

### <span data-ttu-id="2ffb8-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2ffb8-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="2ffb8-112">Questo comando rimuove il set di dati denominato DSM da WikiAds sharesubscription.</span><span class="sxs-lookup"><span data-stu-id="2ffb8-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="2ffb8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ffb8-113">PARAMETERS</span></span>

### <span data-ttu-id="2ffb8-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2ffb8-114">-AccountName</span></span>
<span data-ttu-id="2ffb8-115">Nome account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="2ffb8-115">Azure data share account name</span></span>

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

### <span data-ttu-id="2ffb8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ffb8-116">-DefaultProfile</span></span>
<span data-ttu-id="2ffb8-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2ffb8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ffb8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ffb8-118">-InputObject</span></span>
<span data-ttu-id="2ffb8-119">Oggetto mapping set di dati di Azure</span><span class="sxs-lookup"><span data-stu-id="2ffb8-119">The azure data set mapping object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ffb8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2ffb8-120">-Name</span></span>
<span data-ttu-id="2ffb8-121">Nome mapping set di dati di Azure</span><span class="sxs-lookup"><span data-stu-id="2ffb8-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="2ffb8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ffb8-122">-PassThru</span></span>
<span data-ttu-id="2ffb8-123">Oggetto restituito (se specificato).</span><span class="sxs-lookup"><span data-stu-id="2ffb8-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="2ffb8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ffb8-124">-ResourceGroupName</span></span>
<span data-ttu-id="2ffb8-125">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="2ffb8-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="2ffb8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ffb8-126">-ResourceId</span></span>
<span data-ttu-id="2ffb8-127">ID risorsa del mapping del set di dati di Azure</span><span class="sxs-lookup"><span data-stu-id="2ffb8-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="2ffb8-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="2ffb8-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="2ffb8-129">Nome della sottoscrizione per la condivisione dei dati di Azure</span><span class="sxs-lookup"><span data-stu-id="2ffb8-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="2ffb8-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ffb8-130">-Confirm</span></span>
<span data-ttu-id="2ffb8-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ffb8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ffb8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ffb8-132">-WhatIf</span></span>
<span data-ttu-id="2ffb8-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ffb8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ffb8-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ffb8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ffb8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ffb8-135">CommonParameters</span></span>
<span data-ttu-id="2ffb8-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ffb8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ffb8-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2ffb8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ffb8-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="2ffb8-138">INPUTS</span></span>

### <span data-ttu-id="2ffb8-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2ffb8-139">System.String</span></span>

### <span data-ttu-id="2ffb8-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="2ffb8-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="2ffb8-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ffb8-141">OUTPUTS</span></span>

### <span data-ttu-id="2ffb8-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2ffb8-142">System.Boolean</span></span>

## <span data-ttu-id="2ffb8-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="2ffb8-143">NOTES</span></span>

## <span data-ttu-id="2ffb8-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ffb8-144">RELATED LINKS</span></span>
