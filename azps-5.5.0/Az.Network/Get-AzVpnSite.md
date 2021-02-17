---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
ms.openlocfilehash: 44a40fb446904c8d1bfa40820ae34e0a4aca2caa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184559"
---
# <span data-ttu-id="3e34f-101">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="3e34f-101">Get-AzVpnSite</span></span>

## <span data-ttu-id="3e34f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e34f-102">SYNOPSIS</span></span>
<span data-ttu-id="3e34f-103">Ottiene una risorsa VpnSite di Azure in base al nome O elenca tutti i siti Vpn in un ResourceGroup o SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="3e34f-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="3e34f-104">Si tratta di una rappresentazione RM dei rami dei clienti caricati in Connettività di Azure per S2S con un hub virtuale di Cortex.</span><span class="sxs-lookup"><span data-stu-id="3e34f-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="3e34f-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e34f-105">SYNTAX</span></span>

### <span data-ttu-id="3e34f-106">ListBySubscriptionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3e34f-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e34f-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e34f-107">ListByResourceGroupName</span></span>
```
Get-AzVpnSite [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e34f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3e34f-108">DESCRIPTION</span></span>
<span data-ttu-id="3e34f-109">Ottiene una risorsa VpnSite di Azure in base al nome O elenca tutti i siti Vpn in un ResourceGroup o SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="3e34f-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="3e34f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e34f-110">EXAMPLES</span></span>

### <span data-ttu-id="3e34f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3e34f-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="3e34f-112">Come descritto in precedenza verrà creato un gruppo di risorse, wan virtuale negli Stati Uniti occidentali, nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="3e34f-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="3e34f-113">Viene quindi creato un sito Vpn che rappresenta un ramo di un cliente e lo collega alla WAN virtuale.</span><span class="sxs-lookup"><span data-stu-id="3e34f-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="3e34f-114">Una volta creato, il sito viene creato usando il comando Get-AzVpnSite sito.</span><span class="sxs-lookup"><span data-stu-id="3e34f-114">Once the site is created, it gets the site using the Get-AzVpnSite command.</span></span>

### <span data-ttu-id="3e34f-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3e34f-115">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnSite -Name test*

ResourceGroupName : testRG
Name              : testVpnSite1
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite1
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded

ResourceGroupName : testRG
Name              : testVpnSite2
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite2
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="3e34f-116">Questo cmdlet recupera tutti i siti che iniziano con "test".</span><span class="sxs-lookup"><span data-stu-id="3e34f-116">This cmdlet gets all Sites that start with "test".</span></span>

## <span data-ttu-id="3e34f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e34f-117">PARAMETERS</span></span>

### <span data-ttu-id="3e34f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e34f-118">-DefaultProfile</span></span>
<span data-ttu-id="3e34f-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e34f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e34f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3e34f-120">-Name</span></span>
<span data-ttu-id="3e34f-121">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="3e34f-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnSiteName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e34f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e34f-122">-ResourceGroupName</span></span>
<span data-ttu-id="3e34f-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3e34f-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e34f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e34f-124">CommonParameters</span></span>
<span data-ttu-id="3e34f-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e34f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e34f-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3e34f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e34f-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="3e34f-127">INPUTS</span></span>

### <span data-ttu-id="3e34f-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3e34f-128">None</span></span>

## <span data-ttu-id="3e34f-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e34f-129">OUTPUTS</span></span>

### <span data-ttu-id="3e34f-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="3e34f-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="3e34f-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="3e34f-131">NOTES</span></span>

## <span data-ttu-id="3e34f-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e34f-132">RELATED LINKS</span></span>

[<span data-ttu-id="3e34f-133">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="3e34f-133">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="3e34f-134">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="3e34f-134">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="3e34f-135">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="3e34f-135">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
