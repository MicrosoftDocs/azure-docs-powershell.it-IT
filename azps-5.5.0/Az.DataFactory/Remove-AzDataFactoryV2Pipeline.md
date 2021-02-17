---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: b1d39c3d60d043485cc4ec4dc0c4ba986a97e800
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186247"
---
# <span data-ttu-id="db7cc-101">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="db7cc-101">Remove-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="db7cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db7cc-102">SYNOPSIS</span></span>
<span data-ttu-id="db7cc-103">Rimuove una pipeline da Data factory.</span><span class="sxs-lookup"><span data-stu-id="db7cc-103">Removes a pipeline from Data Factory.</span></span>

## <span data-ttu-id="db7cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db7cc-104">SYNTAX</span></span>

### <span data-ttu-id="db7cc-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="db7cc-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db7cc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="db7cc-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db7cc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="db7cc-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db7cc-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="db7cc-108">DESCRIPTION</span></span>
<span data-ttu-id="db7cc-109">Il cmdlet Remove-AzDataFactoryV2Pipeline rimuove una pipeline da Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="db7cc-109">The Remove-AzDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="db7cc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db7cc-110">EXAMPLES</span></span>

### <span data-ttu-id="db7cc-111">Esempio 1: Rimuovere una pipeline</span><span class="sxs-lookup"><span data-stu-id="db7cc-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="db7cc-112">Questo cmdlet rimuove la pipeline denominata DPWikisample dal data factory denominato WikiADF.</span><span class="sxs-lookup"><span data-stu-id="db7cc-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="db7cc-113">Il comando restituisce il valore $True.</span><span class="sxs-lookup"><span data-stu-id="db7cc-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="db7cc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db7cc-114">PARAMETERS</span></span>

### <span data-ttu-id="db7cc-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="db7cc-115">-DataFactoryName</span></span>
<span data-ttu-id="db7cc-116">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="db7cc-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="db7cc-117">Questo cmdlet rimuove una pipeline dal data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="db7cc-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="db7cc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db7cc-118">-DefaultProfile</span></span>
<span data-ttu-id="db7cc-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db7cc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db7cc-120">-Force</span><span class="sxs-lookup"><span data-stu-id="db7cc-120">-Force</span></span>
<span data-ttu-id="db7cc-121">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="db7cc-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="db7cc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db7cc-122">-InputObject</span></span>
<span data-ttu-id="db7cc-123">Specifica un oggetto Pipeline.</span><span class="sxs-lookup"><span data-stu-id="db7cc-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="db7cc-124">Questo cmdlet rimuove la pipeline specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="db7cc-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="db7cc-125">-Name</span><span class="sxs-lookup"><span data-stu-id="db7cc-125">-Name</span></span>
<span data-ttu-id="db7cc-126">Specifica il nome della pipeline da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="db7cc-126">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="db7cc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db7cc-127">-ResourceGroupName</span></span>
<span data-ttu-id="db7cc-128">Specifica il nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="db7cc-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="db7cc-129">Questo cmdlet rimuove una pipeline dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="db7cc-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="db7cc-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db7cc-130">-ResourceId</span></span>
<span data-ttu-id="db7cc-131">ID della risorsa Azure della pipeline da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="db7cc-131">The Azure resource ID of the pipeline to remove.</span></span>

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

### <span data-ttu-id="db7cc-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db7cc-132">-Confirm</span></span>
<span data-ttu-id="db7cc-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db7cc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db7cc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db7cc-134">-WhatIf</span></span>
<span data-ttu-id="db7cc-135">Mostra cosa succede se il cmdlet viene eseguito, ma non lo esegue.</span><span class="sxs-lookup"><span data-stu-id="db7cc-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="db7cc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db7cc-136">CommonParameters</span></span>
<span data-ttu-id="db7cc-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db7cc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db7cc-138">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db7cc-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db7cc-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="db7cc-139">INPUTS</span></span>

### <span data-ttu-id="db7cc-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="db7cc-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="db7cc-141">System.String</span><span class="sxs-lookup"><span data-stu-id="db7cc-141">System.String</span></span>

## <span data-ttu-id="db7cc-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db7cc-142">OUTPUTS</span></span>

### <span data-ttu-id="db7cc-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="db7cc-143">System.Boolean</span></span>

## <span data-ttu-id="db7cc-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="db7cc-144">NOTES</span></span>
<span data-ttu-id="db7cc-145">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="db7cc-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="db7cc-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db7cc-146">RELATED LINKS</span></span>

[<span data-ttu-id="db7cc-147">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="db7cc-147">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="db7cc-148">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="db7cc-148">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="db7cc-149">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="db7cc-149">Invoke-AzDataFactoryV2Pipeline</span></span>]()

