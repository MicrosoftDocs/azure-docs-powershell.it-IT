---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 4e15a9490fcaa41c77bb4ba822429646c6e45952
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511588"
---
# <span data-ttu-id="8cd3b-101">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8cd3b-101">Get-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="8cd3b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8cd3b-102">SYNOPSIS</span></span>
<span data-ttu-id="8cd3b-103">Ottiene i dettagli di una capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="8cd3b-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cd3b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8cd3b-104">SYNTAX</span></span>

### <span data-ttu-id="8cd3b-105">ByCapacityOrResourceGroupOrSubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8cd3b-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cd3b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8cd3b-106">ByResourceId</span></span>
```
Get-AzureRmPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8cd3b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cd3b-107">DESCRIPTION</span></span>
<span data-ttu-id="8cd3b-108">Il cmdlet Get-AzureRmPowerBIEmbeddedCapacity ottiene i dettagli di una capacità incorporata PowerBI.</span><span class="sxs-lookup"><span data-stu-id="8cd3b-108">The Get-AzureRmPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="8cd3b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8cd3b-109">EXAMPLES</span></span>

### <span data-ttu-id="8cd3b-110">Esempio 1: ottenere le capacità del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="8cd3b-110">Example 1: Get resource group capacities</span></span>
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

<span data-ttu-id="8cd3b-111">Questo comando consente di ottenere tutte le capacità embedded di Azure PowerBI nel gruppo di risorse denominato testRG</span><span class="sxs-lookup"><span data-stu-id="8cd3b-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="8cd3b-112">Esempio 2: ottenere una capacità</span><span class="sxs-lookup"><span data-stu-id="8cd3b-112">Example 2: Get a capacity</span></span>
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

<span data-ttu-id="8cd3b-113">Questo comando consente di ottenere la capacità incorporata di Azure PowerBI denominata testcapacity nel gruppo di risorse denominato testRG.</span><span class="sxs-lookup"><span data-stu-id="8cd3b-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="8cd3b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8cd3b-114">PARAMETERS</span></span>

### <span data-ttu-id="8cd3b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cd3b-115">-DefaultProfile</span></span>
<span data-ttu-id="8cd3b-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8cd3b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cd3b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="8cd3b-117">-Name</span></span>
<span data-ttu-id="8cd3b-118">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="8cd3b-118">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByCapacityOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cd3b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cd3b-119">-ResourceGroupName</span></span>
<span data-ttu-id="8cd3b-120">Nome del gruppo di risorse Azure a cui appartiene la capacità</span><span class="sxs-lookup"><span data-stu-id="8cd3b-120">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByCapacityOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cd3b-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cd3b-121">-ResourceId</span></span>
<span data-ttu-id="8cd3b-122">ID risorsa di Azure</span><span class="sxs-lookup"><span data-stu-id="8cd3b-122">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cd3b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cd3b-123">CommonParameters</span></span>
<span data-ttu-id="8cd3b-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cd3b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cd3b-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cd3b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cd3b-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8cd3b-126">INPUTS</span></span>

### <span data-ttu-id="8cd3b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8cd3b-127">System.String</span></span>

## <span data-ttu-id="8cd3b-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8cd3b-128">OUTPUTS</span></span>

### <span data-ttu-id="8cd3b-129">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8cd3b-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="8cd3b-130">Note</span><span class="sxs-lookup"><span data-stu-id="8cd3b-130">NOTES</span></span>

## <span data-ttu-id="8cd3b-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8cd3b-131">RELATED LINKS</span></span>

[<span data-ttu-id="8cd3b-132">New-AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="8cd3b-132">New-AzureRmPowerBIEmbeddedCapacity </span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="8cd3b-133">Remove-AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="8cd3b-133">Remove-AzureRmPowerBIEmbeddedCapacity </span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
