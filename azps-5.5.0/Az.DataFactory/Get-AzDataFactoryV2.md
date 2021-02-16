---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
ms.openlocfilehash: fac2e899984f9d626f6c7342043166649327a0f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204466"
---
# <span data-ttu-id="bf522-101">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="bf522-101">Get-AzDataFactoryV2</span></span>

## <span data-ttu-id="bf522-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf522-102">SYNOPSIS</span></span>
<span data-ttu-id="bf522-103">Ottiene informazioni su Data factory.</span><span class="sxs-lookup"><span data-stu-id="bf522-103">Gets information about Data Factory.</span></span>

## <span data-ttu-id="bf522-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bf522-104">SYNTAX</span></span>

### <span data-ttu-id="bf522-105">BySubscriptionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bf522-105">BySubscriptionId (Default)</span></span>
```
Get-AzDataFactoryV2 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf522-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="bf522-106">ByFactoryName</span></span>
```
Get-AzDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf522-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bf522-107">DESCRIPTION</span></span>
<span data-ttu-id="bf522-108">Il Get-AzDataFactoryV2 cmdlet recupera informazioni sulle data factories in un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="bf522-108">The Get-AzDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="bf522-109">Se si specifica il nome di un data factory, questo cmdlet ottiene informazioni su tale data factory.</span><span class="sxs-lookup"><span data-stu-id="bf522-109">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="bf522-110">Se non si specifica un nome, questo cmdlet ottiene informazioni su tutti i data factories in un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="bf522-110">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="bf522-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bf522-111">EXAMPLES</span></span>

### <span data-ttu-id="bf522-112">Esempio 1: Ottenere tutti i data factories</span><span class="sxs-lookup"><span data-stu-id="bf522-112">Example 1: Get all data factories</span></span>
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

<span data-ttu-id="bf522-113">Visualizza informazioni su tutti i data factories nella sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bf522-113">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="bf522-114">Esempio 2: Ottenere uno specifico data factory</span><span class="sxs-lookup"><span data-stu-id="bf522-114">Example 2: Get a specific data factory</span></span>
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

<span data-ttu-id="bf522-115">Questo comando visualizza informazioni sul data factory denominato WikiADF nella sottoscrizione del gruppo di risorse denominato ADF e quindi lo archivia nella $DataFactory variabile.</span><span class="sxs-lookup"><span data-stu-id="bf522-115">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="bf522-116">Specificare il parametro DataFactory nei cmdlet successivi per usare il data factory archiviato in $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="bf522-116">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="bf522-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf522-117">PARAMETERS</span></span>

### <span data-ttu-id="bf522-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf522-118">-DefaultProfile</span></span>
<span data-ttu-id="bf522-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bf522-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf522-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bf522-120">-Name</span></span>
<span data-ttu-id="bf522-121">Specifica il nome del data factory su cui ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="bf522-121">Specifies the name of the data factory about which to get information.</span></span>

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

### <span data-ttu-id="bf522-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf522-122">-ResourceGroupName</span></span>
<span data-ttu-id="bf522-123">Specifica il nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="bf522-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="bf522-124">Questo cmdlet ottiene informazioni sulle fattorie di dati appartenenti al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="bf522-124">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

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

### <span data-ttu-id="bf522-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf522-125">CommonParameters</span></span>
<span data-ttu-id="bf522-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf522-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf522-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bf522-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf522-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="bf522-128">INPUTS</span></span>

### <span data-ttu-id="bf522-129">System.String</span><span class="sxs-lookup"><span data-stu-id="bf522-129">System.String</span></span>

## <span data-ttu-id="bf522-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bf522-130">OUTPUTS</span></span>

### <span data-ttu-id="bf522-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="bf522-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="bf522-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="bf522-132">NOTES</span></span>
<span data-ttu-id="bf522-133">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="bf522-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="bf522-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bf522-134">RELATED LINKS</span></span>

[<span data-ttu-id="bf522-135">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="bf522-135">Set-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="bf522-136">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="bf522-136">Remove-AzDataFactoryV2</span></span>]()

