---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
ms.openlocfilehash: 6d3353e9f2daead1135b3da4ebde530137d8ae1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684592"
---
# <span data-ttu-id="9b635-101">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="9b635-101">Remove-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="9b635-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9b635-102">SYNOPSIS</span></span>
<span data-ttu-id="9b635-103">Rimuove una pipeline da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="9b635-103">Removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="9b635-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b635-104">SYNTAX</span></span>

### <span data-ttu-id="9b635-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9b635-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b635-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9b635-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b635-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b635-107">DESCRIPTION</span></span>
<span data-ttu-id="9b635-108">Il cmdlet **Remove-AzDataFactoryPipeline** rimuove una pipeline da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="9b635-108">The **Remove-AzDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="9b635-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b635-109">EXAMPLES</span></span>

### <span data-ttu-id="9b635-110">Esempio 1: rimuovere una pipeline</span><span class="sxs-lookup"><span data-stu-id="9b635-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="9b635-111">Questo cmdlet consente di rimuovere la pipeline denominata DPWikisample dalla data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="9b635-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="9b635-112">Il comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="9b635-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="9b635-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9b635-113">PARAMETERS</span></span>

### <span data-ttu-id="9b635-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9b635-114">-DataFactory</span></span>
<span data-ttu-id="9b635-115">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="9b635-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="9b635-116">Questo cmdlet consente di rimuovere una pipeline dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="9b635-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b635-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="9b635-117">-DataFactoryName</span></span>
<span data-ttu-id="9b635-118">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="9b635-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9b635-119">Questo cmdlet consente di rimuovere una pipeline dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="9b635-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9b635-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b635-120">-DefaultProfile</span></span>
<span data-ttu-id="9b635-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9b635-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b635-122">-Force</span><span class="sxs-lookup"><span data-stu-id="9b635-122">-Force</span></span>
<span data-ttu-id="9b635-123">Indica che questo cmdlet rimuove una pipeline senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="9b635-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="9b635-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="9b635-124">-Name</span></span>
<span data-ttu-id="9b635-125">Specifica il nome della pipeline da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="9b635-125">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b635-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b635-126">-ResourceGroupName</span></span>
<span data-ttu-id="9b635-127">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="9b635-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9b635-128">Questo cmdlet consente di rimuovere una pipeline dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="9b635-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9b635-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9b635-129">-Confirm</span></span>
<span data-ttu-id="9b635-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b635-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b635-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b635-131">-WhatIf</span></span>
<span data-ttu-id="9b635-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b635-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b635-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b635-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b635-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b635-134">CommonParameters</span></span>
<span data-ttu-id="9b635-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b635-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b635-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b635-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b635-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9b635-137">INPUTS</span></span>

### <span data-ttu-id="9b635-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9b635-138">System.String</span></span>

### <span data-ttu-id="9b635-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9b635-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="9b635-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b635-140">OUTPUTS</span></span>

### <span data-ttu-id="9b635-141">System. void</span><span class="sxs-lookup"><span data-stu-id="9b635-141">System.Void</span></span>

## <span data-ttu-id="9b635-142">Note</span><span class="sxs-lookup"><span data-stu-id="9b635-142">NOTES</span></span>
* <span data-ttu-id="9b635-143">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="9b635-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9b635-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b635-144">RELATED LINKS</span></span>

[<span data-ttu-id="9b635-145">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="9b635-145">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="9b635-146">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="9b635-146">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="9b635-147">Curriculum vitae-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="9b635-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="9b635-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="9b635-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="9b635-149">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="9b635-149">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


