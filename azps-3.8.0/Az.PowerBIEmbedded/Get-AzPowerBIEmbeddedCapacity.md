---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: ce52463e9e983f3ad2483262775f5d4114370aa8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018624"
---
# <span data-ttu-id="ce085-101">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="ce085-101">Get-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="ce085-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ce085-102">SYNOPSIS</span></span>
<span data-ttu-id="ce085-103">Ottiene i dettagli di una capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="ce085-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="ce085-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce085-104">SYNTAX</span></span>

### <span data-ttu-id="ce085-105">ByCapacityOrResourceGroupOrSubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ce085-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce085-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ce085-106">ByResourceId</span></span>
```
Get-AzPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ce085-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce085-107">DESCRIPTION</span></span>
<span data-ttu-id="ce085-108">Il cmdlet Get-AzPowerBIEmbeddedCapacity ottiene i dettagli di una capacità incorporata PowerBI.</span><span class="sxs-lookup"><span data-stu-id="ce085-108">The Get-AzPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="ce085-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce085-109">EXAMPLES</span></span>

### <span data-ttu-id="ce085-110">Esempio 1: ottenere le capacità del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ce085-110">Example 1: Get resource group capacities</span></span>
```
PS C:\>Get-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG"
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

<span data-ttu-id="ce085-111">Questo comando consente di ottenere tutte le capacità embedded di Azure PowerBI nel gruppo di risorse denominato testRG</span><span class="sxs-lookup"><span data-stu-id="ce085-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="ce085-112">Esempio 2: ottenere una capacità</span><span class="sxs-lookup"><span data-stu-id="ce085-112">Example 2: Get a capacity</span></span>
```
PS C:\>Get-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity"
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

<span data-ttu-id="ce085-113">Questo comando consente di ottenere la capacità incorporata di Azure PowerBI denominata testcapacity nel gruppo di risorse denominato testRG.</span><span class="sxs-lookup"><span data-stu-id="ce085-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="ce085-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce085-114">PARAMETERS</span></span>

### <span data-ttu-id="ce085-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce085-115">-DefaultProfile</span></span>
<span data-ttu-id="ce085-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce085-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce085-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce085-117">-Name</span></span>
<span data-ttu-id="ce085-118">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="ce085-118">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="ce085-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce085-119">-ResourceGroupName</span></span>
<span data-ttu-id="ce085-120">Nome del gruppo di risorse Azure a cui appartiene la capacità</span><span class="sxs-lookup"><span data-stu-id="ce085-120">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="ce085-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce085-121">-ResourceId</span></span>
<span data-ttu-id="ce085-122">ID risorsa di Azure</span><span class="sxs-lookup"><span data-stu-id="ce085-122">Azure resource ID</span></span>

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

### <span data-ttu-id="ce085-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce085-123">CommonParameters</span></span>
<span data-ttu-id="ce085-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce085-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce085-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce085-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce085-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ce085-126">INPUTS</span></span>

### <span data-ttu-id="ce085-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ce085-127">System.String</span></span>

## <span data-ttu-id="ce085-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce085-128">OUTPUTS</span></span>

### <span data-ttu-id="ce085-129">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="ce085-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="ce085-130">Note</span><span class="sxs-lookup"><span data-stu-id="ce085-130">NOTES</span></span>

## <span data-ttu-id="ce085-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce085-131">RELATED LINKS</span></span>

[<span data-ttu-id="ce085-132">New-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="ce085-132">New-AzPowerBIEmbeddedCapacity </span></span>](./New-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="ce085-133">Remove-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="ce085-133">Remove-AzPowerBIEmbeddedCapacity </span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
