---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: 028c33db36df5debb6f951f11e27f0586e7a21dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192768"
---
# <span data-ttu-id="6eec5-101">New-AzVpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="6eec5-101">New-AzVpnClientIpsecPolicy</span></span>

## <span data-ttu-id="6eec5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6eec5-102">SYNOPSIS</span></span>
<span data-ttu-id="6eec5-103">Questo comando consente agli utenti di creare l'oggetto criteri IPSec VPN specificando uno o tutti i valori, ad esempio IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup, per impostare il gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="6eec5-103">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="6eec5-104">Questo comando consente di usare l'oggetto output per impostare i criteri IPSec VPN per il gateway nuovo/esistente.</span><span class="sxs-lookup"><span data-stu-id="6eec5-104">This command let output object is used to set vpn ipsec policy for both new / existing gateway.</span></span>

## <span data-ttu-id="6eec5-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6eec5-105">SYNTAX</span></span>

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6eec5-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6eec5-106">DESCRIPTION</span></span>
<span data-ttu-id="6eec5-107">Questo comando consente agli utenti di creare l'oggetto criteri IPSec VPN specificando uno o tutti i valori, ad esempio IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup, per impostare il gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="6eec5-107">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="6eec5-108">Questo comando consente di usare l'oggetto output per impostare i criteri IPSec VPN per il gateway nuovo/esistente.</span><span class="sxs-lookup"><span data-stu-id="6eec5-108">This command let output object is used to set vpn ipsec policy for both new / existing gateway.</span></span>

## <span data-ttu-id="6eec5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6eec5-109">EXAMPLES</span></span>

### <span data-ttu-id="6eec5-110">Esempio 1: definire l'oggetto criteri IPSec VPN:</span><span class="sxs-lookup"><span data-stu-id="6eec5-110">Example 1: Define vpn ipsec policy object:</span></span>
```powershell
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

<span data-ttu-id="6eec5-111">Questo cmdlet viene usato per creare l'oggetto criteri IPSec VPN usando i valori passati di uno o tutti i parametri che l'utente può passare a param: VpnClientIpsecPolicy of PS command let: New-AzVirtualNetworkGateway (nuova creazione di gateway VPN)/Set-AzVirtualNetworkGateway (aggiornamento del gateway VPN esistente) in ResourceGroup:</span><span class="sxs-lookup"><span data-stu-id="6eec5-111">This cmdlet is used to create the vpn ipsec policy object using the passed one or all parameters' values which user can pass to param:VpnClientIpsecPolicy of PS command let: New-AzVirtualNetworkGateway (New VPN Gateway creation) / Set-AzVirtualNetworkGateway (existing VPN Gateway update) in ResourceGroup :</span></span>

### <span data-ttu-id="6eec5-112">Esempio 2: creare un nuovo gateway di rete virtuale con l'impostazione di criteri IPSec personalizzati VPN:</span><span class="sxs-lookup"><span data-stu-id="6eec5-112">Example 2: Create new virtual network gateway with setting vpn custom ipsec policy:</span></span>
```powershell
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="6eec5-113">Questo cmdlet restituisce l'oggetto gateway di rete virtuale dopo la creazione.</span><span class="sxs-lookup"><span data-stu-id="6eec5-113">This cmdlet returns virtual network gateway object after creation.</span></span> 

### <span data-ttu-id="6eec5-114">Esempio 3: impostare i criteri IPSec personalizzati VPN nel gateway di rete virtuale esistente:</span><span class="sxs-lookup"><span data-stu-id="6eec5-114">Example 3: Set vpn custom ipsec policy on existing virtual network gateway:</span></span>
```powershell
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="6eec5-115">Questo cmdlet restituisce un oggetto gateway di rete virtuale dopo l'impostazione dei criteri IPSec personalizzati VPN.</span><span class="sxs-lookup"><span data-stu-id="6eec5-115">This cmdlet returns virtual network gateway object after setting vpn custom ipsec policy.</span></span>

### <span data-ttu-id="6eec5-116">Esempio 4: ottenere il gateway di rete virtuale per verificare se i criteri personalizzati di VPN sono impostati correttamente:</span><span class="sxs-lookup"><span data-stu-id="6eec5-116">Example 4: Get virtual network gateway to see if vpn custom policy is set correctly:</span></span>
```powershell
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

