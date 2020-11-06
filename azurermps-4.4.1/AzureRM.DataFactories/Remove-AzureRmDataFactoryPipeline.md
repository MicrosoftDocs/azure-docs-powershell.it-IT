---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 48638f53f58fd420e9a7b3dfe2e50a3e61d2314f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510699"
---
# <span data-ttu-id="dd8d5-101">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="dd8d5-101">Remove-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="dd8d5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dd8d5-102">SYNOPSIS</span></span>
<span data-ttu-id="dd8d5-103">Rimuove una pipeline da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-103">Removes a pipeline from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd8d5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd8d5-104">SYNTAX</span></span>

### <span data-ttu-id="dd8d5-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dd8d5-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd8d5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="dd8d5-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd8d5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd8d5-107">DESCRIPTION</span></span>
<span data-ttu-id="dd8d5-108">Il cmdlet **Remove-AzureRmDataFactoryPipeline** rimuove una pipeline da Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-108">The **Remove-AzureRmDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="dd8d5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd8d5-109">EXAMPLES</span></span>

### <span data-ttu-id="dd8d5-110">Esempio 1: rimuovere una pipeline</span><span class="sxs-lookup"><span data-stu-id="dd8d5-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="dd8d5-111">Questo cmdlet consente di rimuovere la pipeline denominata DPWikisample dalla data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="dd8d5-112">Il comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="dd8d5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd8d5-113">PARAMETERS</span></span>

### <span data-ttu-id="dd8d5-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="dd8d5-114">-DataFactory</span></span>
<span data-ttu-id="dd8d5-115">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="dd8d5-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="dd8d5-116">Questo cmdlet consente di rimuovere una pipeline dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="dd8d5-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="dd8d5-117">-DataFactoryName</span></span>
<span data-ttu-id="dd8d5-118">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="dd8d5-119">Questo cmdlet consente di rimuovere una pipeline dalla data factory specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="dd8d5-120">-Force</span><span class="sxs-lookup"><span data-stu-id="dd8d5-120">-Force</span></span>
<span data-ttu-id="dd8d5-121">Indica che questo cmdlet rimuove una pipeline senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-121">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="dd8d5-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd8d5-122">-Name</span></span>
<span data-ttu-id="dd8d5-123">Specifica il nome della pipeline da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-123">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="dd8d5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd8d5-124">-ResourceGroupName</span></span>
<span data-ttu-id="dd8d5-125">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="dd8d5-126">Questo cmdlet consente di rimuovere una pipeline dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-126">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="dd8d5-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dd8d5-127">-Confirm</span></span>
<span data-ttu-id="dd8d5-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd8d5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd8d5-129">-WhatIf</span></span>
<span data-ttu-id="dd8d5-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd8d5-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd8d5-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd8d5-132">-DefaultProfile</span></span>
<span data-ttu-id="dd8d5-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd8d5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd8d5-134">CommonParameters</span></span>
<span data-ttu-id="dd8d5-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd8d5-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd8d5-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd8d5-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dd8d5-137">INPUTS</span></span>

## <span data-ttu-id="dd8d5-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd8d5-138">OUTPUTS</span></span>

### <span data-ttu-id="dd8d5-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd8d5-139">System.Boolean</span></span>

## <span data-ttu-id="dd8d5-140">Note</span><span class="sxs-lookup"><span data-stu-id="dd8d5-140">NOTES</span></span>
* <span data-ttu-id="dd8d5-141">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="dd8d5-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="dd8d5-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd8d5-142">RELATED LINKS</span></span>

[<span data-ttu-id="dd8d5-143">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="dd8d5-143">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="dd8d5-144">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="dd8d5-144">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="dd8d5-145">Curriculum vitae-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="dd8d5-145">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="dd8d5-146">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="dd8d5-146">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="dd8d5-147">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="dd8d5-147">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


