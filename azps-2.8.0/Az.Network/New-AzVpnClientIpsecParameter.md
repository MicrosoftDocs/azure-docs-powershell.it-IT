---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 975826c459111e900e733b751c15d854c54ee2a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854369"
---
# <span data-ttu-id="bb31d-101">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="bb31d-101">New-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="bb31d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bb31d-102">SYNOPSIS</span></span>
<span data-ttu-id="bb31d-103">Questo comando consente agli utenti di creare l'oggetto parametri IPSec VPN specificando uno o tutti i valori, ad esempio IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup, per impostare il gateway VPN esistente.</span><span class="sxs-lookup"><span data-stu-id="bb31d-103">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="bb31d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb31d-104">SYNTAX</span></span>

```
New-AzVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb31d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb31d-105">DESCRIPTION</span></span>
<span data-ttu-id="bb31d-106">Questo comando consente agli utenti di creare l'oggetto parametri IPSec VPN specificando uno o tutti i valori, ad esempio IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup, per impostare il gateway VPN esistente.</span><span class="sxs-lookup"><span data-stu-id="bb31d-106">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="bb31d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb31d-107">EXAMPLES</span></span>

### <span data-ttu-id="bb31d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bb31d-108">Example 1</span></span>
```
PS C:\> $vpnclientipsecparams1 = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

<span data-ttu-id="bb31d-109">New-AzVpnClientIpsecParameter cmdlet viene usato per creare l'oggetto parametri IPSec VPN usando i valori passati di uno o tutti i parametri che l'utente può impostare per qualsiasi gateway di rete virtuale esistente in ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="bb31d-109">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="bb31d-110">Questo oggetto VpnClientIPsecParameters creato viene passato al comando Set-AzVpnClientIpsecParameter per impostare i criteri personalizzati IPSec VPN specificati nel gateway di rete virtuale, come illustrato nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="bb31d-110">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="bb31d-111">Questo comando restituisce l'oggetto di VpnClientIPsecParameters che mostra i parametri impostati.</span><span class="sxs-lookup"><span data-stu-id="bb31d-111">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="bb31d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bb31d-112">PARAMETERS</span></span>

### <span data-ttu-id="bb31d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb31d-113">-DefaultProfile</span></span>
<span data-ttu-id="bb31d-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bb31d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb31d-115">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="bb31d-115">-DhGroup</span></span>
<span data-ttu-id="bb31d-116">I gruppi di VpnClient DH usati nella fase 1 IKE per la SA iniziale.</span><span class="sxs-lookup"><span data-stu-id="bb31d-116">The VpnClient DH Groups used in IKE Phase 1 for initial SA.</span></span>

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

### <span data-ttu-id="bb31d-117">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="bb31d-117">-IkeEncryption</span></span>
<span data-ttu-id="bb31d-118">Algoritmo di crittografia IKE VpnClient (fase 2 IKE)</span><span class="sxs-lookup"><span data-stu-id="bb31d-118">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="bb31d-119">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="bb31d-119">-IkeIntegrity</span></span>
<span data-ttu-id="bb31d-120">Algoritmo di integrità IKE di VpnClient (fase 2 IKE)</span><span class="sxs-lookup"><span data-stu-id="bb31d-120">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="bb31d-121">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="bb31d-121">-IpsecEncryption</span></span>
<span data-ttu-id="bb31d-122">Algoritmo di crittografia IPSec VpnClient (fase 1 IKE)</span><span class="sxs-lookup"><span data-stu-id="bb31d-122">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="bb31d-123">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="bb31d-123">-IpsecIntegrity</span></span>
<span data-ttu-id="bb31d-124">Algoritmo di integrità IPSec di VpnClient (fase 1 IKE)</span><span class="sxs-lookup"><span data-stu-id="bb31d-124">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="bb31d-125">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="bb31d-125">-PfsGroup</span></span>
<span data-ttu-id="bb31d-126">Gruppi PFS VpnClient usati nella fase 2 IKE per New Child SA</span><span class="sxs-lookup"><span data-stu-id="bb31d-126">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="bb31d-127">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="bb31d-127">-SADataSize</span></span>
<span data-ttu-id="bb31d-128">Associazione di sicurezza IPSec VpnClient (denominata anche modalità rapida o fase 2 SA) dimensione del payload in KB</span><span class="sxs-lookup"><span data-stu-id="bb31d-128">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="bb31d-129">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="bb31d-129">-SALifeTime</span></span>
<span data-ttu-id="bb31d-130">Associazione di sicurezza IPSec VpnClient (chiamata anche modalità rapida o fase 2 SA) durata in secondi</span><span class="sxs-lookup"><span data-stu-id="bb31d-130">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="bb31d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb31d-131">CommonParameters</span></span>
<span data-ttu-id="bb31d-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb31d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb31d-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb31d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb31d-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bb31d-134">INPUTS</span></span>

### <span data-ttu-id="bb31d-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bb31d-135">None</span></span>

## <span data-ttu-id="bb31d-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb31d-136">OUTPUTS</span></span>

### <span data-ttu-id="bb31d-137">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="bb31d-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="bb31d-138">Note</span><span class="sxs-lookup"><span data-stu-id="bb31d-138">NOTES</span></span>

## <span data-ttu-id="bb31d-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb31d-139">RELATED LINKS</span></span>

[<span data-ttu-id="bb31d-140">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="bb31d-140">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="bb31d-141">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="bb31d-141">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="bb31d-142">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="bb31d-142">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
