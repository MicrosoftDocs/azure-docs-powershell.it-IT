---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzAvailabilitySet.md
ms.openlocfilehash: 223f309fb0381f75a6398c44209baa2f3eb3bc22
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969389"
---
# <span data-ttu-id="41083-101">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="41083-101">Get-AzAvailabilitySet</span></span>

## <span data-ttu-id="41083-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41083-102">SYNOPSIS</span></span>
<span data-ttu-id="41083-103">Ottiene i set di disponibilità di Azure in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="41083-103">Gets Azure availability sets in a resource group.</span></span>

## <span data-ttu-id="41083-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41083-104">SYNTAX</span></span>

```
Get-AzAvailabilitySet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41083-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="41083-105">DESCRIPTION</span></span>
<span data-ttu-id="41083-106">Il cmdlet **Get-AzAvailabilitySet** ottiene i set di disponibilità di Azure in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="41083-106">The **Get-AzAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="41083-107">È possibile specificare il nome di un set di disponibilità specifico da ottenere.</span><span class="sxs-lookup"><span data-stu-id="41083-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="41083-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41083-108">EXAMPLES</span></span>

### <span data-ttu-id="41083-109">Esempio 1: Ottenere un set di disponibilità specifico</span><span class="sxs-lookup"><span data-stu-id="41083-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="41083-110">Questo comando ottiene il set di disponibilità denominato AvailabilitySet03 nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="41083-110">This command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="41083-111">Esempio 2: Ottenere tutti i set di disponibilità</span><span class="sxs-lookup"><span data-stu-id="41083-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet10
Name                      : AvailabilitySet10
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="41083-112">Questo comando recupera tutti i set di disponibilità nel gruppo di risorse denominato Gruppo ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="41083-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="41083-113">Esempio 3: Ottenere tutti i set di disponibilità con i filtri</span><span class="sxs-lookup"><span data-stu-id="41083-113">Example 3: Get all availability sets with filtering</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup1*" -Name "AvailabilitySet0*"

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="41083-114">Questo comando recupera tutti i set di disponibilità nel gruppo di risorse denominato ResourceGroup11 che iniziano con "AvailabilitySet0".</span><span class="sxs-lookup"><span data-stu-id="41083-114">This command gets all the availability sets in the resource group named ResourceGroup11 that start with "AvailabilitySet0".</span></span>

### <span data-ttu-id="41083-115">Esempio 4: Ottenere tutti i set di disponibilità con un nome che inizia con AvailabilitySet0</span><span class="sxs-lookup"><span data-stu-id="41083-115">Example 4: Get all availability sets with name starting with AvailabilitySet0</span></span>
```
PS C:\> Get-AzAvailabilitySet -Name AvailabilitySet0*

ResourceGroupName         : ResourceGroup11
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet02
Name                      : AvailabilitySet02
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []


ResourceGroupName         : ResourceGroup12
Id                        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup12/providers/
                            Microsoft.Compute/availabilitySets/AvailabilitySet03
Name                      : AvailabilitySet03
Type                      : Microsoft.Compute/availabilitySets
Location                  : eastus
Managed                   : False
Sku                       : Classic
Tags                      : {
                              "a": "b"
                            }
PlatformFaultDomainCount  : 3
PlatformUpdateDomainCount : 2
Statuses                  : []
VirtualMachinesReferences : []
```

<span data-ttu-id="41083-116">Questo comando ottiene tutti i set di disponibilità che iniziano con "AvailabilitySet0".</span><span class="sxs-lookup"><span data-stu-id="41083-116">This command gets all the availability sets that start with "AvailabilitySet0".</span></span>

## <span data-ttu-id="41083-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41083-117">PARAMETERS</span></span>

### <span data-ttu-id="41083-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41083-118">-DefaultProfile</span></span>
<span data-ttu-id="41083-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="41083-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41083-120">-Name</span><span class="sxs-lookup"><span data-stu-id="41083-120">-Name</span></span>
<span data-ttu-id="41083-121">Specifica il nome di un set di disponibilità che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41083-121">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="41083-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41083-122">-ResourceGroupName</span></span>
<span data-ttu-id="41083-123">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="41083-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="41083-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41083-124">CommonParameters</span></span>
<span data-ttu-id="41083-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41083-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41083-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="41083-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41083-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="41083-127">INPUTS</span></span>

### <span data-ttu-id="41083-128">System.String</span><span class="sxs-lookup"><span data-stu-id="41083-128">System.String</span></span>

## <span data-ttu-id="41083-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41083-129">OUTPUTS</span></span>

### <span data-ttu-id="41083-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="41083-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="41083-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="41083-131">NOTES</span></span>

## <span data-ttu-id="41083-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41083-132">RELATED LINKS</span></span>

[<span data-ttu-id="41083-133">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="41083-133">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)

[<span data-ttu-id="41083-134">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="41083-134">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


