---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
ms.openlocfilehash: 7e53c6828fa5c7bae40037f2fd64bb06ddf0be45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852837"
---
# <span data-ttu-id="b77a2-101">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="b77a2-101">New-AzVpnSiteLink</span></span>

## <span data-ttu-id="b77a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b77a2-102">SYNOPSIS</span></span>
<span data-ttu-id="b77a2-103">Crea un oggetto VpnSiteLink di Azure.</span><span class="sxs-lookup"><span data-stu-id="b77a2-103">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="b77a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b77a2-104">SYNTAX</span></span>

```
New-AzVpnSiteLink -Name <String> -IPAddress <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b77a2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b77a2-105">DESCRIPTION</span></span>
<span data-ttu-id="b77a2-106">Crea un oggetto VpnSiteLink di Azure.</span><span class="sxs-lookup"><span data-stu-id="b77a2-106">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="b77a2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b77a2-107">EXAMPLES</span></span>

### <span data-ttu-id="b77a2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b77a2-108">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)
```

<span data-ttu-id="b77a2-109">Il precedente creerà un gruppo di risorse, una WAN virtuale e un VpnSite con 1 VpnSiteLinks in West US nel gruppo di risorse "testRG" in Azure.</span><span class="sxs-lookup"><span data-stu-id="b77a2-109">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>

## <span data-ttu-id="b77a2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b77a2-110">PARAMETERS</span></span>

### <span data-ttu-id="b77a2-111">-BGPAsn</span><span class="sxs-lookup"><span data-stu-id="b77a2-111">-BGPAsn</span></span>
<span data-ttu-id="b77a2-112">BGP ASN per questo VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="b77a2-112">The BGP ASN for this VpnSiteLink.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b77a2-113">-BGPPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="b77a2-113">-BGPPeeringAddress</span></span>
<span data-ttu-id="b77a2-114">Indirizzo di peering BGP per questo VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="b77a2-114">The BGP Peering Address for this VpnSiteLink.</span></span>

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

### <span data-ttu-id="b77a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b77a2-115">-DefaultProfile</span></span>
<span data-ttu-id="b77a2-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b77a2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b77a2-117">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="b77a2-117">-IPAddress</span></span>
<span data-ttu-id="b77a2-118">L'hop successivo IpAddress.</span><span class="sxs-lookup"><span data-stu-id="b77a2-118">The Next Hop IpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b77a2-119">-LinkProviderName</span><span class="sxs-lookup"><span data-stu-id="b77a2-119">-LinkProviderName</span></span>
<span data-ttu-id="b77a2-120">Nome del provider di collegamenti.</span><span class="sxs-lookup"><span data-stu-id="b77a2-120">Link Provider Name.</span></span>

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

### <span data-ttu-id="b77a2-121">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="b77a2-121">-LinkSpeedInMbps</span></span>
<span data-ttu-id="b77a2-122">Velocità di collegamento in Mbps.</span><span class="sxs-lookup"><span data-stu-id="b77a2-122">Link Speed In Mbps.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b77a2-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="b77a2-123">-Name</span></span>
<span data-ttu-id="b77a2-124">Nome</span><span class="sxs-lookup"><span data-stu-id="b77a2-124">Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b77a2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b77a2-125">CommonParameters</span></span>
<span data-ttu-id="b77a2-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b77a2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b77a2-127">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b77a2-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b77a2-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b77a2-128">INPUTS</span></span>

### <span data-ttu-id="b77a2-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b77a2-129">None</span></span>

## <span data-ttu-id="b77a2-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b77a2-130">OUTPUTS</span></span>

### <span data-ttu-id="b77a2-131">Microsoft. Azure. Commands. Network. Models. PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="b77a2-131">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="b77a2-132">Note</span><span class="sxs-lookup"><span data-stu-id="b77a2-132">NOTES</span></span>

## <span data-ttu-id="b77a2-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b77a2-133">RELATED LINKS</span></span>

[<span data-ttu-id="b77a2-134">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="b77a2-134">New-AzVpnSite</span></span>](./New-AzVpnSite.md)