---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecPolicy.md
ms.openlocfilehash: 98ea39141614c800b7b71d2f0c75519762bb87b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521326"
---
# <span data-ttu-id="93c76-101">New-AzureRmVpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="93c76-101">New-AzureRmVpnClientIpsecPolicy</span></span>

## <span data-ttu-id="93c76-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="93c76-102">SYNOPSIS</span></span>
<span data-ttu-id="93c76-103">Questo comando consente agli utenti di creare l'oggetto criteri IPSec VPN specificando uno o tutti i valori, ad esempio IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup, per impostare il gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="93c76-103">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="93c76-104">Questo comando consente di usare l'oggetto output per impostare i criteri IPSec VPN per il gateway New/esistenti.</span><span class="sxs-lookup"><span data-stu-id="93c76-104">This command let output object is used to set vpn ipsec policy for both new / exisitng gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93c76-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93c76-105">SYNTAX</span></span>

```
New-AzureRmVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93c76-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93c76-106">DESCRIPTION</span></span>
<span data-ttu-id="93c76-107">Questo comando consente agli utenti di creare l'oggetto criteri IPSec VPN specificando uno o tutti i valori, ad esempio IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup, per impostare il gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="93c76-107">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="93c76-108">Questo comando consente di usare l'oggetto output per impostare i criteri IPSec VPN per il gateway New/esistenti.</span><span class="sxs-lookup"><span data-stu-id="93c76-108">This command let output object is used to set vpn ipsec policy for both new / exisitng gateway.</span></span>

## <span data-ttu-id="93c76-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93c76-109">EXAMPLES</span></span>

### <span data-ttu-id="93c76-110">Definire l'oggetto criteri IPSec VPN:</span><span class="sxs-lookup"><span data-stu-id="93c76-110">Define vpn ipsec policy object:</span></span>
```
PS C:\>$vpnclientipsecpolicy = New-AzureRmVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

<span data-ttu-id="93c76-111">Questo cmdlet viene usato per creare l'oggetto criteri IPSec VPN usando i valori passati di uno o tutti i parametri che l'utente può passare a param: VpnClientIpsecPolicy of PS command let: New-AzureRmVirtualNetworkGateway (nuova creazione di gateway VPN)/Set-AzureRmVirtualNetworkGateway (aggiornamento del gateway VPN esistente) in ResourceGroup:</span><span class="sxs-lookup"><span data-stu-id="93c76-111">This cmdlet is used to create the vpn ipsec policy object using the passed one or all parameters' values which user can pass to param:VpnClientIpsecPolicy of PS command let: New-AzureRmVirtualNetworkGateway (New VPN Gateway creation) / Set-AzureRmVirtualNetworkGateway (existing VPN Gateway update) in ResourceGroup :</span></span>

### <span data-ttu-id="93c76-112">Creare un nuovo gateway di rete virtuale con l'impostazione di criteri IPSec personalizzati VPN:</span><span class="sxs-lookup"><span data-stu-id="93c76-112">Create new virtual network gateway with setting vpn custom ipsec policy:</span></span>
```
PS C:\> $vnetGateway = New-AzureRmVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="93c76-113">Questo cmdlet restituisce l'oggetto gateway di rete virtuale dopo la creazione.</span><span class="sxs-lookup"><span data-stu-id="93c76-113">This cmdlet returns virtual network gateway object after creation.</span></span> 

### <span data-ttu-id="93c76-114">Impostare i criteri IPSec personalizzati VPN nel gateway di rete virtuale esistente:</span><span class="sxs-lookup"><span data-stu-id="93c76-114">Set vpn custom ipsec policy on existing virtual network gateway:</span></span>
```
PS C:\> $vnetGateway = Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="93c76-115">Questo cmdlet restituisce un oggetto gateway di rete virtuale dopo l'impostazione dei criteri IPSec personalizzati VPN.</span><span class="sxs-lookup"><span data-stu-id="93c76-115">This cmdlet returns virtual network gateway object after setting vpn custom ipsec policy.</span></span>

