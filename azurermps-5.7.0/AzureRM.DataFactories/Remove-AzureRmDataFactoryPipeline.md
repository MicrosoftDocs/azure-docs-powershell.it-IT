---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: dec686838bd7826b57e7b158f4ed741608eaf782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509928"
---
# <span data-ttu-id="37fd0-101">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="37fd0-101">Remove-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="37fd0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="37fd0-102">SYNOPSIS</span></span>
<span data-ttu-id="37fd0-103">Rimuove una pipeline da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="37fd0-103">Removes a pipeline from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37fd0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37fd0-104">SYNTAX</span></span>

### <span data-ttu-id="37fd0-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="37fd0-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37fd0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="37fd0-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37fd0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37fd0-107">DESCRIPTION</span></span>
<span data-ttu-id="37fd0-108">Il cmdlet **Remove-AzureRmDataFactoryPipeline** rimuove una pipeline da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="37fd0-108">The **Remove-AzureRmDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="37fd0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37fd0-109">EXAMPLES</span></span>

### <span data-ttu-id="37fd0-110">Esempio 1: rimuovere una pipeline</span><span class="sxs-lookup"><span data-stu-id="37fd0-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="37fd0-111">Questo cmdlet consente di rimuovere la pipeline denominata DPWikisample dalla data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="37fd0-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="37fd0-112">Il comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="37fd0-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="37fd0-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37fd0-113">PARAMETERS</span></span>

### <span data-ttu-id="37fd0-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="37fd0-114">-DataFactory</span></span>
<span data-ttu-id="37fd0-115">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="37fd0-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="37fd0-116">Questo cmdlet consente di rimuovere una pipeline dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="37fd0-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37fd0-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="37fd0-117">-DataFactoryName</span></span>
<span data-ttu-id="37fd0-118">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="37fd0-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="37fd0-119">Questo cmdlet consente di rimuovere una pipeline dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="37fd0-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37fd0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37fd0-120">-DefaultProfile</span></span>
<span data-ttu-id="37fd0-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="37fd0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37fd0-122">-Force</span><span class="sxs-lookup"><span data-stu-id="37fd0-122">-Force</span></span>
<span data-ttu-id="37fd0-123">Indica che questo cmdlet rimuove una pipeline senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="37fd0-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37fd0-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="37fd0-124">-Name</span></span>
<span data-ttu-id="37fd0-125">Specifica il nome della pipeline da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="37fd0-125">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37fd0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37fd0-126">-ResourceGroupName</span></span>
<span data-ttu-id="37fd0-127">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="37fd0-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="37fd0-128">Questo cmdlet consente di rimuovere una pipeline dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="37fd0-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37fd0-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="37fd0-129">-Confirm</span></span>
<span data-ttu-id="37fd0-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37fd0-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37fd0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37fd0-131">-WhatIf</span></span>
<span data-ttu-id="37fd0-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37fd0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37fd0-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37fd0-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37fd0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37fd0-134">CommonParameters</span></span>
<span data-ttu-id="37fd0-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37fd0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37fd0-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37fd0-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37fd0-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="37fd0-137">INPUTS</span></span>

### <span data-ttu-id="37fd0-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="37fd0-138">None</span></span>
<span data-ttu-id="37fd0-139">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="37fd0-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="37fd0-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37fd0-140">OUTPUTS</span></span>

### <span data-ttu-id="37fd0-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="37fd0-141">System.Boolean</span></span>

## <span data-ttu-id="37fd0-142">Note</span><span class="sxs-lookup"><span data-stu-id="37fd0-142">NOTES</span></span>
* <span data-ttu-id="37fd0-143">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="37fd0-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="37fd0-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37fd0-144">RELATED LINKS</span></span>

[<span data-ttu-id="37fd0-145">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="37fd0-145">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="37fd0-146">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="37fd0-146">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="37fd0-147">Curriculum vitae-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="37fd0-147">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="37fd0-148">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="37fd0-148">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="37fd0-149">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="37fd0-149">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