<span data-ttu-id="6eec5-117">Questo cmdlet restituisce l'oggetto gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="6eec5-117">This cmdlet returns virtual network gateway object.</span></span>

## <span data-ttu-id="6eec5-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6eec5-118">PARAMETERS</span></span>

### <span data-ttu-id="6eec5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eec5-119">-DefaultProfile</span></span>
<span data-ttu-id="6eec5-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6eec5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6eec5-121">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="6eec5-121">-DhGroup</span></span>
<span data-ttu-id="6eec5-122">I gruppi di VpnClient DH usati nella fase 1 IKE per la SA iniziale</span><span class="sxs-lookup"><span data-stu-id="6eec5-122">The VpnClient DH Groups used in IKE Phase 1 for initial SA</span></span>

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

### <span data-ttu-id="6eec5-123">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="6eec5-123">-IkeEncryption</span></span>
<span data-ttu-id="6eec5-124">Algoritmo di crittografia IKE VpnClient (fase 2 IKE)</span><span class="sxs-lookup"><span data-stu-id="6eec5-124">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="6eec5-125">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="6eec5-125">-IkeIntegrity</span></span>
<span data-ttu-id="6eec5-126">Algoritmo di integrità IKE di VpnClient (fase 2 IKE)</span><span class="sxs-lookup"><span data-stu-id="6eec5-126">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="6eec5-127">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="6eec5-127">-IpsecEncryption</span></span>
<span data-ttu-id="6eec5-128">Algoritmo di crittografia IPSec VpnClient (fase 1 IKE)</span><span class="sxs-lookup"><span data-stu-id="6eec5-128">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="6eec5-129">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="6eec5-129">-IpsecIntegrity</span></span>
<span data-ttu-id="6eec5-130">Algoritmo di integrità IPSec di VpnClient (fase 1 IKE)</span><span class="sxs-lookup"><span data-stu-id="6eec5-130">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="6eec5-131">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="6eec5-131">-PfsGroup</span></span>
<span data-ttu-id="6eec5-132">Gruppi PFS VpnClient usati nella fase 2 IKE per New Child SA</span><span class="sxs-lookup"><span data-stu-id="6eec5-132">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="6eec5-133">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="6eec5-133">-SADataSize</span></span>
<span data-ttu-id="6eec5-134">Associazione di sicurezza IPSec VpnClient (denominata anche modalità rapida o fase 2 SA) dimensione del payload in KB</span><span class="sxs-lookup"><span data-stu-id="6eec5-134">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="6eec5-135">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="6eec5-135">-SALifeTime</span></span>
<span data-ttu-id="6eec5-136">Associazione di sicurezza IPSec VpnClient (chiamata anche modalità rapida o fase 2 SA) durata in secondi</span><span class="sxs-lookup"><span data-stu-id="6eec5-136">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="6eec5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eec5-137">CommonParameters</span></span>
<span data-ttu-id="6eec5-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eec5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eec5-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6eec5-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eec5-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6eec5-140">INPUTS</span></span>

### <span data-ttu-id="6eec5-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6eec5-141">None</span></span>

## <span data-ttu-id="6eec5-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6eec5-142">OUTPUTS</span></span>

### <span data-ttu-id="6eec5-143">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="6eec5-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="6eec5-144">Note</span><span class="sxs-lookup"><span data-stu-id="6eec5-144">NOTES</span></span>

## <span data-ttu-id="6eec5-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6eec5-145">RELATED LINKS</span></span>