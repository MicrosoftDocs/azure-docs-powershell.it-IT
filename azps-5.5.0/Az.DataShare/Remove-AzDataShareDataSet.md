---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
ms.openlocfilehash: c3d5105fc3b43a3f6b7ff8b45c5ba8236fed656b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194575"
---
# <span data-ttu-id="3d90f-101">Remove-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="3d90f-101">Remove-AzDataShareDataSet</span></span>

## <span data-ttu-id="3d90f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d90f-102">SYNOPSIS</span></span>
<span data-ttu-id="3d90f-103">Rimuove un mapping del set di dati</span><span class="sxs-lookup"><span data-stu-id="3d90f-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="3d90f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d90f-104">SYNTAX</span></span>

### <span data-ttu-id="3d90f-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3d90f-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d90f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d90f-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d90f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d90f-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSet -InputObject <PSDataShareDataSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d90f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3d90f-108">DESCRIPTION</span></span>
<span data-ttu-id="3d90f-109">Il cmdlet **Remove-AzDataShareDataSet** rimuove un set di dati.</span><span class="sxs-lookup"><span data-stu-id="3d90f-109">The **Remove-AzDataShareDataSet** cmdlet removes a dataset.</span></span>

## <span data-ttu-id="3d90f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d90f-110">EXAMPLES</span></span>

### <span data-ttu-id="3d90f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3d90f-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "DS"
Are you sure you want to remove dataset mapping "DS"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="3d90f-112">Questo comando rimuove il set di dati denominato DS dalla condivisione di WikiAds.</span><span class="sxs-lookup"><span data-stu-id="3d90f-112">This commands removes the dataset named DS from share WikiAds.</span></span> 

## <span data-ttu-id="3d90f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d90f-113">PARAMETERS</span></span>

### <span data-ttu-id="3d90f-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3d90f-114">-AccountName</span></span>
<span data-ttu-id="3d90f-115">Nome dell'account per la condivisione dei dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="3d90f-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="3d90f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d90f-116">-DefaultProfile</span></span>
<span data-ttu-id="3d90f-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3d90f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d90f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d90f-118">-InputObject</span></span>
<span data-ttu-id="3d90f-119">Oggetto set di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="3d90f-119">The azure data set object.</span></span>


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

### <span data-ttu-id="3d90f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3d90f-120">-Name</span></span>
<span data-ttu-id="3d90f-121">Nome del set di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="3d90f-121">Azure data set name.</span></span>

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

### <span data-ttu-id="3d90f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d90f-122">-PassThru</span></span>
<span data-ttu-id="3d90f-123">Oggetto restituito (se specificato).</span><span class="sxs-lookup"><span data-stu-id="3d90f-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="3d90f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d90f-124">-ResourceGroupName</span></span>
<span data-ttu-id="3d90f-125">Nome del gruppo di risorse dell'account di condivisione dei dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="3d90f-125">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="3d90f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d90f-126">-ResourceId</span></span>
<span data-ttu-id="3d90f-127">ID della risorsa del set di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="3d90f-127">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="3d90f-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="3d90f-128">-ShareName</span></span>
<span data-ttu-id="3d90f-129">Nome della condivisione dei dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="3d90f-129">Azure data share name.</span></span>

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

### <span data-ttu-id="3d90f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d90f-130">-Confirm</span></span>
<span data-ttu-id="3d90f-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d90f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d90f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d90f-132">-WhatIf</span></span>
<span data-ttu-id="3d90f-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3d90f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d90f-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3d90f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d90f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d90f-135">CommonParameters</span></span>
<span data-ttu-id="3d90f-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d90f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d90f-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3d90f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d90f-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="3d90f-138">INPUTS</span></span>

### <span data-ttu-id="3d90f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3d90f-139">System.String</span></span>

### <span data-ttu-id="3d90f-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="3d90f-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="3d90f-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d90f-141">OUTPUTS</span></span>

### <span data-ttu-id="3d90f-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3d90f-142">System.Boolean</span></span>

## <span data-ttu-id="3d90f-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="3d90f-143">NOTES</span></span>

## <span data-ttu-id="3d90f-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d90f-144">RELATED LINKS</span></span>
