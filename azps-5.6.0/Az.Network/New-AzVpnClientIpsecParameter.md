---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 3b34fb1de6b661a622690f93808eaf0660da461b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995327"
---
# <span data-ttu-id="1896c-101">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="1896c-101">New-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="1896c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1896c-102">SYNOPSIS</span></span>
<span data-ttu-id="1896c-103">Questo comando consente agli utenti di creare l'oggetto parametri IPSec Vpn specificando uno o tutti i valori come IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup da impostare nel gateway VPN esistente.</span><span class="sxs-lookup"><span data-stu-id="1896c-103">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="1896c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1896c-104">SYNTAX</span></span>

```
New-AzVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1896c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1896c-105">DESCRIPTION</span></span>
<span data-ttu-id="1896c-106">Questo comando consente agli utenti di creare l'oggetto parametri IPSec Vpn specificando uno o tutti i valori come IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup da impostare nel gateway VPN esistente.</span><span class="sxs-lookup"><span data-stu-id="1896c-106">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="1896c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1896c-107">EXAMPLES</span></span>

### <span data-ttu-id="1896c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1896c-108">Example 1</span></span>
```
PS C:\> $vpnclientipsecparams1 = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

<span data-ttu-id="1896c-109">New-AzVpnClientIpsecParameter cmdlet viene usato per creare l'oggetto parametri ipsec vpn dell'uso dei valori passati di uno o di tutti i parametri che l'utente può impostare per qualsiasi gateway di rete virtuale esistente in ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1896c-109">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="1896c-110">Questo oggetto VpnClientIPsecParameters creato viene passato Set-AzVpnClientIpsecParameter un comando per impostare il criterio personalizzato VPN ipsec specificato nel gateway di rete virtuale, come illustrato nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="1896c-110">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="1896c-111">Questo comando restituisce l'oggetto vpnClientIPsecParameters che mostra i parametri impostati.</span><span class="sxs-lookup"><span data-stu-id="1896c-111">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="1896c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1896c-112">PARAMETERS</span></span>

### <span data-ttu-id="1896c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1896c-113">-DefaultProfile</span></span>
<span data-ttu-id="1896c-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1896c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1896c-115">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="1896c-115">-DhGroup</span></span>
<span data-ttu-id="1896c-116">Gruppi VpnClient DH usati nella fase 1 di IKE per l'accesso condiviso iniziale.</span><span class="sxs-lookup"><span data-stu-id="1896c-116">The VpnClient DH Groups used in IKE Phase 1 for initial SA.</span></span>

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

### <span data-ttu-id="1896c-117">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="1896c-117">-IkeEncryption</span></span>
<span data-ttu-id="1896c-118">Algoritmo di crittografia IKE Per VpnClient (Fase IKE 2)</span><span class="sxs-lookup"><span data-stu-id="1896c-118">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="1896c-119">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="1896c-119">-IkeIntegrity</span></span>
<span data-ttu-id="1896c-120">Algoritmo di integrità IKE di VpnClient (Fase IKE 2)</span><span class="sxs-lookup"><span data-stu-id="1896c-120">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="1896c-121">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="1896c-121">-IpsecEncryption</span></span>
<span data-ttu-id="1896c-122">Algoritmo di crittografia IPSec VpnClient (Fase IKE 1)</span><span class="sxs-lookup"><span data-stu-id="1896c-122">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="1896c-123">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="1896c-123">-IpsecIntegrity</span></span>
<span data-ttu-id="1896c-124">Algoritmo di integrità IPSec di VpnClient (Fase IKE 1)</span><span class="sxs-lookup"><span data-stu-id="1896c-124">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="1896c-125">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="1896c-125">-PfsGroup</span></span>
<span data-ttu-id="1896c-126">Gruppi PFS VpnClient usati nella fase 2 di IKE per la nuova sa figlio</span><span class="sxs-lookup"><span data-stu-id="1896c-126">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="1896c-127">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="1896c-127">-SADataSize</span></span>
<span data-ttu-id="1896c-128">Dimensioni del payload della modalità rapida o sa della fase 2 in KB per l'associazione di sicurezza IPSec vpn</span><span class="sxs-lookup"><span data-stu-id="1896c-128">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="1896c-129">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="1896c-129">-SALifeTime</span></span>
<span data-ttu-id="1896c-130">Durata in secondi dell'associazione di sicurezza IPSec di VpnClient (chiamata anche modalità rapida o SA di fase 2)</span><span class="sxs-lookup"><span data-stu-id="1896c-130">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="1896c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1896c-131">CommonParameters</span></span>
<span data-ttu-id="1896c-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1896c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1896c-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1896c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1896c-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="1896c-134">INPUTS</span></span>

### <span data-ttu-id="1896c-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1896c-135">None</span></span>

## <span data-ttu-id="1896c-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1896c-136">OUTPUTS</span></span>

### <span data-ttu-id="1896c-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="1896c-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="1896c-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="1896c-138">NOTES</span></span>

## <span data-ttu-id="1896c-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1896c-139">RELATED LINKS</span></span>

[<span data-ttu-id="1896c-140">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="1896c-140">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="1896c-141">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="1896c-141">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="1896c-142">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="1896c-142">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
