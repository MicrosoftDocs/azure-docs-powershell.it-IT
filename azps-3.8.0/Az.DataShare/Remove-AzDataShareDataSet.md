---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
ms.openlocfilehash: 1d9566bedbb3e7479f1e9e00c3cc179a225cab2e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020826"
---
# <span data-ttu-id="f333d-101">Remove-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="f333d-101">Remove-AzDataShareDataSet</span></span>

## <span data-ttu-id="f333d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f333d-102">SYNOPSIS</span></span>
<span data-ttu-id="f333d-103">Rimuove un mapping del DataSet</span><span class="sxs-lookup"><span data-stu-id="f333d-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="f333d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f333d-104">SYNTAX</span></span>

### <span data-ttu-id="f333d-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f333d-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f333d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f333d-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f333d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f333d-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSet -InputObject <PSDataShareDataSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f333d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f333d-108">DESCRIPTION</span></span>
<span data-ttu-id="f333d-109">Il cmdlet **Remove-AzDataShareDataSet** rimuove un set di dati.</span><span class="sxs-lookup"><span data-stu-id="f333d-109">The **Remove-AzDataShareDataSet** cmdlet removes a dataset.</span></span>

## <span data-ttu-id="f333d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f333d-110">EXAMPLES</span></span>

### <span data-ttu-id="f333d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f333d-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "DS"
Are you sure you want to remove dataset mapping "DS"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="f333d-112">Questo comando rimuove il DataSet denominato DS da Share WikiAds.</span><span class="sxs-lookup"><span data-stu-id="f333d-112">This commands removes the dataset named DS from share WikiAds.</span></span> 

## <span data-ttu-id="f333d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f333d-113">PARAMETERS</span></span>

### <span data-ttu-id="f333d-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f333d-114">-AccountName</span></span>
<span data-ttu-id="f333d-115">Nome dell'account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="f333d-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="f333d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f333d-116">-DefaultProfile</span></span>
<span data-ttu-id="f333d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f333d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f333d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f333d-118">-InputObject</span></span>
<span data-ttu-id="f333d-119">Oggetto set di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="f333d-119">The azure data set object.</span></span>


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

### <span data-ttu-id="f333d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f333d-120">-Name</span></span>
<span data-ttu-id="f333d-121">Nome del set di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="f333d-121">Azure data set name.</span></span>

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

### <span data-ttu-id="f333d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f333d-122">-PassThru</span></span>
<span data-ttu-id="f333d-123">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="f333d-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="f333d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f333d-124">-ResourceGroupName</span></span>
<span data-ttu-id="f333d-125">Nome del gruppo di risorse dell'account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="f333d-125">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="f333d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f333d-126">-ResourceId</span></span>
<span data-ttu-id="f333d-127">ID risorsa del set di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="f333d-127">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="f333d-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="f333d-128">-ShareName</span></span>
<span data-ttu-id="f333d-129">Nome della condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="f333d-129">Azure data share name.</span></span>

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

### <span data-ttu-id="f333d-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f333d-130">-Confirm</span></span>
<span data-ttu-id="f333d-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f333d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f333d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f333d-132">-WhatIf</span></span>
<span data-ttu-id="f333d-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f333d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f333d-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f333d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f333d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f333d-135">CommonParameters</span></span>
<span data-ttu-id="f333d-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f333d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f333d-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f333d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f333d-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f333d-138">INPUTS</span></span>

### <span data-ttu-id="f333d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f333d-139">System.String</span></span>

### <span data-ttu-id="f333d-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="f333d-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="f333d-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f333d-141">OUTPUTS</span></span>

### <span data-ttu-id="f333d-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f333d-142">System.Boolean</span></span>

## <span data-ttu-id="f333d-143">Note</span><span class="sxs-lookup"><span data-stu-id="f333d-143">NOTES</span></span>

## <span data-ttu-id="f333d-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f333d-144">RELATED LINKS</span></span>
