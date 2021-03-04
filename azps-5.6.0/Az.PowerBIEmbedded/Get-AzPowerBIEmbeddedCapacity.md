---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/get-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 17d7547daaffdfafc117a250d20c0af1f069b70f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953470"
---
# <span data-ttu-id="5bcdc-101">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="5bcdc-101">Get-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="5bcdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bcdc-102">SYNOPSIS</span></span>
<span data-ttu-id="5bcdc-103">Recupera i dettagli di una capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="5bcdc-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="5bcdc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5bcdc-104">SYNTAX</span></span>

### <span data-ttu-id="5bcdc-105">ByCapacityOrResourceGroupOrSubscription (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5bcdc-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bcdc-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5bcdc-106">ByResourceId</span></span>
```
Get-AzPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5bcdc-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5bcdc-107">DESCRIPTION</span></span>
<span data-ttu-id="5bcdc-108">Il Get-AzPowerBIEmbeddedCapacity cmdlet di powerbi ottiene i dettagli di una capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="5bcdc-108">The Get-AzPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="5bcdc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5bcdc-109">EXAMPLES</span></span>

### <span data-ttu-id="5bcdc-110">Esempio 1: Ottenere i capacità del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="5bcdc-110">Example 1: Get resource group capacities</span></span>
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

<span data-ttu-id="5bcdc-111">Questo comando recupera tutta la capacità incorporata di Azure PowerBI nel gruppo di risorse denominato testRG</span><span class="sxs-lookup"><span data-stu-id="5bcdc-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="5bcdc-112">Esempio 2: Ottenere una capacità</span><span class="sxs-lookup"><span data-stu-id="5bcdc-112">Example 2: Get a capacity</span></span>
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

<span data-ttu-id="5bcdc-113">Questo comando recupera la capacità incorporata di Azure PowerBI denominata testcapacity nel gruppo di risorse denominato testRG.</span><span class="sxs-lookup"><span data-stu-id="5bcdc-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="5bcdc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bcdc-114">PARAMETERS</span></span>

### <span data-ttu-id="5bcdc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bcdc-115">-DefaultProfile</span></span>
<span data-ttu-id="5bcdc-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5bcdc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bcdc-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5bcdc-117">-Name</span></span>
<span data-ttu-id="5bcdc-118">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="5bcdc-118">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="5bcdc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bcdc-119">-ResourceGroupName</span></span>
<span data-ttu-id="5bcdc-120">Nome del gruppo di risorse azure a cui appartiene la capacità</span><span class="sxs-lookup"><span data-stu-id="5bcdc-120">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="5bcdc-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5bcdc-121">-ResourceId</span></span>
<span data-ttu-id="5bcdc-122">ID risorsa Azure</span><span class="sxs-lookup"><span data-stu-id="5bcdc-122">Azure resource ID</span></span>

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

### <span data-ttu-id="5bcdc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bcdc-123">CommonParameters</span></span>
<span data-ttu-id="5bcdc-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bcdc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bcdc-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bcdc-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bcdc-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="5bcdc-126">INPUTS</span></span>

### <span data-ttu-id="5bcdc-127">System.String</span><span class="sxs-lookup"><span data-stu-id="5bcdc-127">System.String</span></span>

## <span data-ttu-id="5bcdc-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5bcdc-128">OUTPUTS</span></span>

### <span data-ttu-id="5bcdc-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="5bcdc-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="5bcdc-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="5bcdc-130">NOTES</span></span>

## <span data-ttu-id="5bcdc-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5bcdc-131">RELATED LINKS</span></span>

[<span data-ttu-id="5bcdc-132">New-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="5bcdc-132">New-AzPowerBIEmbeddedCapacity </span></span>](./New-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="5bcdc-133">Remove-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="5bcdc-133">Remove-AzPowerBIEmbeddedCapacity </span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
