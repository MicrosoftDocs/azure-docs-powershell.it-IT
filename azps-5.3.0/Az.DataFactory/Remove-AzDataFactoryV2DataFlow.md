---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 8b5b9e8cfd1909b0d91627a2c0600620f264da78
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477099"
---
# <span data-ttu-id="0b6cf-101">Remove-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="0b6cf-101">Remove-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="0b6cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0b6cf-102">SYNOPSIS</span></span>
<span data-ttu-id="0b6cf-103">Rimuove un flusso di dati da data factory.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-103">Removes a data flow from Data Factory.</span></span>

## <span data-ttu-id="0b6cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b6cf-104">SYNTAX</span></span>

### <span data-ttu-id="0b6cf-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0b6cf-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b6cf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0b6cf-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2DataFlow [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b6cf-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0b6cf-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Force] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b6cf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b6cf-108">DESCRIPTION</span></span>
<span data-ttu-id="0b6cf-109">Il cmdlet Remove-AzDataFactoryV2DataFlow rimuove un flusso di dati da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-109">The Remove-AzDataFactoryV2DataFlow cmdlet removes a data flow from Azure Data Factory.</span></span>

## <span data-ttu-id="0b6cf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b6cf-110">EXAMPLES</span></span>

### <span data-ttu-id="0b6cf-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0b6cf-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Remove-AzDataFactoryV2DataFlow -ResourceGroupName adf -DataFactoryName WikiADF -DataFlowName "dataflow5"

Confirm
Are you sure you want to remove data flow 'dataflow5' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\WINDOWS\system32>
```

<span data-ttu-id="0b6cf-112">Questo comando rimuove il flusso di dati denominato dataflow5 dalla data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-112">This command removes the data flow named dataflow5 from the data factory named WikiADF.</span></span>

## <span data-ttu-id="0b6cf-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0b6cf-113">PARAMETERS</span></span>

### <span data-ttu-id="0b6cf-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="0b6cf-114">-DataFactoryName</span></span>
<span data-ttu-id="0b6cf-115">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-115">The data factory name.</span></span>

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

### <span data-ttu-id="0b6cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b6cf-116">-DefaultProfile</span></span>
<span data-ttu-id="0b6cf-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b6cf-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0b6cf-118">-Force</span></span>
<span data-ttu-id="0b6cf-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="0b6cf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b6cf-120">-InputObject</span></span>
<span data-ttu-id="0b6cf-121">Oggetto flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-121">The data flow object.</span></span>

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

### <span data-ttu-id="0b6cf-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b6cf-122">-Name</span></span>
<span data-ttu-id="0b6cf-123">Nome del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-123">The data flow name.</span></span>

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

### <span data-ttu-id="0b6cf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b6cf-124">-ResourceGroupName</span></span>
<span data-ttu-id="0b6cf-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-125">The resource group name.</span></span>

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

### <span data-ttu-id="0b6cf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b6cf-126">-ResourceId</span></span>
<span data-ttu-id="0b6cf-127">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0b6cf-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b6cf-128">-PassThru</span></span>
<span data-ttu-id="0b6cf-129">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-129">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="0b6cf-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="0b6cf-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0b6cf-131">-Confirm</span></span>
<span data-ttu-id="0b6cf-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b6cf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b6cf-133">-WhatIf</span></span>
<span data-ttu-id="0b6cf-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b6cf-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b6cf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b6cf-136">CommonParameters</span></span>
<span data-ttu-id="0b6cf-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b6cf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b6cf-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b6cf-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b6cf-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0b6cf-139">INPUTS</span></span>

### <span data-ttu-id="0b6cf-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="0b6cf-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="0b6cf-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0b6cf-141">System.String</span></span>

## <span data-ttu-id="0b6cf-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b6cf-142">OUTPUTS</span></span>

### <span data-ttu-id="0b6cf-143">System. void</span><span class="sxs-lookup"><span data-stu-id="0b6cf-143">System.Void</span></span>

### <span data-ttu-id="0b6cf-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0b6cf-144">System.Boolean</span></span>

## <span data-ttu-id="0b6cf-145">Note</span><span class="sxs-lookup"><span data-stu-id="0b6cf-145">NOTES</span></span>
<span data-ttu-id="0b6cf-146">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="0b6cf-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0b6cf-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b6cf-147">RELATED LINKS</span></span>

[<span data-ttu-id="0b6cf-148">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="0b6cf-148">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="0b6cf-149">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="0b6cf-149">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

