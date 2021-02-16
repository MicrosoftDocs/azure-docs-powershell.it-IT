---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
ms.openlocfilehash: 5a6cbbc007c372d2e1765e4e2369d2f3d60d0a07
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179695"
---
# <span data-ttu-id="2248e-101">New-AzIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="2248e-101">New-AzIpsecPolicy</span></span>

## <span data-ttu-id="2248e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2248e-102">SYNOPSIS</span></span>
<span data-ttu-id="2248e-103">Crea un criterio IPSec.</span><span class="sxs-lookup"><span data-stu-id="2248e-103">Creates an IPSec Policy.</span></span>

## <span data-ttu-id="2248e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2248e-104">SYNTAX</span></span>

```
New-AzIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2248e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2248e-105">DESCRIPTION</span></span>
<span data-ttu-id="2248e-106">Il cmdlet New-AzIpsecPolicy crea una proposta per il criterio IPSec da usare in una connessione a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="2248e-106">The New-AzIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="2248e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2248e-107">EXAMPLES</span></span>

### <span data-ttu-id="2248e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2248e-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="2248e-109">Creazione di un criterio IPSec da usare per una nuova connessione a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="2248e-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="2248e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2248e-110">PARAMETERS</span></span>

### <span data-ttu-id="2248e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2248e-111">-DefaultProfile</span></span>
<span data-ttu-id="2248e-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2248e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2248e-113">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="2248e-113">-DhGroup</span></span>
<span data-ttu-id="2248e-114">Gruppi DH usati nella fase 1 di IKE per l'accesso condiviso iniziale</span><span class="sxs-lookup"><span data-stu-id="2248e-114">The DH Groups used in IKE Phase 1 for initial SA</span></span>

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

### <span data-ttu-id="2248e-115">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="2248e-115">-IkeEncryption</span></span>
<span data-ttu-id="2248e-116">Algoritmo di crittografia IKE (Fase 1 IKE)</span><span class="sxs-lookup"><span data-stu-id="2248e-116">The IKE encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="2248e-117">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="2248e-117">-IkeIntegrity</span></span>
<span data-ttu-id="2248e-118">Algoritmo di integrità IKE (Fase 1 IKE)</span><span class="sxs-lookup"><span data-stu-id="2248e-118">The IKE integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="2248e-119">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="2248e-119">-IpsecEncryption</span></span>
<span data-ttu-id="2248e-120">Algoritmo di crittografia IPSec (Fase IKE 2)</span><span class="sxs-lookup"><span data-stu-id="2248e-120">The IPSec encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="2248e-121">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="2248e-121">-IpsecIntegrity</span></span>
<span data-ttu-id="2248e-122">Algoritmo di integrità IPSec (Fase IKE 2)</span><span class="sxs-lookup"><span data-stu-id="2248e-122">The IPSec integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="2248e-123">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="2248e-123">-PfsGroup</span></span>
<span data-ttu-id="2248e-124">Gruppi DH usati nella fase 2 di IKE per la nuova SA figlio</span><span class="sxs-lookup"><span data-stu-id="2248e-124">The DH Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="2248e-125">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="2248e-125">-SADataSizeKilobytes</span></span>
<span data-ttu-id="2248e-126">Dimensione del payload dell'associazione di sicurezza IPSec (chiamata anche modalità rapida o sa di fase 2) in KB</span><span class="sxs-lookup"><span data-stu-id="2248e-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="2248e-127">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="2248e-127">-SALifeTimeSeconds</span></span>
<span data-ttu-id="2248e-128">Durata in secondi dell'associazione di sicurezza IPSec (chiamata anche modalità rapida o sa di fase 2)</span><span class="sxs-lookup"><span data-stu-id="2248e-128">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="2248e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2248e-129">CommonParameters</span></span>
<span data-ttu-id="2248e-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2248e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2248e-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2248e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2248e-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="2248e-132">INPUTS</span></span>

### <span data-ttu-id="2248e-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2248e-133">None</span></span>

## <span data-ttu-id="2248e-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2248e-134">OUTPUTS</span></span>

### <span data-ttu-id="2248e-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="2248e-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="2248e-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="2248e-136">NOTES</span></span>

## <span data-ttu-id="2248e-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2248e-137">RELATED LINKS</span></span>
