---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: e936d237589aec46d0f677344dfcd4274e19816d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508576"
---
# <span data-ttu-id="73265-101">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="73265-101">Remove-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="73265-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="73265-102">SYNOPSIS</span></span>
<span data-ttu-id="73265-103">Rimuove una pipeline dalla data factory.</span><span class="sxs-lookup"><span data-stu-id="73265-103">Removes a pipeline from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73265-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="73265-104">SYNTAX</span></span>

### <span data-ttu-id="73265-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="73265-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73265-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="73265-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73265-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="73265-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73265-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73265-108">DESCRIPTION</span></span>
<span data-ttu-id="73265-109">Il cmdlet Remove-AzureRmDataFactoryV2Pipeline consente di rimuovere una pipeline da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="73265-109">The Remove-AzureRmDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="73265-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="73265-110">EXAMPLES</span></span>

### <span data-ttu-id="73265-111">Esempio 1: rimuovere una pipeline</span><span class="sxs-lookup"><span data-stu-id="73265-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="73265-112">Questo cmdlet consente di rimuovere la pipeline denominata DPWikisample dalla data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="73265-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="73265-113">Il comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="73265-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="73265-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="73265-114">PARAMETERS</span></span>

### <span data-ttu-id="73265-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="73265-115">-Confirm</span></span>
<span data-ttu-id="73265-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73265-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73265-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="73265-117">-DataFactoryName</span></span>
<span data-ttu-id="73265-118">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="73265-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="73265-119">Questo cmdlet consente di rimuovere una pipeline dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="73265-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="73265-120">-Force</span><span class="sxs-lookup"><span data-stu-id="73265-120">-Force</span></span>
<span data-ttu-id="73265-121">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="73265-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="73265-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="73265-122">-Name</span></span>
<span data-ttu-id="73265-123">Specifica il nome della pipeline da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="73265-123">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="73265-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73265-124">-InputObject</span></span>
<span data-ttu-id="73265-125">Specifica un oggetto pipeline.</span><span class="sxs-lookup"><span data-stu-id="73265-125">Specifies a Pipeline object.</span></span>
<span data-ttu-id="73265-126">Questo cmdlet consente di rimuovere la pipeline specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="73265-126">This cmdlet removes the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="73265-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73265-127">-ResourceGroupName</span></span>
<span data-ttu-id="73265-128">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="73265-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="73265-129">Questo cmdlet consente di rimuovere una pipeline dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="73265-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="73265-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73265-130">-ResourceId</span></span>
<span data-ttu-id="73265-131">ID risorsa Azure della pipeline da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="73265-131">The Azure resource ID of the pipeline to remove.</span></span>

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

### <span data-ttu-id="73265-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73265-132">-WhatIf</span></span>
<span data-ttu-id="73265-133">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="73265-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="73265-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73265-134">-DefaultProfile</span></span>
<span data-ttu-id="73265-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="73265-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73265-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73265-136">CommonParameters</span></span>
<span data-ttu-id="73265-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73265-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73265-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73265-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73265-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="73265-139">INPUTS</span></span>

### <span data-ttu-id="73265-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="73265-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="73265-141">System. String</span><span class="sxs-lookup"><span data-stu-id="73265-141">System.String</span></span>

## <span data-ttu-id="73265-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="73265-142">OUTPUTS</span></span>

### <span data-ttu-id="73265-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="73265-143">System.Object</span></span>

## <span data-ttu-id="73265-144">Note</span><span class="sxs-lookup"><span data-stu-id="73265-144">NOTES</span></span>
<span data-ttu-id="73265-145">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="73265-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="73265-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="73265-146">RELATED LINKS</span></span>

[<span data-ttu-id="73265-147">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="73265-147">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="73265-148">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="73265-148">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="73265-149">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="73265-149">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

