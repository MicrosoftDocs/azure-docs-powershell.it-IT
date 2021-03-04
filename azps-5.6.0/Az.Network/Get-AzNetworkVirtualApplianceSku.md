---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkvirtualappliancesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
ms.openlocfilehash: e165b481b1321f5ddd81766452120f55f6f0e153
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954526"
---
# <span data-ttu-id="e1bad-101">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="e1bad-101">Get-AzNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="e1bad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1bad-102">SYNOPSIS</span></span>
<span data-ttu-id="e1bad-103">Ottieni o elenca le SKU di Network Virtual Appliance disponibili nell'inventario.</span><span class="sxs-lookup"><span data-stu-id="e1bad-103">Get or List available Network Virtual Appliance Skus in the inventory.</span></span>

## <span data-ttu-id="e1bad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1bad-104">SYNTAX</span></span>

```
Get-AzNetworkVirtualApplianceSku [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1bad-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e1bad-105">DESCRIPTION</span></span>
<span data-ttu-id="e1bad-106">Il Get-AzNetworkVirtualApplianceSku ottiene o elenca le SKU di Network Virtual Appliance disponibili nell'inventario di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e1bad-106">The Get-AzNetworkVirtualApplianceSku gets or lists available Network Virtual Appliance Skus in the Microsoft Azure inventory.</span></span>

## <span data-ttu-id="e1bad-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1bad-107">EXAMPLES</span></span>

### <span data-ttu-id="e1bad-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e1bad-108">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku -SkuName barracudasdwanrelease                                                                                                                        

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="e1bad-109">Ottenere una SKU in base al nome.</span><span class="sxs-lookup"><span data-stu-id="e1bad-109">Get a sku by name.</span></span>

### <span data-ttu-id="e1bad-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e1bad-110">Example 2</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku                                                                                                                                                       

Vendor              : barracuda sdwan nightly
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan nightly
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracuda sdwan
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="e1bad-111">Elencare tutte le SKU disponibili di Network Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="e1bad-111">List all available Skus of Network Virtual Appliance.</span></span>

## <span data-ttu-id="e1bad-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1bad-112">PARAMETERS</span></span>

### <span data-ttu-id="e1bad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1bad-113">-DefaultProfile</span></span>
<span data-ttu-id="e1bad-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e1bad-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1bad-115">-SKUName</span><span class="sxs-lookup"><span data-stu-id="e1bad-115">-SkuName</span></span>
<span data-ttu-id="e1bad-116">Nome della SKU.</span><span class="sxs-lookup"><span data-stu-id="e1bad-116">The Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1bad-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1bad-117">CommonParameters</span></span>
<span data-ttu-id="e1bad-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1bad-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1bad-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e1bad-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1bad-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="e1bad-120">INPUTS</span></span>

### <span data-ttu-id="e1bad-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e1bad-121">None</span></span>

## <span data-ttu-id="e1bad-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1bad-122">OUTPUTS</span></span>

### <span data-ttu-id="e1bad-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="e1bad-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="e1bad-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="e1bad-124">NOTES</span></span>

## <span data-ttu-id="e1bad-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1bad-125">RELATED LINKS</span></span>
