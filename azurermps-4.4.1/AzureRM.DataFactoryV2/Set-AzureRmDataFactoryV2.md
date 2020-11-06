---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 8dc191223d5ec17856605c7640d324cc2ee3794e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522152"
---
# <span data-ttu-id="4450f-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4450f-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="4450f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4450f-102">SYNOPSIS</span></span>
<span data-ttu-id="4450f-103">Crea una data factory.</span><span class="sxs-lookup"><span data-stu-id="4450f-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4450f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4450f-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
[[-Tag] <Hashtable>] [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="4450f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4450f-105">DESCRIPTION</span></span>
<span data-ttu-id="4450f-106">Il cmdlet **set-AzureRmDataFactoryV2** crea una factory di dati con il nome e il percorso del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="4450f-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="4450f-107">Eseguire queste operazioni nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="4450f-107">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="4450f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4450f-108">EXAMPLES</span></span>

### <span data-ttu-id="4450f-109">Esempio 1: creare una data factory</span><span class="sxs-lookup"><span data-stu-id="4450f-109">Example 1: Create a data factory</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

```

<span data-ttu-id="4450f-110">Questo comando crea una factory di dati denominata WikiADF nel gruppo di risorse denominato ADF nella posizione Westus.</span><span class="sxs-lookup"><span data-stu-id="4450f-110">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="4450f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4450f-111">PARAMETERS</span></span>

### <span data-ttu-id="4450f-112">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4450f-112">-Confirm</span></span>
<span data-ttu-id="4450f-113">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4450f-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4450f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="4450f-114">-Force</span></span>
<span data-ttu-id="4450f-115">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="4450f-115">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="4450f-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4450f-116">-Location</span></span>
<span data-ttu-id="4450f-117">La factory di dati viene creata nell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="4450f-117">The data factory is created in this region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4450f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="4450f-118">-Name</span></span>
<span data-ttu-id="4450f-119">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="4450f-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4450f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4450f-120">-ResourceGroupName</span></span>
<span data-ttu-id="4450f-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4450f-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4450f-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="4450f-122">-Tag</span></span>
<span data-ttu-id="4450f-123">Tag della data factory.</span><span class="sxs-lookup"><span data-stu-id="4450f-123">The tags of the data factory.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4450f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4450f-124">-WhatIf</span></span>
<span data-ttu-id="4450f-125">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4450f-125">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="4450f-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4450f-126">INPUTS</span></span>

### <span data-ttu-id="4450f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4450f-127">System.String</span></span>
<span data-ttu-id="4450f-128">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4450f-128">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4450f-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4450f-129">OUTPUTS</span></span>

### <span data-ttu-id="4450f-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4450f-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="4450f-131">Note</span><span class="sxs-lookup"><span data-stu-id="4450f-131">NOTES</span></span>
<span data-ttu-id="4450f-132">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="4450f-132">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4450f-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4450f-133">RELATED LINKS</span></span>
[<span data-ttu-id="4450f-134">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4450f-134">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="4450f-135">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4450f-135">Remove-AzureRmDataFactoryV2</span></span>]()
