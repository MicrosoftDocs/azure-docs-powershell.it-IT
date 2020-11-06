---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: ed3284445121bf2ab6ecdd9aef2d8abe6d1351f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507516"
---
# <span data-ttu-id="e8978-101">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e8978-101">Remove-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="e8978-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e8978-102">SYNOPSIS</span></span>
<span data-ttu-id="e8978-103">Rimuove una pipeline dalla data factory.</span><span class="sxs-lookup"><span data-stu-id="e8978-103">Removes a pipeline from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8978-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8978-104">SYNTAX</span></span>

### <span data-ttu-id="e8978-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e8978-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8978-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e8978-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8978-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e8978-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8978-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8978-108">DESCRIPTION</span></span>
<span data-ttu-id="e8978-109">Il cmdlet Remove-AzureRmDataFactoryV2Pipeline consente di rimuovere una pipeline da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e8978-109">The Remove-AzureRmDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="e8978-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8978-110">EXAMPLES</span></span>

### <span data-ttu-id="e8978-111">Esempio 1: rimuovere una pipeline</span><span class="sxs-lookup"><span data-stu-id="e8978-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="e8978-112">Questo cmdlet consente di rimuovere la pipeline denominata DPWikisample dalla data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e8978-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="e8978-113">Il comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="e8978-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="e8978-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e8978-114">PARAMETERS</span></span>

### <span data-ttu-id="e8978-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e8978-115">-DataFactoryName</span></span>
<span data-ttu-id="e8978-116">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="e8978-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e8978-117">Questo cmdlet consente di rimuovere una pipeline dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e8978-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e8978-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8978-118">-DefaultProfile</span></span>
<span data-ttu-id="e8978-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e8978-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8978-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e8978-120">-Force</span></span>
<span data-ttu-id="e8978-121">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="e8978-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e8978-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8978-122">-InputObject</span></span>
<span data-ttu-id="e8978-123">Specifica un oggetto pipeline.</span><span class="sxs-lookup"><span data-stu-id="e8978-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="e8978-124">Questo cmdlet consente di rimuovere la pipeline specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e8978-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8978-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8978-125">-Name</span></span>
<span data-ttu-id="e8978-126">Specifica il nome della pipeline da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e8978-126">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8978-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8978-127">-ResourceGroupName</span></span>
<span data-ttu-id="e8978-128">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="e8978-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e8978-129">Questo cmdlet consente di rimuovere una pipeline dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e8978-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e8978-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8978-130">-ResourceId</span></span>
<span data-ttu-id="e8978-131">ID risorsa Azure della pipeline da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e8978-131">The Azure resource ID of the pipeline to remove.</span></span>

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

### <span data-ttu-id="e8978-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e8978-132">-Confirm</span></span>
<span data-ttu-id="e8978-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8978-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8978-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8978-134">-WhatIf</span></span>
<span data-ttu-id="e8978-135">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8978-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e8978-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8978-136">CommonParameters</span></span>
<span data-ttu-id="e8978-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8978-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8978-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8978-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8978-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e8978-139">INPUTS</span></span>

### <span data-ttu-id="e8978-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="e8978-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="e8978-141">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e8978-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="e8978-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e8978-142">System.String</span></span>

## <span data-ttu-id="e8978-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8978-143">OUTPUTS</span></span>

### <span data-ttu-id="e8978-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e8978-144">System.Boolean</span></span>

## <span data-ttu-id="e8978-145">Note</span><span class="sxs-lookup"><span data-stu-id="e8978-145">NOTES</span></span>
<span data-ttu-id="e8978-146">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="e8978-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e8978-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8978-147">RELATED LINKS</span></span>

[<span data-ttu-id="e8978-148">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e8978-148">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="e8978-149">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e8978-149">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="e8978-150">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e8978-150">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

