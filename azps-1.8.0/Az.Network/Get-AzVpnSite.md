---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
ms.openlocfilehash: aad8b9c253dadfa199a16e3cf0a996c430b3b7d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678402"
---
# <span data-ttu-id="651f4-101">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="651f4-101">Get-AzVpnSite</span></span>

## <span data-ttu-id="651f4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="651f4-102">SYNOPSIS</span></span>
<span data-ttu-id="651f4-103">Ottiene una risorsa di Azure VpnSite per nome o elenca tutti i VpnSites in un ResourceGroup o SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="651f4-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="651f4-104">Questa è una rappresentazione RM delle branche del cliente caricata in Azure per la connettività S2S con un hub virtuale Cortex.</span><span class="sxs-lookup"><span data-stu-id="651f4-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="651f4-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="651f4-105">SYNTAX</span></span>

### <span data-ttu-id="651f4-106">ListBySubscriptionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="651f4-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="651f4-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="651f4-107">ListByResourceGroupName</span></span>
```
Get-AzVpnSite [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="651f4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="651f4-108">DESCRIPTION</span></span>
<span data-ttu-id="651f4-109">Ottiene una risorsa di Azure VpnSite per nome o elenca tutti i VpnSites in un ResourceGroup o SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="651f4-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="651f4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="651f4-110">EXAMPLES</span></span>

### <span data-ttu-id="651f4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="651f4-111">Example 1</span></span>

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

<span data-ttu-id="651f4-112">Quanto sopra creerà un gruppo di risorse, Virtual WAN in West US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="651f4-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="651f4-113">Crea quindi un VpnSite per rappresentare un ramo Customer e lo collega alla rete WAN virtuale.</span><span class="sxs-lookup"><span data-stu-id="651f4-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="651f4-114">Dopo aver creato il sito, il sito viene usato tramite il comando Get-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="651f4-114">Once the site is created, it gets the site using the Get-AzVpnSite command.</span></span>

### <span data-ttu-id="651f4-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="651f4-115">Example 2</span></span>

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

<span data-ttu-id="651f4-116">Questo cmdlet consente di ottenere tutti i siti che iniziano con "test".</span><span class="sxs-lookup"><span data-stu-id="651f4-116">This cmdlet gets all Sites that start with "test".</span></span>

## <span data-ttu-id="651f4-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="651f4-117">PARAMETERS</span></span>

### <span data-ttu-id="651f4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="651f4-118">-DefaultProfile</span></span>
<span data-ttu-id="651f4-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="651f4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="651f4-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="651f4-120">-Name</span></span>
<span data-ttu-id="651f4-121">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="651f4-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnSiteName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="651f4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="651f4-122">-ResourceGroupName</span></span>
<span data-ttu-id="651f4-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="651f4-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="651f4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="651f4-124">CommonParameters</span></span>
<span data-ttu-id="651f4-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="651f4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="651f4-126">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="651f4-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="651f4-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="651f4-127">INPUTS</span></span>

### <span data-ttu-id="651f4-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="651f4-128">None</span></span>

## <span data-ttu-id="651f4-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="651f4-129">OUTPUTS</span></span>

### <span data-ttu-id="651f4-130">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="651f4-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="651f4-131">Note</span><span class="sxs-lookup"><span data-stu-id="651f4-131">NOTES</span></span>

## <span data-ttu-id="651f4-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="651f4-132">RELATED LINKS</span></span>

[<span data-ttu-id="651f4-133">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="651f4-133">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="651f4-134">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="651f4-134">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="651f4-135">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="651f4-135">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)