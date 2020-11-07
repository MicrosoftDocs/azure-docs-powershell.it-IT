---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: 89106b6474e52863514c65614d334cf5d8382f3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688387"
---
# <span data-ttu-id="13fbb-101">New-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="13fbb-101">New-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="13fbb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="13fbb-102">SYNOPSIS</span></span>
<span data-ttu-id="13fbb-103">Questo comando consente agli utenti di creare l'oggetto parametri IPSec VPN specificando uno o tutti i valori, ad esempio IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup, per impostare il gateway VPN esistente.</span><span class="sxs-lookup"><span data-stu-id="13fbb-103">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13fbb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13fbb-104">SYNTAX</span></span>

```
New-AzureRmVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13fbb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13fbb-105">DESCRIPTION</span></span>
<span data-ttu-id="13fbb-106">Questo comando consente agli utenti di creare l'oggetto parametri IPSec VPN specificando uno o tutti i valori, ad esempio IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup, per impostare il gateway VPN esistente.</span><span class="sxs-lookup"><span data-stu-id="13fbb-106">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="13fbb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13fbb-107">EXAMPLES</span></span>

### <span data-ttu-id="13fbb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="13fbb-108">Example 1</span></span>
```
PS C:\> $vpnclientipsecparams1 = New-AzureRmVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

<span data-ttu-id="13fbb-109">New-AzureRmVpnClientIpsecParameter cmdlet viene usato per creare l'oggetto parametri IPSec VPN usando i valori passati di uno o tutti i parametri che l'utente può impostare per qualsiasi gateway di rete virtuale esistente in ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="13fbb-109">New-AzureRmVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="13fbb-110">Questo oggetto VpnClientIPsecParameters creato viene passato al comando Set-AzureRmVpnClientIpsecParameter per impostare i criteri personalizzati IPSec VPN specificati nel gateway di rete virtuale, come illustrato nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="13fbb-110">This created VpnClientIPsecParameters object is passed to Set-AzureRmVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="13fbb-111">Questo comando restituisce l'oggetto di VpnClientIPsecParameters che mostra i parametri impostati.</span><span class="sxs-lookup"><span data-stu-id="13fbb-111">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="13fbb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="13fbb-112">PARAMETERS</span></span>

### <span data-ttu-id="13fbb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13fbb-113">-DefaultProfile</span></span>
<span data-ttu-id="13fbb-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="13fbb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13fbb-115">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="13fbb-115">-DhGroup</span></span>
<span data-ttu-id="13fbb-116">I gruppi di vpnclient DH usati nella fase 1 IKE per la SA iniziale.</span><span class="sxs-lookup"><span data-stu-id="13fbb-116">The Vpnclient DH Groups used in IKE Phase 1 for initial SA.</span></span>

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

### <span data-ttu-id="13fbb-117">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="13fbb-117">-IkeEncryption</span></span>
<span data-ttu-id="13fbb-118">Algoritmo di crittografia IKE vpnclient (fase 2 IKE)</span><span class="sxs-lookup"><span data-stu-id="13fbb-118">The Vpnclient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="13fbb-119">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="13fbb-119">-IkeIntegrity</span></span>
<span data-ttu-id="13fbb-120">Algoritmo di integrità IKE di vpnclient (fase 2 IKE)</span><span class="sxs-lookup"><span data-stu-id="13fbb-120">The Vpnclient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="13fbb-121">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="13fbb-121">-IpsecEncryption</span></span>
<span data-ttu-id="13fbb-122">Algoritmo di crittografia IPSec vpnclient (fase 1 IKE)</span><span class="sxs-lookup"><span data-stu-id="13fbb-122">The Vpnclient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="13fbb-123">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="13fbb-123">-IpsecIntegrity</span></span>
<span data-ttu-id="13fbb-124">Algoritmo di integrità IPSec di vpnclient (fase 1 IKE)</span><span class="sxs-lookup"><span data-stu-id="13fbb-124">The Vpnclient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="13fbb-125">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="13fbb-125">-PfsGroup</span></span>
<span data-ttu-id="13fbb-126">Gruppi PFS vpnclient usati nella fase 2 IKE per New Child SA</span><span class="sxs-lookup"><span data-stu-id="13fbb-126">The Vpnclient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="13fbb-127">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="13fbb-127">-SADataSize</span></span>
<span data-ttu-id="13fbb-128">Associazione di sicurezza IPSec vpnclient (denominata anche modalità rapida o fase 2 SA) dimensione del payload in KB</span><span class="sxs-lookup"><span data-stu-id="13fbb-128">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="13fbb-129">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="13fbb-129">-SALifeTime</span></span>
<span data-ttu-id="13fbb-130">Associazione di sicurezza IPSec vpnclient (chiamata anche modalità rapida o fase 2 SA) durata in secondi</span><span class="sxs-lookup"><span data-stu-id="13fbb-130">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="13fbb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13fbb-131">CommonParameters</span></span>
<span data-ttu-id="13fbb-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13fbb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13fbb-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13fbb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13fbb-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="13fbb-134">INPUTS</span></span>

### <span data-ttu-id="13fbb-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="13fbb-135">None</span></span>

## <span data-ttu-id="13fbb-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13fbb-136">OUTPUTS</span></span>

### <span data-ttu-id="13fbb-137">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="13fbb-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="13fbb-138">Note</span><span class="sxs-lookup"><span data-stu-id="13fbb-138">NOTES</span></span>

## <span data-ttu-id="13fbb-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13fbb-139">RELATED LINKS</span></span>
