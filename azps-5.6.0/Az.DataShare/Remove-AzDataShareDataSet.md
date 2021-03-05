---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
ms.openlocfilehash: 8ede4fe94eccd9d9f08977a0af9cc8847e4aca1f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004237"
---
# <span data-ttu-id="b5da7-101">Remove-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="b5da7-101">Remove-AzDataShareDataSet</span></span>

## <span data-ttu-id="b5da7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5da7-102">SYNOPSIS</span></span>
<span data-ttu-id="b5da7-103">Rimuove un mapping del set di dati</span><span class="sxs-lookup"><span data-stu-id="b5da7-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="b5da7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5da7-104">SYNTAX</span></span>

### <span data-ttu-id="b5da7-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b5da7-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5da7-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5da7-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5da7-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5da7-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSet -InputObject <PSDataShareDataSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5da7-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b5da7-108">DESCRIPTION</span></span>
<span data-ttu-id="b5da7-109">Il cmdlet **Remove-AzDataShareDataSet** rimuove un set di dati.</span><span class="sxs-lookup"><span data-stu-id="b5da7-109">The **Remove-AzDataShareDataSet** cmdlet removes a dataset.</span></span>

## <span data-ttu-id="b5da7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5da7-110">EXAMPLES</span></span>

### <span data-ttu-id="b5da7-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b5da7-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "DS"
Are you sure you want to remove dataset mapping "DS"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="b5da7-112">Questo comando rimuove il set di dati denominato DS dalla condivisione di WikiAds.</span><span class="sxs-lookup"><span data-stu-id="b5da7-112">This commands removes the dataset named DS from share WikiAds.</span></span> 

## <span data-ttu-id="b5da7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5da7-113">PARAMETERS</span></span>

### <span data-ttu-id="b5da7-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b5da7-114">-AccountName</span></span>
<span data-ttu-id="b5da7-115">Nome dell'account per la condivisione dei dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="b5da7-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="b5da7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5da7-116">-DefaultProfile</span></span>
<span data-ttu-id="b5da7-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b5da7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5da7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5da7-118">-InputObject</span></span>
<span data-ttu-id="b5da7-119">Oggetto set di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="b5da7-119">The azure data set object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5da7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b5da7-120">-Name</span></span>
<span data-ttu-id="b5da7-121">Nome del set di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="b5da7-121">Azure data set name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5da7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5da7-122">-PassThru</span></span>
<span data-ttu-id="b5da7-123">Oggetto restituito (se specificato).</span><span class="sxs-lookup"><span data-stu-id="b5da7-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="b5da7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5da7-124">-ResourceGroupName</span></span>
<span data-ttu-id="b5da7-125">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="b5da7-125">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="b5da7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5da7-126">-ResourceId</span></span>
<span data-ttu-id="b5da7-127">ID risorsa del set di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="b5da7-127">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="b5da7-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b5da7-128">-ShareName</span></span>
<span data-ttu-id="b5da7-129">Nome della condivisione dei dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="b5da7-129">Azure data share name.</span></span>

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

### <span data-ttu-id="b5da7-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5da7-130">-Confirm</span></span>
<span data-ttu-id="b5da7-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5da7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5da7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5da7-132">-WhatIf</span></span>
<span data-ttu-id="b5da7-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5da7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5da7-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5da7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5da7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5da7-135">CommonParameters</span></span>
<span data-ttu-id="b5da7-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5da7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5da7-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b5da7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5da7-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="b5da7-138">INPUTS</span></span>

### <span data-ttu-id="b5da7-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b5da7-139">System.String</span></span>

### <span data-ttu-id="b5da7-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="b5da7-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="b5da7-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5da7-141">OUTPUTS</span></span>

### <span data-ttu-id="b5da7-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b5da7-142">System.Boolean</span></span>

## <span data-ttu-id="b5da7-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="b5da7-143">NOTES</span></span>

## <span data-ttu-id="b5da7-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5da7-144">RELATED LINKS</span></span>
