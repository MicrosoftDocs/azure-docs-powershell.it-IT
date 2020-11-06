---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnSite.md
ms.openlocfilehash: 0277e61a6b1b180691908b2e86c0050eb8d62b1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513708"
---
# <span data-ttu-id="1b822-101">Get-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="1b822-101">Get-AzureRmVpnSite</span></span>

## <span data-ttu-id="1b822-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1b822-102">SYNOPSIS</span></span>
<span data-ttu-id="1b822-103">Ottiene una risorsa di Azure VpnSite per nome o elenca tutti i VpnSites in un ResourceGroup o SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="1b822-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="1b822-104">Questa è una rappresentazione RM delle branche del cliente caricata in Azure per la connettività S2S con un hub virtuale Cortex.</span><span class="sxs-lookup"><span data-stu-id="1b822-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b822-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b822-105">SYNTAX</span></span>

### <span data-ttu-id="1b822-106">ListBySubscriptionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1b822-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b822-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b822-107">ListByResourceGroupName</span></span>
```
Get-AzureRmVpnSite -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b822-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b822-108">DESCRIPTION</span></span>
<span data-ttu-id="1b822-109">Ottiene una risorsa di Azure VpnSite per nome o elenca tutti i VpnSites in un ResourceGroup o SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="1b822-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="1b822-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b822-110">EXAMPLES</span></span>

### <span data-ttu-id="1b822-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1b822-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"

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

<span data-ttu-id="1b822-112">Quanto sopra creerà un gruppo di risorse, Virtual WAN in West US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="1b822-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="1b822-113">Crea quindi un VpnSite per rappresentare un ramo Customer e lo collega alla rete WAN virtuale.</span><span class="sxs-lookup"><span data-stu-id="1b822-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="1b822-114">Dopo aver creato il sito, il sito viene usato tramite il comando Get-AzureRmVpnSite.</span><span class="sxs-lookup"><span data-stu-id="1b822-114">Once the site is created, it gets the site using the Get-AzureRmVpnSite command.</span></span>

## <span data-ttu-id="1b822-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1b822-115">PARAMETERS</span></span>

### <span data-ttu-id="1b822-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b822-116">-DefaultProfile</span></span>
<span data-ttu-id="1b822-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b822-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b822-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="1b822-118">-Name</span></span>
<span data-ttu-id="1b822-119">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="1b822-119">The resource name.</span></span>

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

### <span data-ttu-id="1b822-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b822-120">-ResourceGroupName</span></span>
<span data-ttu-id="1b822-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1b822-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b822-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b822-122">CommonParameters</span></span>
<span data-ttu-id="1b822-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b822-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b822-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b822-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b822-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1b822-125">INPUTS</span></span>

### <span data-ttu-id="1b822-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1b822-126">None</span></span>

## <span data-ttu-id="1b822-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b822-127">OUTPUTS</span></span>

### <span data-ttu-id="1b822-128">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="1b822-128">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="1b822-129">Note</span><span class="sxs-lookup"><span data-stu-id="1b822-129">NOTES</span></span>

## <span data-ttu-id="1b822-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b822-130">RELATED LINKS</span></span>
