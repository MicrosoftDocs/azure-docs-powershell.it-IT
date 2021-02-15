---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: 028c33db36df5debb6f951f11e27f0586e7a21dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193543"
---
# <span data-ttu-id="c5c79-101">New-AzVpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="c5c79-101">New-AzVpnClientIpsecPolicy</span></span>

## <span data-ttu-id="c5c79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5c79-102">SYNOPSIS</span></span>
<span data-ttu-id="c5c79-103">Questo comando consente agli utenti di creare l'oggetto criterio Ipsec Vpn specificando uno o tutti i valori come IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup da impostare nel gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="c5c79-103">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="c5c79-104">Questo comando consente di usare l'oggetto di output per impostare il criterio ipsec vpn per un gateway nuovo o esistente.</span><span class="sxs-lookup"><span data-stu-id="c5c79-104">This command let output object is used to set vpn ipsec policy for both new / existing gateway.</span></span>

## <span data-ttu-id="c5c79-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5c79-105">SYNTAX</span></span>

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5c79-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c5c79-106">DESCRIPTION</span></span>
<span data-ttu-id="c5c79-107">Questo comando consente agli utenti di creare l'oggetto criterio Ipsec Vpn specificando uno o tutti i valori come IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup da impostare nel gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="c5c79-107">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="c5c79-108">Questo comando consente di usare l'oggetto di output per impostare il criterio ipsec vpn per un gateway nuovo o esistente.</span><span class="sxs-lookup"><span data-stu-id="c5c79-108">This command let output object is used to set vpn ipsec policy for both new / existing gateway.</span></span>

## <span data-ttu-id="c5c79-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5c79-109">EXAMPLES</span></span>

### <span data-ttu-id="c5c79-110">Esempio 1: Definire l'oggetto criterio IPSec vpn:</span><span class="sxs-lookup"><span data-stu-id="c5c79-110">Example 1: Define vpn ipsec policy object:</span></span>
```powershell
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

<span data-ttu-id="c5c79-111">Questo cmdlet viene usato per creare l'oggetto criterio ipsec vpn usando i valori passati per uno o tutti i parametri che l'utente può passare al param:VpnClientIpsecPolicy del comando PS let: New-AzVirtualNetworkGateway (creazione nuovo gateway VPN) / Set-AzVirtualNetworkGateway (aggiornamento del Gateway VPN esistente) in ResourceGroup:</span><span class="sxs-lookup"><span data-stu-id="c5c79-111">This cmdlet is used to create the vpn ipsec policy object using the passed one or all parameters' values which user can pass to param:VpnClientIpsecPolicy of PS command let: New-AzVirtualNetworkGateway (New VPN Gateway creation) / Set-AzVirtualNetworkGateway (existing VPN Gateway update) in ResourceGroup :</span></span>

### <span data-ttu-id="c5c79-112">Esempio 2: Creare un nuovo gateway di rete virtuale con l'impostazione del criterio ipsec personalizzato vpn:</span><span class="sxs-lookup"><span data-stu-id="c5c79-112">Example 2: Create new virtual network gateway with setting vpn custom ipsec policy:</span></span>
```powershell
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="c5c79-113">Questo cmdlet restituisce l'oggetto gateway di rete virtuale dopo la creazione.</span><span class="sxs-lookup"><span data-stu-id="c5c79-113">This cmdlet returns virtual network gateway object after creation.</span></span> 

### <span data-ttu-id="c5c79-114">Esempio 3: Impostare i criteri IPSec personalizzati della vpn in un gateway di rete virtuale esistente:</span><span class="sxs-lookup"><span data-stu-id="c5c79-114">Example 3: Set vpn custom ipsec policy on existing virtual network gateway:</span></span>
```powershell
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="c5c79-115">Questo cmdlet restituisce l'oggetto gateway di rete virtuale dopo l'impostazione del criterio ipsec personalizzato vpn.</span><span class="sxs-lookup"><span data-stu-id="c5c79-115">This cmdlet returns virtual network gateway object after setting vpn custom ipsec policy.</span></span>

### <span data-ttu-id="c5c79-116">Esempio 4: Ottenere il gateway di rete virtuale per verificare se il criterio personalizzato vpn è impostato correttamente:</span><span class="sxs-lookup"><span data-stu-id="c5c79-116">Example 4: Get virtual network gateway to see if vpn custom policy is set correctly:</span></span>
```powershell
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

