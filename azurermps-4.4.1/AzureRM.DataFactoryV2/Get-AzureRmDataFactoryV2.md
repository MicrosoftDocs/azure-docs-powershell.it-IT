---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 8742babd73e28e28797db75952d7eb9e9c8dc4a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518287"
---
# <span data-ttu-id="36c52-101">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="36c52-101">Get-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="36c52-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="36c52-102">SYNOPSIS</span></span>
<span data-ttu-id="36c52-103">Ottiene informazioni su Data Factory.</span><span class="sxs-lookup"><span data-stu-id="36c52-103">Gets information about Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36c52-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36c52-104">SYNTAX</span></span>

```
Get-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>]
```

## <span data-ttu-id="36c52-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36c52-105">DESCRIPTION</span></span>
<span data-ttu-id="36c52-106">Il cmdlet Get-AzureRmDataFactoryV2 ottiene informazioni sulle Factory di dati in un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="36c52-106">The Get-AzureRmDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="36c52-107">Se specifichi il nome di una data factory, questo cmdlet ottiene informazioni su tale data factory.</span><span class="sxs-lookup"><span data-stu-id="36c52-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="36c52-108">Se non specifichi un nome, questo cmdlet recupera informazioni su tutti i factory di dati in un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="36c52-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>


## <span data-ttu-id="36c52-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36c52-109">EXAMPLES</span></span>

### <span data-ttu-id="36c52-110">Esempio 1: ottenere tutte le factory di dati</span><span class="sxs-lookup"><span data-stu-id="36c52-110">Example 1: Get all data factories</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

    DataFactoryName   : WikiADF2
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf2
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          :
    ProvisioningState : Succeeded

```

<span data-ttu-id="36c52-111">Visualizza informazioni su tutti i factory di dati nell'abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="36c52-111">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="36c52-112">Esempio 2: ottenere una factory di dati specifica</span><span class="sxs-lookup"><span data-stu-id="36c52-112">Example 2: Get a specific data factory</span></span>
```
PS C:\> $DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataF
                        actory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

```

<span data-ttu-id="36c52-113">Questo comando Visualizza le informazioni sulla factory di dati denominate WikiADF nell'abbonamento per il gruppo di risorse denominato ADF e lo archivia nella variabile $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="36c52-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="36c52-114">Specifica il parametro DataFactory nei cmdlet successivi per usare la factory di dati archiviata in $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="36c52-114">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="36c52-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36c52-115">PARAMETERS</span></span>

### <span data-ttu-id="36c52-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="36c52-116">-Name</span></span>
<span data-ttu-id="36c52-117">Specifica il nome della factory di dati per cui ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="36c52-117">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36c52-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36c52-118">-ResourceGroupName</span></span>
<span data-ttu-id="36c52-119">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="36c52-119">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="36c52-120">Questo cmdlet ottiene informazioni sulle Factory di dati che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="36c52-120">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

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

## <span data-ttu-id="36c52-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="36c52-121">INPUTS</span></span>

### <span data-ttu-id="36c52-122">System. String</span><span class="sxs-lookup"><span data-stu-id="36c52-122">System.String</span></span>


## <span data-ttu-id="36c52-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36c52-123">OUTPUTS</span></span>

### <span data-ttu-id="36c52-124">System. Collections. Generic. list ' 1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="36c52-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="36c52-125">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="36c52-125">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="36c52-126">Note</span><span class="sxs-lookup"><span data-stu-id="36c52-126">NOTES</span></span>
<span data-ttu-id="36c52-127">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="36c52-127">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="36c52-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36c52-128">RELATED LINKS</span></span>
[<span data-ttu-id="36c52-129">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="36c52-129">Set-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="36c52-130">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="36c52-130">Remove-AzureRmDataFactoryV2</span></span>]()