### <span data-ttu-id="93c76-116">Ottenere gateway di rete virtuale per verificare se i criteri personalizzati di VPN sono impostati correttamente:</span><span class="sxs-lookup"><span data-stu-id="93c76-116">Get virtual network gateway to see if vpn custom policy is set correctly:</span></span>
```
PS C:\> $gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

<span data-ttu-id="93c76-117">Questo cmdlet restituisce l'oggetto gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="93c76-117">This cmdlet returns virtual network gateway object.</span></span>

## <span data-ttu-id="93c76-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="93c76-118">PARAMETERS</span></span>

### <span data-ttu-id="93c76-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93c76-119">-DefaultProfile</span></span>
<span data-ttu-id="93c76-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="93c76-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93c76-121">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="93c76-121">-DhGroup</span></span>
<span data-ttu-id="93c76-122">I gruppi di vpnclient DH usati nella fase 1 IKE per la SA iniziale</span><span class="sxs-lookup"><span data-stu-id="93c76-122">The Vpnclient DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DHGroup24, ECP384, ECP256, DHGroup14, DHGroup2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93c76-123">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="93c76-123">-IkeEncryption</span></span>
<span data-ttu-id="93c76-124">Algoritmo di crittografia IKE vpnclient (fase 2 IKE)</span><span class="sxs-lookup"><span data-stu-id="93c76-124">The Vpnclient IKE encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93c76-125">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="93c76-125">-IkeIntegrity</span></span>
<span data-ttu-id="93c76-126">Algoritmo di integrità IKE di vpnclient (fase 2 IKE)</span><span class="sxs-lookup"><span data-stu-id="93c76-126">The Vpnclient IKE integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SHA384, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93c76-127">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="93c76-127">-IpsecEncryption</span></span>
<span data-ttu-id="93c76-128">Algoritmo di crittografia IPSec vpnclient (fase 1 IKE)</span><span class="sxs-lookup"><span data-stu-id="93c76-128">The Vpnclient IPSec encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93c76-129">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="93c76-129">-IpsecIntegrity</span></span>
<span data-ttu-id="93c76-130">Algoritmo di integrità IPSec di vpnclient (fase 1 IKE)</span><span class="sxs-lookup"><span data-stu-id="93c76-130">The Vpnclient IPSec integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93c76-131">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="93c76-131">-PfsGroup</span></span>
<span data-ttu-id="93c76-132">Gruppi PFS vpnclient usati nella fase 2 IKE per New Child SA</span><span class="sxs-lookup"><span data-stu-id="93c76-132">The Vpnclient PFS Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PFS24, PFSMM, ECP384, ECP256, PFS14, PFS2, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93c76-133">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="93c76-133">-SADataSize</span></span>
<span data-ttu-id="93c76-134">Associazione di sicurezza IPSec vpnclient (denominata anche modalità rapida o fase 2 SA) dimensione del payload in KB</span><span class="sxs-lookup"><span data-stu-id="93c76-134">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93c76-135">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="93c76-135">-SALifeTime</span></span>
<span data-ttu-id="93c76-136">Associazione di sicurezza IPSec vpnclient (chiamata anche modalità rapida o fase 2 SA) durata in secondi</span><span class="sxs-lookup"><span data-stu-id="93c76-136">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93c76-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93c76-137">CommonParameters</span></span>
<span data-ttu-id="93c76-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93c76-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93c76-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93c76-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93c76-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="93c76-140">INPUTS</span></span>

### <span data-ttu-id="93c76-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="93c76-141">None</span></span>

## <span data-ttu-id="93c76-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93c76-142">OUTPUTS</span></span>

### <span data-ttu-id="93c76-143">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="93c76-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="93c76-144">Note</span><span class="sxs-lookup"><span data-stu-id="93c76-144">NOTES</span></span>

## <span data-ttu-id="93c76-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93c76-145">RELATED LINKS</span></span>
