---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 16873efe9ba51eb71821fe7149c5abb1f316c4eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685713"
---
# <span data-ttu-id="02b76-101">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="02b76-101">Get-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="02b76-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="02b76-102">SYNOPSIS</span></span>
<span data-ttu-id="02b76-103">Ottiene i dettagli di una capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="02b76-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02b76-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="02b76-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIEmbeddedCapacity [[-ResourceGroupName] <String>] 
    [<CommonParameters>]

Get-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> 
    [<CommonParameters>]
```

## <span data-ttu-id="02b76-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02b76-105">DESCRIPTION</span></span>
<span data-ttu-id="02b76-106">Il cmdlet Get-AzureRmPowerBIEmbeddedCapacity ottiene i dettagli di una capacità incorporata PowerBI.</span><span class="sxs-lookup"><span data-stu-id="02b76-106">The Get-AzureRmPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="02b76-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="02b76-107">EXAMPLES</span></span>

### <span data-ttu-id="02b76-108">Esempio 1: ottenere le capacità del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="02b76-108">Example 1: Get resource group capacities</span></span>
```
PS C:\>Get-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}

Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/mycapacity
ResourceGroup          : testRG
Name                   : mycapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A4
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="02b76-109">Questo comando consente di ottenere tutte le capacità embedded di Azure PowerBI nel gruppo di risorse denominato testRG</span><span class="sxs-lookup"><span data-stu-id="02b76-109">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="02b76-110">Esempio 2: ottenere una capacità</span><span class="sxs-lookup"><span data-stu-id="02b76-110">Example 2: Get a capacity</span></span>
```
PS C:\>Get-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}

```

<span data-ttu-id="02b76-111">Questo comando consente di ottenere la capacità incorporata di Azure PowerBI denominata testcapacity nel gruppo di risorse denominato testRG.</span><span class="sxs-lookup"><span data-stu-id="02b76-111">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="02b76-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="02b76-112">PARAMETERS</span></span>

### <span data-ttu-id="02b76-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02b76-113">-ResourceGroupName</span></span>
<span data-ttu-id="02b76-114">Nome del gruppo di risorse Azure a cui appartiene la capacità</span><span class="sxs-lookup"><span data-stu-id="02b76-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByCapacity
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="02b76-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="02b76-115">-Name</span></span>
<span data-ttu-id="02b76-116">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="02b76-116">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByCapacity
Aliases: 

Required: True
Position: 1
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="02b76-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02b76-117">-ResourceId</span></span>
<span data-ttu-id="02b76-118">ID risorsa di Azure</span><span class="sxs-lookup"><span data-stu-id="02b76-118">Azure resource ID</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02b76-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02b76-119">CommonParameters</span></span>
<span data-ttu-id="02b76-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02b76-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02b76-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02b76-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02b76-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="02b76-122">INPUTS</span></span>

### <span data-ttu-id="02b76-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="02b76-123">None</span></span>
<span data-ttu-id="02b76-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="02b76-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="02b76-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="02b76-125">OUTPUTS</span></span>

### <span data-ttu-id="02b76-126">Elenco<Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity></span><span class="sxs-lookup"><span data-stu-id="02b76-126">List<Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity></span></span>

## <span data-ttu-id="02b76-127">Note</span><span class="sxs-lookup"><span data-stu-id="02b76-127">NOTES</span></span>

## <span data-ttu-id="02b76-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="02b76-128">RELATED LINKS</span></span>

[<span data-ttu-id="02b76-129">New-AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="02b76-129">New-AzureRmPowerBIEmbeddedCapacity </span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="02b76-130">Remove-AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="02b76-130">Remove-AzureRmPowerBIEmbeddedCapacity </span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
