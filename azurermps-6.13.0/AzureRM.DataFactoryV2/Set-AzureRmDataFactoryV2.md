---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
ms.openlocfilehash: c50023cefbae9a9ba341eba22f40a421c37d12c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515415"
---
# <span data-ttu-id="b3898-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b3898-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="b3898-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3898-102">SYNOPSIS</span></span>
<span data-ttu-id="b3898-103">Crea una data factory.</span><span class="sxs-lookup"><span data-stu-id="b3898-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3898-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3898-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3898-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3898-105">DESCRIPTION</span></span>
<span data-ttu-id="b3898-106">Il cmdlet **set-AzureRmDataFactoryV2** crea una factory di dati con il nome e il percorso del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="b3898-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="b3898-107">Eseguire queste operazioni nell'ordine seguente:--creare una factory di dati.</span><span class="sxs-lookup"><span data-stu-id="b3898-107">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="b3898-108">--Creare servizi collegati.</span><span class="sxs-lookup"><span data-stu-id="b3898-108">-- Create linked services.</span></span>
<span data-ttu-id="b3898-109">--Creare DataSet.</span><span class="sxs-lookup"><span data-stu-id="b3898-109">-- Create datasets.</span></span>
<span data-ttu-id="b3898-110">--Crea una pipeline.</span><span class="sxs-lookup"><span data-stu-id="b3898-110">-- Create a pipeline.</span></span>

## <span data-ttu-id="b3898-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3898-111">EXAMPLES</span></span>

### <span data-ttu-id="b3898-112">Esempio 1: creare una data factory</span><span class="sxs-lookup"><span data-stu-id="b3898-112">Example 1: Create a data factory</span></span>
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

<span data-ttu-id="b3898-113">Questo comando crea una factory di dati denominata WikiADF nel gruppo di risorse denominato ADF nella posizione Westus.</span><span class="sxs-lookup"><span data-stu-id="b3898-113">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="b3898-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3898-114">PARAMETERS</span></span>

### <span data-ttu-id="b3898-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3898-115">-DefaultProfile</span></span>
<span data-ttu-id="b3898-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b3898-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3898-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b3898-117">-Force</span></span>
<span data-ttu-id="b3898-118">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="b3898-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b3898-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b3898-119">-Location</span></span>
<span data-ttu-id="b3898-120">La factory di dati viene creata nell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="b3898-120">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="b3898-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3898-121">-Name</span></span>
<span data-ttu-id="b3898-122">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="b3898-122">The data factory name.</span></span>

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

### <span data-ttu-id="b3898-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3898-123">-ResourceGroupName</span></span>
<span data-ttu-id="b3898-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b3898-124">The resource group name.</span></span>

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

### <span data-ttu-id="b3898-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="b3898-125">-Tag</span></span>
<span data-ttu-id="b3898-126">Tag della data factory.</span><span class="sxs-lookup"><span data-stu-id="b3898-126">The tags of the data factory.</span></span>

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

### <span data-ttu-id="b3898-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b3898-127">-Confirm</span></span>
<span data-ttu-id="b3898-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3898-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3898-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3898-129">-WhatIf</span></span>
<span data-ttu-id="b3898-130">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3898-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="b3898-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3898-131">CommonParameters</span></span>
<span data-ttu-id="b3898-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3898-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3898-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3898-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3898-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3898-134">INPUTS</span></span>

### <span data-ttu-id="b3898-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b3898-135">System.String</span></span>

### <span data-ttu-id="b3898-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b3898-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b3898-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3898-137">OUTPUTS</span></span>

### <span data-ttu-id="b3898-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b3898-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="b3898-139">Note</span><span class="sxs-lookup"><span data-stu-id="b3898-139">NOTES</span></span>
<span data-ttu-id="b3898-140">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="b3898-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b3898-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3898-141">RELATED LINKS</span></span>

[<span data-ttu-id="b3898-142">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b3898-142">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="b3898-143">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b3898-143">Remove-AzureRmDataFactoryV2</span></span>]()
