---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
ms.openlocfilehash: 2bae0bd597cbd97a81efeaecb07e052457b88438
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180998"
---
# <span data-ttu-id="e730f-101">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="e730f-101">Remove-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="e730f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e730f-102">SYNOPSIS</span></span>
<span data-ttu-id="e730f-103">Rimuove una pipeline da Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="e730f-103">Removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="e730f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e730f-104">SYNTAX</span></span>

### <span data-ttu-id="e730f-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="e730f-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e730f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e730f-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e730f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e730f-107">DESCRIPTION</span></span>
<span data-ttu-id="e730f-108">Il cmdlet **Remove-AzDataFactoryPipeline** rimuove una pipeline da Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="e730f-108">The **Remove-AzDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="e730f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e730f-109">EXAMPLES</span></span>

### <span data-ttu-id="e730f-110">Esempio 1: Rimuovere una pipeline</span><span class="sxs-lookup"><span data-stu-id="e730f-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="e730f-111">Questo cmdlet rimuove la pipeline denominata DPWikisample dal data factory denominato WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e730f-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="e730f-112">Il comando restituisce il valore $True.</span><span class="sxs-lookup"><span data-stu-id="e730f-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="e730f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e730f-113">PARAMETERS</span></span>

### <span data-ttu-id="e730f-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e730f-114">-DataFactory</span></span>
<span data-ttu-id="e730f-115">Specifica un **oggetto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="e730f-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="e730f-116">Questo cmdlet rimuove una pipeline dal data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e730f-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e730f-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e730f-117">-DataFactoryName</span></span>
<span data-ttu-id="e730f-118">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="e730f-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e730f-119">Questo cmdlet rimuove una pipeline dal data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e730f-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e730f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e730f-120">-DefaultProfile</span></span>
<span data-ttu-id="e730f-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="e730f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e730f-122">-Force</span><span class="sxs-lookup"><span data-stu-id="e730f-122">-Force</span></span>
<span data-ttu-id="e730f-123">Indica che questo cmdlet rimuove una pipeline senza chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="e730f-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="e730f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e730f-124">-Name</span></span>
<span data-ttu-id="e730f-125">Specifica il nome della pipeline da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e730f-125">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="e730f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e730f-126">-ResourceGroupName</span></span>
<span data-ttu-id="e730f-127">Specifica il nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="e730f-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e730f-128">Questo cmdlet rimuove una pipeline dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e730f-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e730f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e730f-129">-Confirm</span></span>
<span data-ttu-id="e730f-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e730f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e730f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e730f-131">-WhatIf</span></span>
<span data-ttu-id="e730f-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e730f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e730f-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e730f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e730f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e730f-134">CommonParameters</span></span>
<span data-ttu-id="e730f-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e730f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e730f-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e730f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e730f-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="e730f-137">INPUTS</span></span>

### <span data-ttu-id="e730f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e730f-138">System.String</span></span>

### <span data-ttu-id="e730f-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e730f-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="e730f-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e730f-140">OUTPUTS</span></span>

### <span data-ttu-id="e730f-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="e730f-141">System.Void</span></span>

## <span data-ttu-id="e730f-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="e730f-142">NOTES</span></span>
* <span data-ttu-id="e730f-143">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="e730f-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e730f-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e730f-144">RELATED LINKS</span></span>

[<span data-ttu-id="e730f-145">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="e730f-145">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="e730f-146">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="e730f-146">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="e730f-147">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="e730f-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="e730f-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="e730f-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="e730f-149">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="e730f-149">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


