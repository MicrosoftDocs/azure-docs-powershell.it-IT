---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
ms.openlocfilehash: 5a6cbbc007c372d2e1765e4e2369d2f3d60d0a07
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336583"
---
# <span data-ttu-id="802e7-101">New-AzIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="802e7-101">New-AzIpsecPolicy</span></span>

## <span data-ttu-id="802e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="802e7-102">SYNOPSIS</span></span>
<span data-ttu-id="802e7-103">Crea un criterio IPSec.</span><span class="sxs-lookup"><span data-stu-id="802e7-103">Creates an IPSec Policy.</span></span>

## <span data-ttu-id="802e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="802e7-104">SYNTAX</span></span>

```
New-AzIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="802e7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="802e7-105">DESCRIPTION</span></span>
<span data-ttu-id="802e7-106">Il cmdlet New-AzIpsecPolicy crea una proposta di criteri IPSec da usare in una connessione di gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="802e7-106">The New-AzIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="802e7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="802e7-107">EXAMPLES</span></span>

### <span data-ttu-id="802e7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="802e7-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="802e7-109">Creazione di un criterio IPSec da usare per una nuova connessione di gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="802e7-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="802e7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="802e7-110">PARAMETERS</span></span>

### <span data-ttu-id="802e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="802e7-111">-DefaultProfile</span></span>
<span data-ttu-id="802e7-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="802e7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="802e7-113">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="802e7-113">-DhGroup</span></span>
<span data-ttu-id="802e7-114">Gruppi DH usati nella fase 1 IKE per la SA iniziale</span><span class="sxs-lookup"><span data-stu-id="802e7-114">The DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, DHGroup1, DHGroup14, DHGroup2, DHGroup2048, DHGroup24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802e7-115">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="802e7-115">-IkeEncryption</span></span>
<span data-ttu-id="802e7-116">Algoritmo di crittografia IKE (fase 1 IKE)</span><span class="sxs-lookup"><span data-stu-id="802e7-116">The IKE encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DES, DES3, AES128, AES192, AES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802e7-117">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="802e7-117">-IkeIntegrity</span></span>
<span data-ttu-id="802e7-118">Algoritmo di integrità IKE (fase 1 IKE)</span><span class="sxs-lookup"><span data-stu-id="802e7-118">The IKE integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MD5, SHA1, SHA256, SHA384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802e7-119">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="802e7-119">-IpsecEncryption</span></span>
<span data-ttu-id="802e7-120">Algoritmo di crittografia IPSec (IKE-fase 2)</span><span class="sxs-lookup"><span data-stu-id="802e7-120">The IPSec encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, DES, DES3, AES128, AES192, AES256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802e7-121">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="802e7-121">-IpsecIntegrity</span></span>
<span data-ttu-id="802e7-122">Algoritmo di integrità IPSec (fase 2 IKE)</span><span class="sxs-lookup"><span data-stu-id="802e7-122">The IPSec integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MD5, SHA1, SHA256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802e7-123">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="802e7-123">-PfsGroup</span></span>
<span data-ttu-id="802e7-124">Gruppi DH usati nella fase 2 IKE per New Child SA</span><span class="sxs-lookup"><span data-stu-id="802e7-124">The DH Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, PFS1, PFS2, PFS2048, PFS24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802e7-125">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="802e7-125">-SADataSizeKilobytes</span></span>
<span data-ttu-id="802e7-126">Associazione di sicurezza IPSec (chiamata anche modalità rapida o fase 2 SA) in KB</span><span class="sxs-lookup"><span data-stu-id="802e7-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="802e7-127">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="802e7-127">-SALifeTimeSeconds</span></span>
<span data-ttu-id="802e7-128">Associazione di sicurezza IPSec (chiamata anche modalità rapida o fase 2 SA) durata in secondi</span><span class="sxs-lookup"><span data-stu-id="802e7-128">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="802e7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="802e7-129">CommonParameters</span></span>
<span data-ttu-id="802e7-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="802e7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="802e7-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="802e7-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="802e7-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="802e7-132">INPUTS</span></span>

### <span data-ttu-id="802e7-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="802e7-133">None</span></span>

## <span data-ttu-id="802e7-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="802e7-134">OUTPUTS</span></span>

### <span data-ttu-id="802e7-135">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="802e7-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="802e7-136">Note</span><span class="sxs-lookup"><span data-stu-id="802e7-136">NOTES</span></span>

## <span data-ttu-id="802e7-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="802e7-137">RELATED LINKS</span></span>
