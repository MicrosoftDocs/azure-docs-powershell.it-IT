---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
ms.openlocfilehash: d52ddd20253e2d6969a19b92f7bd973584a7f630
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865343"
---
# <span data-ttu-id="61268-101">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="61268-101">Get-AzDataFactoryV2</span></span>

## <span data-ttu-id="61268-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61268-102">SYNOPSIS</span></span>
<span data-ttu-id="61268-103">Ottiene informazioni su Data Factory.</span><span class="sxs-lookup"><span data-stu-id="61268-103">Gets information about Data Factory.</span></span>

## <span data-ttu-id="61268-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61268-104">SYNTAX</span></span>

### <span data-ttu-id="61268-105">BySubscriptionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="61268-105">BySubscriptionId (Default)</span></span>
```
Get-AzDataFactoryV2 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61268-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="61268-106">ByFactoryName</span></span>
```
Get-AzDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61268-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61268-107">DESCRIPTION</span></span>
<span data-ttu-id="61268-108">Il cmdlet Get-AzDataFactoryV2 ottiene informazioni sulle Factory di dati in un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="61268-108">The Get-AzDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="61268-109">Se specifichi il nome di una data factory, questo cmdlet ottiene informazioni su tale data factory.</span><span class="sxs-lookup"><span data-stu-id="61268-109">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="61268-110">Se non specifichi un nome, questo cmdlet recupera informazioni su tutti i factory di dati in un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="61268-110">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="61268-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61268-111">EXAMPLES</span></span>

### <span data-ttu-id="61268-112">Esempio 1: ottenere tutte le factory di dati</span><span class="sxs-lookup"><span data-stu-id="61268-112">Example 1: Get all data factories</span></span>
```
PS C:\> Get-AzDataFactoryV2 -ResourceGroupName "ADF"

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

<span data-ttu-id="61268-113">Visualizza informazioni su tutti i factory di dati nell'abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="61268-113">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="61268-114">Esempio 2: ottenere una factory di dati specifica</span><span class="sxs-lookup"><span data-stu-id="61268-114">Example 2: Get a specific data factory</span></span>
```
PS C:\> $DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataF
                        actory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
```

<span data-ttu-id="61268-115">Questo comando Visualizza le informazioni sulla factory di dati denominate WikiADF nell'abbonamento per il gruppo di risorse denominato ADF e lo archivia nella variabile $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="61268-115">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="61268-116">Specifica il parametro DataFactory nei cmdlet successivi per usare la factory di dati archiviata in $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="61268-116">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="61268-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61268-117">PARAMETERS</span></span>

### <span data-ttu-id="61268-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61268-118">-DefaultProfile</span></span>
<span data-ttu-id="61268-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61268-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61268-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="61268-120">-Name</span></span>
<span data-ttu-id="61268-121">Specifica il nome della factory di dati per cui ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="61268-121">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61268-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61268-122">-ResourceGroupName</span></span>
<span data-ttu-id="61268-123">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="61268-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="61268-124">Questo cmdlet ottiene informazioni sulle Factory di dati che appartengono al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="61268-124">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

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

### <span data-ttu-id="61268-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61268-125">CommonParameters</span></span>
<span data-ttu-id="61268-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61268-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61268-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61268-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61268-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61268-128">INPUTS</span></span>

### <span data-ttu-id="61268-129">System. String</span><span class="sxs-lookup"><span data-stu-id="61268-129">System.String</span></span>

## <span data-ttu-id="61268-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61268-130">OUTPUTS</span></span>

### <span data-ttu-id="61268-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="61268-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="61268-132">Note</span><span class="sxs-lookup"><span data-stu-id="61268-132">NOTES</span></span>
<span data-ttu-id="61268-133">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="61268-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="61268-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61268-134">RELATED LINKS</span></span>

[<span data-ttu-id="61268-135">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="61268-135">Set-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="61268-136">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="61268-136">Remove-AzDataFactoryV2</span></span>]()

