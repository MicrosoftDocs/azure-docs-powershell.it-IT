---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 75c155b765a1bcbc565a85fc0f47130a6d2a5cf0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674958"
---
# <span data-ttu-id="26874-101">Remove-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="26874-101">Remove-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="26874-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26874-102">SYNOPSIS</span></span>
<span data-ttu-id="26874-103">Rimuove un flusso di dati da data factory.</span><span class="sxs-lookup"><span data-stu-id="26874-103">Removes a data flow from Data Factory.</span></span>

## <span data-ttu-id="26874-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26874-104">SYNTAX</span></span>

### <span data-ttu-id="26874-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="26874-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26874-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="26874-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2DataFlow [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26874-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="26874-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Force] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26874-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26874-108">DESCRIPTION</span></span>
<span data-ttu-id="26874-109">Il cmdlet Remove-AzDataFactoryV2DataFlow rimuove un flusso di dati da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="26874-109">The Remove-AzDataFactoryV2DataFlow cmdlet removes a data flow from Azure Data Factory.</span></span>

## <span data-ttu-id="26874-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26874-110">EXAMPLES</span></span>

### <span data-ttu-id="26874-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="26874-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Remove-AzDataFactoryV2DataFlow -ResourceGroupName adf -DataFactoryName WikiADF -DataFlowName "dataflow5"

Confirm
Are you sure you want to remove data flow 'dataflow5' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\WINDOWS\system32>
```

<span data-ttu-id="26874-112">Questo comando rimuove il flusso di dati denominato dataflow5 dalla data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="26874-112">This command removes the data flow named dataflow5 from the data factory named WikiADF.</span></span>

## <span data-ttu-id="26874-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26874-113">PARAMETERS</span></span>

### <span data-ttu-id="26874-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="26874-114">-DataFactoryName</span></span>
<span data-ttu-id="26874-115">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="26874-115">The data factory name.</span></span>

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

### <span data-ttu-id="26874-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26874-116">-DefaultProfile</span></span>
<span data-ttu-id="26874-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26874-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26874-118">-Force</span><span class="sxs-lookup"><span data-stu-id="26874-118">-Force</span></span>
<span data-ttu-id="26874-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="26874-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="26874-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26874-120">-InputObject</span></span>
<span data-ttu-id="26874-121">Oggetto flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="26874-121">The data flow object.</span></span>

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

### <span data-ttu-id="26874-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="26874-122">-Name</span></span>
<span data-ttu-id="26874-123">Nome del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="26874-123">The data flow name.</span></span>

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

### <span data-ttu-id="26874-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26874-124">-ResourceGroupName</span></span>
<span data-ttu-id="26874-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="26874-125">The resource group name.</span></span>

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

### <span data-ttu-id="26874-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26874-126">-ResourceId</span></span>
<span data-ttu-id="26874-127">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="26874-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="26874-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26874-128">-PassThru</span></span>
<span data-ttu-id="26874-129">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="26874-129">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="26874-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="26874-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="26874-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="26874-131">-Confirm</span></span>
<span data-ttu-id="26874-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26874-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26874-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26874-133">-WhatIf</span></span>
<span data-ttu-id="26874-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26874-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26874-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26874-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26874-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26874-136">CommonParameters</span></span>
<span data-ttu-id="26874-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26874-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26874-138">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26874-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26874-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26874-139">INPUTS</span></span>

### <span data-ttu-id="26874-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="26874-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="26874-141">System. String</span><span class="sxs-lookup"><span data-stu-id="26874-141">System.String</span></span>

## <span data-ttu-id="26874-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26874-142">OUTPUTS</span></span>

### <span data-ttu-id="26874-143">System. void</span><span class="sxs-lookup"><span data-stu-id="26874-143">System.Void</span></span>

### <span data-ttu-id="26874-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26874-144">System.Boolean</span></span>

## <span data-ttu-id="26874-145">Note</span><span class="sxs-lookup"><span data-stu-id="26874-145">NOTES</span></span>
<span data-ttu-id="26874-146">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="26874-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="26874-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26874-147">RELATED LINKS</span></span>

[<span data-ttu-id="26874-148">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="26874-148">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="26874-149">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="26874-149">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)
