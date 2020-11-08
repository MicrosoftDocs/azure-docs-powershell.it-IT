---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
ms.openlocfilehash: c3d5105fc3b43a3f6b7ff8b45c5ba8236fed656b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031800"
---
# <span data-ttu-id="a0737-101">Remove-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="a0737-101">Remove-AzDataShareDataSet</span></span>

## <span data-ttu-id="a0737-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a0737-102">SYNOPSIS</span></span>
<span data-ttu-id="a0737-103">Rimuove un mapping del DataSet</span><span class="sxs-lookup"><span data-stu-id="a0737-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="a0737-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0737-104">SYNTAX</span></span>

### <span data-ttu-id="a0737-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a0737-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0737-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0737-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0737-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0737-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSet -InputObject <PSDataShareDataSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0737-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0737-108">DESCRIPTION</span></span>
<span data-ttu-id="a0737-109">Il cmdlet **Remove-AzDataShareDataSet** rimuove un set di dati.</span><span class="sxs-lookup"><span data-stu-id="a0737-109">The **Remove-AzDataShareDataSet** cmdlet removes a dataset.</span></span>

## <span data-ttu-id="a0737-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0737-110">EXAMPLES</span></span>

### <span data-ttu-id="a0737-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a0737-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "DS"
Are you sure you want to remove dataset mapping "DS"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="a0737-112">Questo comando rimuove il DataSet denominato DS da Share WikiAds.</span><span class="sxs-lookup"><span data-stu-id="a0737-112">This commands removes the dataset named DS from share WikiAds.</span></span> 

## <span data-ttu-id="a0737-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a0737-113">PARAMETERS</span></span>

### <span data-ttu-id="a0737-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a0737-114">-AccountName</span></span>
<span data-ttu-id="a0737-115">Nome dell'account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="a0737-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="a0737-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0737-116">-DefaultProfile</span></span>
<span data-ttu-id="a0737-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a0737-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0737-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0737-118">-InputObject</span></span>
<span data-ttu-id="a0737-119">Oggetto set di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="a0737-119">The azure data set object.</span></span>


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

### <span data-ttu-id="a0737-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0737-120">-Name</span></span>
<span data-ttu-id="a0737-121">Nome del set di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="a0737-121">Azure data set name.</span></span>

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

### <span data-ttu-id="a0737-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0737-122">-PassThru</span></span>
<span data-ttu-id="a0737-123">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="a0737-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="a0737-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0737-124">-ResourceGroupName</span></span>
<span data-ttu-id="a0737-125">Nome del gruppo di risorse dell'account di condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="a0737-125">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="a0737-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0737-126">-ResourceId</span></span>
<span data-ttu-id="a0737-127">ID risorsa del set di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="a0737-127">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="a0737-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="a0737-128">-ShareName</span></span>
<span data-ttu-id="a0737-129">Nome della condivisione dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="a0737-129">Azure data share name.</span></span>

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

### <span data-ttu-id="a0737-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a0737-130">-Confirm</span></span>
<span data-ttu-id="a0737-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0737-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0737-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0737-132">-WhatIf</span></span>
<span data-ttu-id="a0737-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0737-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0737-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0737-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0737-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0737-135">CommonParameters</span></span>
<span data-ttu-id="a0737-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0737-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0737-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0737-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0737-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a0737-138">INPUTS</span></span>

### <span data-ttu-id="a0737-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a0737-139">System.String</span></span>

### <span data-ttu-id="a0737-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="a0737-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="a0737-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0737-141">OUTPUTS</span></span>

### <span data-ttu-id="a0737-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a0737-142">System.Boolean</span></span>

## <span data-ttu-id="a0737-143">Note</span><span class="sxs-lookup"><span data-stu-id="a0737-143">NOTES</span></span>

## <span data-ttu-id="a0737-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0737-144">RELATED LINKS</span></span>
