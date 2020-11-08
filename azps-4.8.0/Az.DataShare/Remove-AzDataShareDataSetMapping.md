---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 16b212a0c5549f74b56e8c80be8d949a025ecb24
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031284"
---
# <span data-ttu-id="ef09e-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="ef09e-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="ef09e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ef09e-102">SYNOPSIS</span></span>
<span data-ttu-id="ef09e-103">Rimuove un mapping del DataSet</span><span class="sxs-lookup"><span data-stu-id="ef09e-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="ef09e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef09e-104">SYNTAX</span></span>

### <span data-ttu-id="ef09e-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ef09e-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef09e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef09e-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef09e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef09e-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef09e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef09e-108">DESCRIPTION</span></span>
<span data-ttu-id="ef09e-109">Il cmdlet **Remove-AzDataShareDataSetMapping** rimuove i mapping di un DataSet.</span><span class="sxs-lookup"><span data-stu-id="ef09e-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="ef09e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef09e-110">EXAMPLES</span></span>

### <span data-ttu-id="ef09e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ef09e-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="ef09e-112">Questo comando rimuove il DataSet denominato DSM da sharesubscription WikiAds.</span><span class="sxs-lookup"><span data-stu-id="ef09e-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="ef09e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ef09e-113">PARAMETERS</span></span>

### <span data-ttu-id="ef09e-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ef09e-114">-AccountName</span></span>
<span data-ttu-id="ef09e-115">Nome dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="ef09e-115">Azure data share account name</span></span>

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

### <span data-ttu-id="ef09e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef09e-116">-DefaultProfile</span></span>
<span data-ttu-id="ef09e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ef09e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef09e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef09e-118">-InputObject</span></span>
<span data-ttu-id="ef09e-119">Oggetto mapping set di dati di Azure</span><span class="sxs-lookup"><span data-stu-id="ef09e-119">The azure data set mapping object</span></span>


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

### <span data-ttu-id="ef09e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ef09e-120">-Name</span></span>
<span data-ttu-id="ef09e-121">Nome del mapping set di dati di Azure</span><span class="sxs-lookup"><span data-stu-id="ef09e-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="ef09e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef09e-122">-PassThru</span></span>
<span data-ttu-id="ef09e-123">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="ef09e-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="ef09e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef09e-124">-ResourceGroupName</span></span>
<span data-ttu-id="ef09e-125">Nome del gruppo di risorse dell'account di condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="ef09e-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="ef09e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef09e-126">-ResourceId</span></span>
<span data-ttu-id="ef09e-127">ID risorsa del mapping del set di dati di Azure</span><span class="sxs-lookup"><span data-stu-id="ef09e-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="ef09e-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ef09e-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="ef09e-129">Nome dell'abbonamento a condivisione dati di Azure</span><span class="sxs-lookup"><span data-stu-id="ef09e-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="ef09e-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ef09e-130">-Confirm</span></span>
<span data-ttu-id="ef09e-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef09e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef09e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef09e-132">-WhatIf</span></span>
<span data-ttu-id="ef09e-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ef09e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef09e-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ef09e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef09e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef09e-135">CommonParameters</span></span>
<span data-ttu-id="ef09e-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef09e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef09e-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef09e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef09e-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ef09e-138">INPUTS</span></span>

### <span data-ttu-id="ef09e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ef09e-139">System.String</span></span>

### <span data-ttu-id="ef09e-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="ef09e-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="ef09e-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef09e-141">OUTPUTS</span></span>

### <span data-ttu-id="ef09e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ef09e-142">System.Boolean</span></span>

## <span data-ttu-id="ef09e-143">Note</span><span class="sxs-lookup"><span data-stu-id="ef09e-143">NOTES</span></span>

## <span data-ttu-id="ef09e-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef09e-144">RELATED LINKS</span></span>
