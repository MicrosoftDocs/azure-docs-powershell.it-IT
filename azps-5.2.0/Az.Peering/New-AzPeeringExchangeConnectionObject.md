---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: d3522a2916944c3ab14535a3b7957babd5f4a6ab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324066"
---
# <span data-ttu-id="4d820-101">New-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="4d820-101">New-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="4d820-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d820-102">SYNOPSIS</span></span>
<span data-ttu-id="4d820-103">Crea un PSObject in memoria da usare per creare o modificare un peering.</span><span class="sxs-lookup"><span data-stu-id="4d820-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="4d820-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d820-104">SYNTAX</span></span>

### <span data-ttu-id="4d820-105">Indirizzoipv4 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4d820-105">IPv4Address (Default)</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d820-106">Indirizzoipv6</span><span class="sxs-lookup"><span data-stu-id="4d820-106">IPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d820-107">IPv4AddressIPv6Address</span><span class="sxs-lookup"><span data-stu-id="4d820-107">IPv4AddressIPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 -PeerSessionIPv6Address <String> [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>]
 [-MD5AuthenticationKey <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d820-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d820-108">DESCRIPTION</span></span>
<span data-ttu-id="4d820-109">Crea un PSObject in memoria</span><span class="sxs-lookup"><span data-stu-id="4d820-109">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="4d820-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d820-110">EXAMPLES</span></span>

### <span data-ttu-id="4d820-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4d820-111">Example 1</span></span>
```powershell
PS C:> $exconnection = New-AzPeeringExchangeConnectionObject -PeeringDBFacilityId 99999 -PeerSessionIPv4Address 10.3.151.99 -MaxPrefixesAdvertisedIPv4 20000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId     : 99999
PeerSessionIPv4Address  : 10.3.151.99
MaxPrefixesAdvertisedV4 : 20000
Md5AuthenticationKey    : 25234523452123411fd234qdwfas3234
```

<span data-ttu-id="4d820-112">Oggetto connessione locale</span><span class="sxs-lookup"><span data-stu-id="4d820-112">Local connection object</span></span>

## <span data-ttu-id="4d820-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d820-113">PARAMETERS</span></span>

### <span data-ttu-id="4d820-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d820-114">-DefaultProfile</span></span>
<span data-ttu-id="4d820-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d820-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d820-116">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="4d820-116">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="4d820-117">Il numero massimo di IPv4 pubblicizzato</span><span class="sxs-lookup"><span data-stu-id="4d820-117">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="4d820-118">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="4d820-118">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="4d820-119">Il numero massimo di IPv6 pubblicizzato</span><span class="sxs-lookup"><span data-stu-id="4d820-119">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="4d820-120">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="4d820-120">-MD5AuthenticationKey</span></span>
<span data-ttu-id="4d820-121">Chiave di autenticazione MD5 per Session.</span><span class="sxs-lookup"><span data-stu-id="4d820-121">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="4d820-122">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="4d820-122">-PeeringDBFacilityId</span></span>
<span data-ttu-id="4d820-123">ID struttura peering disponibile in https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="4d820-123">The peering facility Id found on https://peeringdb.com</span></span>

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

### <span data-ttu-id="4d820-124">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="4d820-124">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="4d820-125">Indirizzo IPv4 della sessione peer</span><span class="sxs-lookup"><span data-stu-id="4d820-125">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="4d820-126">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="4d820-126">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="4d820-127">Indirizzo IPv6 della sessione peer</span><span class="sxs-lookup"><span data-stu-id="4d820-127">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="4d820-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d820-128">CommonParameters</span></span>
<span data-ttu-id="4d820-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d820-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d820-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d820-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d820-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d820-131">INPUTS</span></span>

### <span data-ttu-id="4d820-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4d820-132">None</span></span>

## <span data-ttu-id="4d820-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d820-133">OUTPUTS</span></span>

### <span data-ttu-id="4d820-134">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="4d820-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="4d820-135">Note</span><span class="sxs-lookup"><span data-stu-id="4d820-135">NOTES</span></span>

## <span data-ttu-id="4d820-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d820-136">RELATED LINKS</span></span>