<span data-ttu-id="c5c79-117">Questo cmdlet restituisce l'oggetto gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c5c79-117">This cmdlet returns virtual network gateway object.</span></span>

## <span data-ttu-id="c5c79-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5c79-118">PARAMETERS</span></span>

### <span data-ttu-id="c5c79-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5c79-119">-DefaultProfile</span></span>
<span data-ttu-id="c5c79-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c5c79-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5c79-121">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="c5c79-121">-DhGroup</span></span>
<span data-ttu-id="c5c79-122">Gruppi VpnClient DH usati nella fase 1 di IKE per l'accesso condiviso iniziale</span><span class="sxs-lookup"><span data-stu-id="c5c79-122">The VpnClient DH Groups used in IKE Phase 1 for initial SA</span></span>

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

### <span data-ttu-id="c5c79-123">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="c5c79-123">-IkeEncryption</span></span>
<span data-ttu-id="c5c79-124">Algoritmo di crittografia IKE per VpnClient (Fase IKE 2)</span><span class="sxs-lookup"><span data-stu-id="c5c79-124">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="c5c79-125">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="c5c79-125">-IkeIntegrity</span></span>
<span data-ttu-id="c5c79-126">Algoritmo di integrità IKE di VpnClient (Fase IKE 2)</span><span class="sxs-lookup"><span data-stu-id="c5c79-126">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="c5c79-127">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="c5c79-127">-IpsecEncryption</span></span>
<span data-ttu-id="c5c79-128">Algoritmo di crittografia IPSec VpnClient (Fase IKE 1)</span><span class="sxs-lookup"><span data-stu-id="c5c79-128">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="c5c79-129">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="c5c79-129">-IpsecIntegrity</span></span>
<span data-ttu-id="c5c79-130">Algoritmo di integrità IPSec di VpnClient (Fase IKE 1)</span><span class="sxs-lookup"><span data-stu-id="c5c79-130">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="c5c79-131">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="c5c79-131">-PfsGroup</span></span>
<span data-ttu-id="c5c79-132">Gruppi PFS VpnClient usati nella fase 2 di IKE per la nuova sa figlio</span><span class="sxs-lookup"><span data-stu-id="c5c79-132">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="c5c79-133">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="c5c79-133">-SADataSize</span></span>
<span data-ttu-id="c5c79-134">Dimensioni del payload della modalità rapida o sa della fase 2 in KB per l'associazione di sicurezza IPSec vpn</span><span class="sxs-lookup"><span data-stu-id="c5c79-134">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="c5c79-135">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="c5c79-135">-SALifeTime</span></span>
<span data-ttu-id="c5c79-136">Durata in secondi dell'associazione di sicurezza IPSec di VpnClient (chiamata anche modalità rapida o SA di fase 2)</span><span class="sxs-lookup"><span data-stu-id="c5c79-136">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="c5c79-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5c79-137">CommonParameters</span></span>
<span data-ttu-id="c5c79-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5c79-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5c79-139">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5c79-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5c79-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="c5c79-140">INPUTS</span></span>

### <span data-ttu-id="c5c79-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c5c79-141">None</span></span>

## <span data-ttu-id="c5c79-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5c79-142">OUTPUTS</span></span>

### <span data-ttu-id="c5c79-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="c5c79-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="c5c79-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="c5c79-144">NOTES</span></span>

## <span data-ttu-id="c5c79-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5c79-145">RELATED LINKS</span></span>
