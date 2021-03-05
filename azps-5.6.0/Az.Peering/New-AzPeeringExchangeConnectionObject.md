---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: c4e57d3d7945f4ae06fc2461e660945bf7edfd6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989363"
---
# <span data-ttu-id="b4b1a-101">New-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="b4b1a-101">New-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="b4b1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4b1a-102">SYNOPSIS</span></span>
<span data-ttu-id="b4b1a-103">Crea un OGGETTO PSObject in memoria da usare per la creazione o la modifica di un peering.</span><span class="sxs-lookup"><span data-stu-id="b4b1a-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="b4b1a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4b1a-104">SYNTAX</span></span>

### <span data-ttu-id="b4b1a-105">IPv4Address (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b4b1a-105">IPv4Address (Default)</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4b1a-106">IPv6Address</span><span class="sxs-lookup"><span data-stu-id="b4b1a-106">IPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4b1a-107">IPv4AddressIPv6Address</span><span class="sxs-lookup"><span data-stu-id="b4b1a-107">IPv4AddressIPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 -PeerSessionIPv6Address <String> [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>]
 [-MD5AuthenticationKey <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4b1a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b4b1a-108">DESCRIPTION</span></span>
<span data-ttu-id="b4b1a-109">Crea un oggetto PSObject in memoria</span><span class="sxs-lookup"><span data-stu-id="b4b1a-109">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="b4b1a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4b1a-110">EXAMPLES</span></span>

### <span data-ttu-id="b4b1a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b4b1a-111">Example 1</span></span>
```powershell
PS C:> $exconnection = New-AzPeeringExchangeConnectionObject -PeeringDBFacilityId 99999 -PeerSessionIPv4Address 10.3.151.99 -MaxPrefixesAdvertisedIPv4 20000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId     : 99999
PeerSessionIPv4Address  : 10.3.151.99
MaxPrefixesAdvertisedV4 : 20000
Md5AuthenticationKey    : 25234523452123411fd234qdwfas3234
```

<span data-ttu-id="b4b1a-112">Oggetto connessione locale</span><span class="sxs-lookup"><span data-stu-id="b4b1a-112">Local connection object</span></span>

## <span data-ttu-id="b4b1a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4b1a-113">PARAMETERS</span></span>

### <span data-ttu-id="b4b1a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4b1a-114">-DefaultProfile</span></span>
<span data-ttu-id="b4b1a-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b4b1a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4b1a-116">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="b4b1a-116">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="b4b1a-117">Il numero massimo di IPv4 annunciati</span><span class="sxs-lookup"><span data-stu-id="b4b1a-117">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="b4b1a-118">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="b4b1a-118">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="b4b1a-119">Il numero massimo di IPv6 annunciati</span><span class="sxs-lookup"><span data-stu-id="b4b1a-119">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="b4b1a-120">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="b4b1a-120">-MD5AuthenticationKey</span></span>
<span data-ttu-id="b4b1a-121">Chiave di autenticazione MD5 per la sessione.</span><span class="sxs-lookup"><span data-stu-id="b4b1a-121">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="b4b1a-122">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="b4b1a-122">-PeeringDBFacilityId</span></span>
<span data-ttu-id="b4b1a-123">ID della struttura di peering trovato in https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="b4b1a-123">The peering facility Id found on https://peeringdb.com</span></span>

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

### <span data-ttu-id="b4b1a-124">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="b4b1a-124">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="b4b1a-125">Indirizzo IPv4 della sessione peer</span><span class="sxs-lookup"><span data-stu-id="b4b1a-125">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="b4b1a-126">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="b4b1a-126">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="b4b1a-127">Indirizzo IPv6 della sessione peer</span><span class="sxs-lookup"><span data-stu-id="b4b1a-127">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="b4b1a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4b1a-128">CommonParameters</span></span>
<span data-ttu-id="b4b1a-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4b1a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4b1a-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b4b1a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4b1a-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="b4b1a-131">INPUTS</span></span>

### <span data-ttu-id="b4b1a-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b4b1a-132">None</span></span>

## <span data-ttu-id="b4b1a-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4b1a-133">OUTPUTS</span></span>

### <span data-ttu-id="b4b1a-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="b4b1a-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="b4b1a-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="b4b1a-135">NOTES</span></span>

## <span data-ttu-id="b4b1a-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4b1a-136">RELATED LINKS</span></span>
