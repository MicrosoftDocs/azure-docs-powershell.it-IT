---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: ce52463e9e983f3ad2483262775f5d4114370aa8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191406"
---
# <span data-ttu-id="ba666-101">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="ba666-101">Get-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="ba666-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba666-102">SYNOPSIS</span></span>
<span data-ttu-id="ba666-103">Recupera i dettagli di una capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="ba666-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="ba666-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba666-104">SYNTAX</span></span>

### <span data-ttu-id="ba666-105">ByCapacityOrResourceGroupOrSubscription (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ba666-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba666-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ba666-106">ByResourceId</span></span>
```
Get-AzPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba666-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ba666-107">DESCRIPTION</span></span>
<span data-ttu-id="ba666-108">Il Get-AzPowerBIEmbeddedCapacity cmdlet di powerbi ottiene i dettagli di una capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="ba666-108">The Get-AzPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="ba666-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba666-109">EXAMPLES</span></span>

### <span data-ttu-id="ba666-110">Esempio 1: Ottenere i due gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="ba666-110">Example 1: Get resource group capacities</span></span>
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

<span data-ttu-id="ba666-111">Questo comando recupera tutta la capacità incorporata di Azure PowerBI nel gruppo di risorse denominato testRG</span><span class="sxs-lookup"><span data-stu-id="ba666-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="ba666-112">Esempio 2: Ottenere una capacità</span><span class="sxs-lookup"><span data-stu-id="ba666-112">Example 2: Get a capacity</span></span>
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

<span data-ttu-id="ba666-113">Questo comando recupera la capacità incorporata di Azure PowerBI denominata testcapacity nel gruppo di risorse denominato testRG.</span><span class="sxs-lookup"><span data-stu-id="ba666-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="ba666-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba666-114">PARAMETERS</span></span>

### <span data-ttu-id="ba666-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba666-115">-DefaultProfile</span></span>
<span data-ttu-id="ba666-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba666-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba666-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ba666-117">-Name</span></span>
<span data-ttu-id="ba666-118">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="ba666-118">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="ba666-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba666-119">-ResourceGroupName</span></span>
<span data-ttu-id="ba666-120">Nome del gruppo di risorse azure a cui appartiene la capacità</span><span class="sxs-lookup"><span data-stu-id="ba666-120">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="ba666-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba666-121">-ResourceId</span></span>
<span data-ttu-id="ba666-122">ID risorsa Azure</span><span class="sxs-lookup"><span data-stu-id="ba666-122">Azure resource ID</span></span>

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

### <span data-ttu-id="ba666-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba666-123">CommonParameters</span></span>
<span data-ttu-id="ba666-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba666-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba666-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba666-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba666-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="ba666-126">INPUTS</span></span>

### <span data-ttu-id="ba666-127">System.String</span><span class="sxs-lookup"><span data-stu-id="ba666-127">System.String</span></span>

## <span data-ttu-id="ba666-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba666-128">OUTPUTS</span></span>

### <span data-ttu-id="ba666-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="ba666-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="ba666-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="ba666-130">NOTES</span></span>

## <span data-ttu-id="ba666-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba666-131">RELATED LINKS</span></span>

[<span data-ttu-id="ba666-132">New-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="ba666-132">New-AzPowerBIEmbeddedCapacity </span></span>](./New-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="ba666-133">Remove-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="ba666-133">Remove-AzPowerBIEmbeddedCapacity </span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
