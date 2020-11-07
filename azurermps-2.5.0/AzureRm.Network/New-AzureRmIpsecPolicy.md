---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermipsecpolicy
schema: 2.0.0
ms.openlocfilehash: 642284e7e1aa732983ee660ea323707be030b640
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866252"
---
# <span data-ttu-id="2ed27-101">New-AzureRmIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="2ed27-101">New-AzureRmIpsecPolicy</span></span>

## <span data-ttu-id="2ed27-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2ed27-102">SYNOPSIS</span></span>
<span data-ttu-id="2ed27-103">Crea un criterio IPSec.</span><span class="sxs-lookup"><span data-stu-id="2ed27-103">Creates an IPSec Policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ed27-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ed27-104">SYNTAX</span></span>

```
New-AzureRmIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ed27-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ed27-105">DESCRIPTION</span></span>
<span data-ttu-id="2ed27-106">Il cmdlet New-AzureRmIpsecPolicy crea una proposta di criteri IPSec da usare in una connessione di gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="2ed27-106">The New-AzureRmIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="2ed27-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ed27-107">EXAMPLES</span></span>

### <span data-ttu-id="2ed27-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2ed27-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzureRmIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="2ed27-109">Creazione di un criterio IPSec da usare per una nuova connessione di gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="2ed27-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="2ed27-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2ed27-110">PARAMETERS</span></span>

### <span data-ttu-id="2ed27-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ed27-111">-DefaultProfile</span></span>
<span data-ttu-id="2ed27-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2ed27-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed27-113">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="2ed27-113">-DhGroup</span></span>
<span data-ttu-id="2ed27-114">Gruppi DH usati nella fase 1 IKE per la SA iniziale</span><span class="sxs-lookup"><span data-stu-id="2ed27-114">The DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, DHGroup1, DHGroup14, DHGroup2, DHGroup2048, DHGroup24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed27-115">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="2ed27-115">-IkeEncryption</span></span>
<span data-ttu-id="2ed27-116">Algoritmo di crittografia IKE (IKE-fase 2)</span><span class="sxs-lookup"><span data-stu-id="2ed27-116">The IKE encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: DES, DES3, AES128, AES192, AES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed27-117">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="2ed27-117">-IkeIntegrity</span></span>
<span data-ttu-id="2ed27-118">Algoritmo di integrità IKE (fase 2 IKE)</span><span class="sxs-lookup"><span data-stu-id="2ed27-118">The IKE integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: MD5, SHA1, SHA256, SHA384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed27-119">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="2ed27-119">-IpsecEncryption</span></span>
<span data-ttu-id="2ed27-120">Algoritmo di crittografia IPSec (fase 1 IKE)</span><span class="sxs-lookup"><span data-stu-id="2ed27-120">The IPSec encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, DES, DES3, AES128, AES192, AES256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed27-121">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="2ed27-121">-IpsecIntegrity</span></span>
<span data-ttu-id="2ed27-122">Algoritmo di integrità IPSec (fase 1 IKE)</span><span class="sxs-lookup"><span data-stu-id="2ed27-122">The IPSec integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: MD5, SHA1, SHA256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed27-123">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="2ed27-123">-PfsGroup</span></span>
<span data-ttu-id="2ed27-124">Gruppi DH usati nella fase 2 IKE per New Child SA</span><span class="sxs-lookup"><span data-stu-id="2ed27-124">The DH Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, PFS1, PFS2, PFS2048, PFS24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed27-125">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="2ed27-125">-SADataSizeKilobytes</span></span>
<span data-ttu-id="2ed27-126">Associazione di sicurezza IPSec (chiamata anche modalità rapida o fase 2 SA) in KB</span><span class="sxs-lookup"><span data-stu-id="2ed27-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed27-127">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="2ed27-127">-SALifeTimeSeconds</span></span>
<span data-ttu-id="2ed27-128">Associazione di sicurezza IPSec (chiamata anche modalità rapida o fase 2 SA) durata in secondi</span><span class="sxs-lookup"><span data-stu-id="2ed27-128">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed27-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ed27-129">CommonParameters</span></span>
<span data-ttu-id="2ed27-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ed27-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ed27-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ed27-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ed27-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2ed27-132">INPUTS</span></span>

### <span data-ttu-id="2ed27-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2ed27-133">None</span></span>

## <span data-ttu-id="2ed27-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ed27-134">OUTPUTS</span></span>

### <span data-ttu-id="2ed27-135">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="2ed27-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="2ed27-136">Note</span><span class="sxs-lookup"><span data-stu-id="2ed27-136">NOTES</span></span>

## <span data-ttu-id="2ed27-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ed27-137">RELATED LINKS</span></span>

