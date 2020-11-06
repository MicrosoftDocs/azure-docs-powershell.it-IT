---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
ms.openlocfilehash: b5e5d42ba114da87daa3fa3effb15d3ad8bab22c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508556"
---
# <span data-ttu-id="89205-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="89205-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="89205-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="89205-102">SYNOPSIS</span></span>
<span data-ttu-id="89205-103">Crea una data factory.</span><span class="sxs-lookup"><span data-stu-id="89205-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89205-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="89205-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89205-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89205-105">DESCRIPTION</span></span>
<span data-ttu-id="89205-106">Il cmdlet **set-AzureRmDataFactoryV2** crea una factory di dati con il nome e il percorso del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="89205-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="89205-107">Eseguire queste operazioni nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="89205-107">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="89205-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="89205-108">EXAMPLES</span></span>

### <span data-ttu-id="89205-109">Esempio 1: creare una data factory</span><span class="sxs-lookup"><span data-stu-id="89205-109">Example 1: Create a data factory</span></span>
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

<span data-ttu-id="89205-110">Questo comando crea una factory di dati denominata WikiADF nel gruppo di risorse denominato ADF nella posizione Westus.</span><span class="sxs-lookup"><span data-stu-id="89205-110">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="89205-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="89205-111">PARAMETERS</span></span>

### <span data-ttu-id="89205-112">-Confermare</span><span class="sxs-lookup"><span data-stu-id="89205-112">-Confirm</span></span>
<span data-ttu-id="89205-113">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89205-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89205-114">-Force</span><span class="sxs-lookup"><span data-stu-id="89205-114">-Force</span></span>
<span data-ttu-id="89205-115">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="89205-115">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="89205-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="89205-116">-Location</span></span>
<span data-ttu-id="89205-117">La factory di dati viene creata nell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="89205-117">The data factory is created in this region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89205-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="89205-118">-Name</span></span>
<span data-ttu-id="89205-119">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="89205-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89205-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89205-120">-ResourceGroupName</span></span>
<span data-ttu-id="89205-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="89205-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89205-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="89205-122">-Tag</span></span>
<span data-ttu-id="89205-123">Tag della data factory.</span><span class="sxs-lookup"><span data-stu-id="89205-123">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89205-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89205-124">-WhatIf</span></span>
<span data-ttu-id="89205-125">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89205-125">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="89205-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89205-126">-DefaultProfile</span></span>
<span data-ttu-id="89205-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="89205-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89205-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89205-128">CommonParameters</span></span>
<span data-ttu-id="89205-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89205-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89205-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89205-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89205-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="89205-131">INPUTS</span></span>

### <span data-ttu-id="89205-132">System. String</span><span class="sxs-lookup"><span data-stu-id="89205-132">System.String</span></span>
<span data-ttu-id="89205-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="89205-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="89205-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="89205-134">OUTPUTS</span></span>

### <span data-ttu-id="89205-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="89205-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="89205-136">Note</span><span class="sxs-lookup"><span data-stu-id="89205-136">NOTES</span></span>
<span data-ttu-id="89205-137">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="89205-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="89205-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="89205-138">RELATED LINKS</span></span>

[<span data-ttu-id="89205-139">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="89205-139">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="89205-140">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="89205-140">Remove-AzureRmDataFactoryV2</span></span>]()
