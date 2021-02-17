---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: b441c354214775f3f6aad425513a953fbefe7810
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404514"
---
# <span data-ttu-id="0664a-101">Remove-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="0664a-101">Remove-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="0664a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0664a-102">SYNOPSIS</span></span>
<span data-ttu-id="0664a-103">Rimuove un flusso di dati da Data factory.</span><span class="sxs-lookup"><span data-stu-id="0664a-103">Removes a data flow from Data Factory.</span></span>

## <span data-ttu-id="0664a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0664a-104">SYNTAX</span></span>

### <span data-ttu-id="0664a-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="0664a-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0664a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0664a-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2DataFlow [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0664a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0664a-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Force] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0664a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0664a-108">DESCRIPTION</span></span>
<span data-ttu-id="0664a-109">Il cmdlet Remove-AzDataFactoryV2DataFlow rimuove un flusso di dati da Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="0664a-109">The Remove-AzDataFactoryV2DataFlow cmdlet removes a data flow from Azure Data Factory.</span></span>

## <span data-ttu-id="0664a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0664a-110">EXAMPLES</span></span>

### <span data-ttu-id="0664a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0664a-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Remove-AzDataFactoryV2DataFlow -ResourceGroupName adf -DataFactoryName WikiADF -DataFlowName "dataflow5"

Confirm
Are you sure you want to remove data flow 'dataflow5' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\WINDOWS\system32>
```

<span data-ttu-id="0664a-112">Questo comando rimuove il flusso di dati denominato dataflow5 dal data factory denominato WikiADF.</span><span class="sxs-lookup"><span data-stu-id="0664a-112">This command removes the data flow named dataflow5 from the data factory named WikiADF.</span></span>

## <span data-ttu-id="0664a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0664a-113">PARAMETERS</span></span>

### <span data-ttu-id="0664a-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0664a-114">-DataFactoryName</span></span>
<span data-ttu-id="0664a-115">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="0664a-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0664a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0664a-116">-DefaultProfile</span></span>
<span data-ttu-id="0664a-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0664a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0664a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0664a-118">-Force</span></span>
<span data-ttu-id="0664a-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="0664a-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="0664a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0664a-120">-InputObject</span></span>
<span data-ttu-id="0664a-121">Oggetto del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="0664a-121">The data flow object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0664a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0664a-122">-Name</span></span>
<span data-ttu-id="0664a-123">Nome del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="0664a-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFlowName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0664a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0664a-124">-ResourceGroupName</span></span>
<span data-ttu-id="0664a-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0664a-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0664a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0664a-126">-ResourceId</span></span>
<span data-ttu-id="0664a-127">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="0664a-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0664a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0664a-128">-PassThru</span></span>
<span data-ttu-id="0664a-129">Se specificato, write true se l'operazione riesce.</span><span class="sxs-lookup"><span data-stu-id="0664a-129">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="0664a-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0664a-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="0664a-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0664a-131">-Confirm</span></span>
<span data-ttu-id="0664a-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0664a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0664a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0664a-133">-WhatIf</span></span>
<span data-ttu-id="0664a-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0664a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0664a-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0664a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0664a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0664a-136">CommonParameters</span></span>
<span data-ttu-id="0664a-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0664a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0664a-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0664a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0664a-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="0664a-139">INPUTS</span></span>

### <span data-ttu-id="0664a-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="0664a-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="0664a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0664a-141">System.String</span></span>

## <span data-ttu-id="0664a-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0664a-142">OUTPUTS</span></span>

### <span data-ttu-id="0664a-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="0664a-143">System.Void</span></span>

### <span data-ttu-id="0664a-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0664a-144">System.Boolean</span></span>

## <span data-ttu-id="0664a-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="0664a-145">NOTES</span></span>
<span data-ttu-id="0664a-146">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="0664a-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0664a-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0664a-147">RELATED LINKS</span></span>



