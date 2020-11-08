---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: d3522a2916944c3ab14535a3b7957babd5f4a6ab
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022432"
---
# <span data-ttu-id="353fd-101">New-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="353fd-101">New-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="353fd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="353fd-102">SYNOPSIS</span></span>
<span data-ttu-id="353fd-103">Crea un PSObject in memoria da usare per creare o modificare un peering.</span><span class="sxs-lookup"><span data-stu-id="353fd-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="353fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="353fd-104">SYNTAX</span></span>

### <span data-ttu-id="353fd-105">Indirizzoipv4 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="353fd-105">IPv4Address (Default)</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="353fd-106">Indirizzoipv6</span><span class="sxs-lookup"><span data-stu-id="353fd-106">IPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="353fd-107">IPv4AddressIPv6Address</span><span class="sxs-lookup"><span data-stu-id="353fd-107">IPv4AddressIPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 -PeerSessionIPv6Address <String> [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>]
 [-MD5AuthenticationKey <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="353fd-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="353fd-108">DESCRIPTION</span></span>
<span data-ttu-id="353fd-109">Crea un PSObject in memoria</span><span class="sxs-lookup"><span data-stu-id="353fd-109">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="353fd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="353fd-110">EXAMPLES</span></span>

### <span data-ttu-id="353fd-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="353fd-111">Example 1</span></span>
```powershell
PS C:> $exconnection = New-AzPeeringExchangeConnectionObject -PeeringDBFacilityId 99999 -PeerSessionIPv4Address 10.3.151.99 -MaxPrefixesAdvertisedIPv4 20000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId     : 99999
PeerSessionIPv4Address  : 10.3.151.99
MaxPrefixesAdvertisedV4 : 20000
Md5AuthenticationKey    : 25234523452123411fd234qdwfas3234
```

<span data-ttu-id="353fd-112">Oggetto connessione locale</span><span class="sxs-lookup"><span data-stu-id="353fd-112">Local connection object</span></span>

## <span data-ttu-id="353fd-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="353fd-113">PARAMETERS</span></span>

### <span data-ttu-id="353fd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="353fd-114">-DefaultProfile</span></span>
<span data-ttu-id="353fd-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="353fd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="353fd-116">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="353fd-116">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="353fd-117">Il numero massimo di IPv4 pubblicizzato</span><span class="sxs-lookup"><span data-stu-id="353fd-117">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Address, IPv4AddressIPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353fd-118">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="353fd-118">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="353fd-119">Il numero massimo di IPv6 pubblicizzato</span><span class="sxs-lookup"><span data-stu-id="353fd-119">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Address, IPv4AddressIPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353fd-120">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="353fd-120">-MD5AuthenticationKey</span></span>
<span data-ttu-id="353fd-121">Chiave di autenticazione MD5 per Session.</span><span class="sxs-lookup"><span data-stu-id="353fd-121">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353fd-122">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="353fd-122">-PeeringDBFacilityId</span></span>
<span data-ttu-id="353fd-123">ID struttura peering disponibile in https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="353fd-123">The peering facility Id found on https://peeringdb.com</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353fd-124">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="353fd-124">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="353fd-125">Indirizzo IPv4 della sessione peer</span><span class="sxs-lookup"><span data-stu-id="353fd-125">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Address, IPv4AddressIPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353fd-126">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="353fd-126">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="353fd-127">Indirizzo IPv6 della sessione peer</span><span class="sxs-lookup"><span data-stu-id="353fd-127">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Address, IPv4AddressIPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353fd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="353fd-128">CommonParameters</span></span>
<span data-ttu-id="353fd-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="353fd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="353fd-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="353fd-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="353fd-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="353fd-131">INPUTS</span></span>

### <span data-ttu-id="353fd-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="353fd-132">None</span></span>

## <span data-ttu-id="353fd-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="353fd-133">OUTPUTS</span></span>

### <span data-ttu-id="353fd-134">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="353fd-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="353fd-135">Note</span><span class="sxs-lookup"><span data-stu-id="353fd-135">NOTES</span></span>

## <span data-ttu-id="353fd-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="353fd-136">RELATED LINKS</span></span>
