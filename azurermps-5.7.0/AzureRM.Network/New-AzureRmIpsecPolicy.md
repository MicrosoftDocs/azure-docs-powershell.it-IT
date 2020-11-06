---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmIpsecPolicy.md
ms.openlocfilehash: b5a5b3d9844a06e75938a2b87987f5a1f71f04e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518903"
---
# <span data-ttu-id="bc97a-101">New-AzureRmIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="bc97a-101">New-AzureRmIpsecPolicy</span></span>

## <span data-ttu-id="bc97a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bc97a-102">SYNOPSIS</span></span>
<span data-ttu-id="bc97a-103">Crea un criterio IPSec.</span><span class="sxs-lookup"><span data-stu-id="bc97a-103">Creates an IPSec Policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc97a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc97a-104">SYNTAX</span></span>

```
New-AzureRmIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc97a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc97a-105">DESCRIPTION</span></span>
<span data-ttu-id="bc97a-106">Il cmdlet New-AzureRmIpsecPolicy crea una proposta di criteri IPSec da usare in una connessione di gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="bc97a-106">The New-AzureRmIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="bc97a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc97a-107">EXAMPLES</span></span>

### <span data-ttu-id="bc97a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bc97a-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzureRmIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="bc97a-109">Creazione di un criterio IPSec da usare per una nuova connessione di gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="bc97a-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="bc97a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bc97a-110">PARAMETERS</span></span>

### <span data-ttu-id="bc97a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc97a-111">-DefaultProfile</span></span>
<span data-ttu-id="bc97a-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bc97a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc97a-113">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="bc97a-113">-DhGroup</span></span>
<span data-ttu-id="bc97a-114">Gruppi DH usati nella fase 1 IKE per la SA iniziale</span><span class="sxs-lookup"><span data-stu-id="bc97a-114">The DH Groups used in IKE Phase 1 for initial SA</span></span>

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

### <span data-ttu-id="bc97a-115">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="bc97a-115">-IkeEncryption</span></span>
<span data-ttu-id="bc97a-116">Algoritmo di crittografia IKE (IKE-fase 2)</span><span class="sxs-lookup"><span data-stu-id="bc97a-116">The IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="bc97a-117">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="bc97a-117">-IkeIntegrity</span></span>
<span data-ttu-id="bc97a-118">Algoritmo di integrità IKE (fase 2 IKE)</span><span class="sxs-lookup"><span data-stu-id="bc97a-118">The IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="bc97a-119">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="bc97a-119">-IpsecEncryption</span></span>
<span data-ttu-id="bc97a-120">Algoritmo di crittografia IPSec (fase 1 IKE)</span><span class="sxs-lookup"><span data-stu-id="bc97a-120">The IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="bc97a-121">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="bc97a-121">-IpsecIntegrity</span></span>
<span data-ttu-id="bc97a-122">Algoritmo di integrità IPSec (fase 1 IKE)</span><span class="sxs-lookup"><span data-stu-id="bc97a-122">The IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="bc97a-123">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="bc97a-123">-PfsGroup</span></span>
<span data-ttu-id="bc97a-124">Gruppi DH usati nella fase 2 IKE per New Child SA</span><span class="sxs-lookup"><span data-stu-id="bc97a-124">The DH Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="bc97a-125">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="bc97a-125">-SADataSizeKilobytes</span></span>
<span data-ttu-id="bc97a-126">Associazione di sicurezza IPSec (chiamata anche modalità rapida o fase 2 SA) in KB</span><span class="sxs-lookup"><span data-stu-id="bc97a-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="bc97a-127">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="bc97a-127">-SALifeTimeSeconds</span></span>
<span data-ttu-id="bc97a-128">Associazione di sicurezza IPSec (chiamata anche modalità rapida o fase 2 SA) durata in secondi</span><span class="sxs-lookup"><span data-stu-id="bc97a-128">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="bc97a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc97a-129">CommonParameters</span></span>
<span data-ttu-id="bc97a-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc97a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc97a-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc97a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc97a-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bc97a-132">INPUTS</span></span>

### <span data-ttu-id="bc97a-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bc97a-133">None</span></span>

## <span data-ttu-id="bc97a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc97a-134">OUTPUTS</span></span>

### <span data-ttu-id="bc97a-135">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="bc97a-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="bc97a-136">Note</span><span class="sxs-lookup"><span data-stu-id="bc97a-136">NOTES</span></span>

## <span data-ttu-id="bc97a-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc97a-137">RELATED LINKS</span></span>

