---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
ms.openlocfilehash: 444addf1b7f036ffc4fcaae4a1070b9238c29dc0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965678"
---
# <span data-ttu-id="61185-101">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="61185-101">Get-AzVpnSite</span></span>

## <span data-ttu-id="61185-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61185-102">SYNOPSIS</span></span>
<span data-ttu-id="61185-103">Ottiene una risorsa VpnSite di Azure in base al nome O elenca tutti i siti Vpn in un ResourceGroup o SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="61185-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="61185-104">Si tratta di una rappresentazione RM dei rami dei clienti caricati in Connettività di Azure per S2S con un hub virtuale di Cortex.</span><span class="sxs-lookup"><span data-stu-id="61185-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="61185-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61185-105">SYNTAX</span></span>

### <span data-ttu-id="61185-106">ListBySubscriptionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="61185-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61185-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61185-107">ListByResourceGroupName</span></span>
```
Get-AzVpnSite [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61185-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="61185-108">DESCRIPTION</span></span>
<span data-ttu-id="61185-109">Ottiene una risorsa VpnSite di Azure in base al nome O elenca tutti i siti Vpn in un ResourceGroup o SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="61185-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="61185-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61185-110">EXAMPLES</span></span>

### <span data-ttu-id="61185-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="61185-111">Example 1</span></span>

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

<span data-ttu-id="61185-112">La procedura descritta sopra creerà un gruppo di risorse, Virtual WAN negli Stati Uniti occidentali, nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="61185-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="61185-113">Viene quindi creato un sito Vpn che rappresenta un ramo del cliente e lo collega alla WAN virtuale.</span><span class="sxs-lookup"><span data-stu-id="61185-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="61185-114">Una volta creato, il sito viene creato usando il comando Get-AzVpnSite sito.</span><span class="sxs-lookup"><span data-stu-id="61185-114">Once the site is created, it gets the site using the Get-AzVpnSite command.</span></span>

### <span data-ttu-id="61185-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="61185-115">Example 2</span></span>

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

<span data-ttu-id="61185-116">Questo cmdlet recupera tutti i siti che iniziano con "test".</span><span class="sxs-lookup"><span data-stu-id="61185-116">This cmdlet gets all Sites that start with "test".</span></span>

## <span data-ttu-id="61185-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61185-117">PARAMETERS</span></span>

### <span data-ttu-id="61185-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61185-118">-DefaultProfile</span></span>
<span data-ttu-id="61185-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61185-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61185-120">-Name</span><span class="sxs-lookup"><span data-stu-id="61185-120">-Name</span></span>
<span data-ttu-id="61185-121">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="61185-121">The resource name.</span></span>

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

### <span data-ttu-id="61185-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61185-122">-ResourceGroupName</span></span>
<span data-ttu-id="61185-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="61185-123">The resource group name.</span></span>

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

### <span data-ttu-id="61185-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61185-124">CommonParameters</span></span>
<span data-ttu-id="61185-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61185-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61185-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="61185-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61185-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="61185-127">INPUTS</span></span>

### <span data-ttu-id="61185-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="61185-128">None</span></span>

## <span data-ttu-id="61185-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61185-129">OUTPUTS</span></span>

### <span data-ttu-id="61185-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="61185-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="61185-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="61185-131">NOTES</span></span>

## <span data-ttu-id="61185-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61185-132">RELATED LINKS</span></span>

[<span data-ttu-id="61185-133">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="61185-133">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="61185-134">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="61185-134">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="61185-135">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="61185-135">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
