---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: aede985cfac5b8ab25c4056eb44e54ea7c6b1c2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518796"
---
# <span data-ttu-id="ac892-101">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ac892-101">Remove-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="ac892-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ac892-102">SYNOPSIS</span></span>
<span data-ttu-id="ac892-103">Rimuove una pipeline da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ac892-103">Removes a pipeline from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac892-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac892-104">SYNTAX</span></span>

### <span data-ttu-id="ac892-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ac892-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ac892-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ac892-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac892-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac892-107">DESCRIPTION</span></span>
<span data-ttu-id="ac892-108">Il cmdlet **Remove-AzureRmDataFactoryPipeline** rimuove una pipeline da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ac892-108">The **Remove-AzureRmDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="ac892-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac892-109">EXAMPLES</span></span>

### <span data-ttu-id="ac892-110">Esempio 1: rimuovere una pipeline</span><span class="sxs-lookup"><span data-stu-id="ac892-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="ac892-111">Questo cmdlet consente di rimuovere la pipeline denominata DPWikisample dalla data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ac892-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="ac892-112">Il comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="ac892-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="ac892-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ac892-113">PARAMETERS</span></span>

### <span data-ttu-id="ac892-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ac892-114">-DataFactory</span></span>
<span data-ttu-id="ac892-115">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="ac892-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ac892-116">Questo cmdlet consente di rimuovere una pipeline dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ac892-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ac892-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="ac892-117">-DataFactoryName</span></span>
<span data-ttu-id="ac892-118">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="ac892-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ac892-119">Questo cmdlet consente di rimuovere una pipeline dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ac892-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ac892-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac892-120">-DefaultProfile</span></span>
<span data-ttu-id="ac892-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ac892-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac892-122">-Force</span><span class="sxs-lookup"><span data-stu-id="ac892-122">-Force</span></span>
<span data-ttu-id="ac892-123">Indica che questo cmdlet rimuove una pipeline senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="ac892-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="ac892-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac892-124">-Name</span></span>
<span data-ttu-id="ac892-125">Specifica il nome della pipeline da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ac892-125">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="ac892-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac892-126">-ResourceGroupName</span></span>
<span data-ttu-id="ac892-127">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="ac892-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ac892-128">Questo cmdlet consente di rimuovere una pipeline dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ac892-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ac892-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ac892-129">-Confirm</span></span>
<span data-ttu-id="ac892-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac892-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac892-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac892-131">-WhatIf</span></span>
<span data-ttu-id="ac892-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac892-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac892-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac892-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac892-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac892-134">CommonParameters</span></span>
<span data-ttu-id="ac892-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac892-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac892-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac892-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac892-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ac892-137">INPUTS</span></span>

### <span data-ttu-id="ac892-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ac892-138">System.String</span></span>

### <span data-ttu-id="ac892-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ac892-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="ac892-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac892-140">OUTPUTS</span></span>

### <span data-ttu-id="ac892-141">System. void</span><span class="sxs-lookup"><span data-stu-id="ac892-141">System.Void</span></span>

## <span data-ttu-id="ac892-142">Note</span><span class="sxs-lookup"><span data-stu-id="ac892-142">NOTES</span></span>
* <span data-ttu-id="ac892-143">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="ac892-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ac892-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac892-144">RELATED LINKS</span></span>

[<span data-ttu-id="ac892-145">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ac892-145">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="ac892-146">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ac892-146">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="ac892-147">Curriculum vitae-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ac892-147">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="ac892-148">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="ac892-148">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="ac892-149">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ac892-149">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


