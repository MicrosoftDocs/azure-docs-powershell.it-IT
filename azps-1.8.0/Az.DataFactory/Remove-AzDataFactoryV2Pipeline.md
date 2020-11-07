---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 636ba1466eb0c5c0e8fda0433c74ec2291d2db9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684586"
---
# <span data-ttu-id="7cd92-101">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="7cd92-101">Remove-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="7cd92-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7cd92-102">SYNOPSIS</span></span>
<span data-ttu-id="7cd92-103">Rimuove una pipeline dalla data factory.</span><span class="sxs-lookup"><span data-stu-id="7cd92-103">Removes a pipeline from Data Factory.</span></span>

## <span data-ttu-id="7cd92-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7cd92-104">SYNTAX</span></span>

### <span data-ttu-id="7cd92-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7cd92-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cd92-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7cd92-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cd92-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7cd92-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cd92-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7cd92-108">DESCRIPTION</span></span>
<span data-ttu-id="7cd92-109">Il cmdlet Remove-AzDataFactoryV2Pipeline consente di rimuovere una pipeline da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="7cd92-109">The Remove-AzDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="7cd92-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7cd92-110">EXAMPLES</span></span>

### <span data-ttu-id="7cd92-111">Esempio 1: rimuovere una pipeline</span><span class="sxs-lookup"><span data-stu-id="7cd92-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="7cd92-112">Questo cmdlet consente di rimuovere la pipeline denominata DPWikisample dalla data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="7cd92-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="7cd92-113">Il comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="7cd92-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="7cd92-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7cd92-114">PARAMETERS</span></span>

### <span data-ttu-id="7cd92-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="7cd92-115">-DataFactoryName</span></span>
<span data-ttu-id="7cd92-116">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="7cd92-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="7cd92-117">Questo cmdlet consente di rimuovere una pipeline dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="7cd92-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7cd92-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cd92-118">-DefaultProfile</span></span>
<span data-ttu-id="7cd92-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7cd92-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cd92-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7cd92-120">-Force</span></span>
<span data-ttu-id="7cd92-121">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="7cd92-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="7cd92-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cd92-122">-InputObject</span></span>
<span data-ttu-id="7cd92-123">Specifica un oggetto pipeline.</span><span class="sxs-lookup"><span data-stu-id="7cd92-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="7cd92-124">Questo cmdlet consente di rimuovere la pipeline specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="7cd92-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="7cd92-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="7cd92-125">-Name</span></span>
<span data-ttu-id="7cd92-126">Specifica il nome della pipeline da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7cd92-126">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="7cd92-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cd92-127">-ResourceGroupName</span></span>
<span data-ttu-id="7cd92-128">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="7cd92-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7cd92-129">Questo cmdlet consente di rimuovere una pipeline dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="7cd92-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7cd92-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cd92-130">-ResourceId</span></span>
<span data-ttu-id="7cd92-131">ID risorsa Azure della pipeline da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7cd92-131">The Azure resource ID of the pipeline to remove.</span></span>

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

### <span data-ttu-id="7cd92-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7cd92-132">-Confirm</span></span>
<span data-ttu-id="7cd92-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cd92-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cd92-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cd92-134">-WhatIf</span></span>
<span data-ttu-id="7cd92-135">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7cd92-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="7cd92-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cd92-136">CommonParameters</span></span>
<span data-ttu-id="7cd92-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cd92-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cd92-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cd92-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cd92-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7cd92-139">INPUTS</span></span>

### <span data-ttu-id="7cd92-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="7cd92-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="7cd92-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7cd92-141">System.String</span></span>

## <span data-ttu-id="7cd92-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7cd92-142">OUTPUTS</span></span>

### <span data-ttu-id="7cd92-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7cd92-143">System.Boolean</span></span>

## <span data-ttu-id="7cd92-144">Note</span><span class="sxs-lookup"><span data-stu-id="7cd92-144">NOTES</span></span>
<span data-ttu-id="7cd92-145">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="7cd92-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7cd92-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7cd92-146">RELATED LINKS</span></span>

[<span data-ttu-id="7cd92-147">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="7cd92-147">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="7cd92-148">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="7cd92-148">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="7cd92-149">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="7cd92-149">Invoke-AzDataFactoryV2Pipeline</span></span>]()

