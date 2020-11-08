---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: 9f4ceb2ac0bc84198e7fcfb71114c12e48a5616e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032862"
---
# <span data-ttu-id="76fd4-101">Set-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="76fd4-101">Set-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="76fd4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="76fd4-102">SYNOPSIS</span></span>
<span data-ttu-id="76fd4-103">Imposta o aggiorna le informazioni sulla connessione di Exchange.</span><span class="sxs-lookup"><span data-stu-id="76fd4-103">Sets or updates the Exchange Connection information.</span></span> 

## <span data-ttu-id="76fd4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76fd4-104">SYNTAX</span></span>

### <span data-ttu-id="76fd4-105">Indirizzoipv4 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="76fd4-105">IPv4Address (Default)</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76fd4-106">Indirizzoipv6</span><span class="sxs-lookup"><span data-stu-id="76fd4-106">IPv6Address</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76fd4-107">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="76fd4-107">Md5Authentication</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76fd4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76fd4-108">DESCRIPTION</span></span>
<span data-ttu-id="76fd4-109">Usato in combinazione con Update-AzPeering, si tratta di un'operazione in memoria che verrà mantenuta solo con `Update-AzPeering` .</span><span class="sxs-lookup"><span data-stu-id="76fd4-109">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="76fd4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76fd4-110">EXAMPLES</span></span>

### <span data-ttu-id="76fd4-111">Aggiornare l'hash MD5</span><span class="sxs-lookup"><span data-stu-id="76fd4-111">Update Md5 Hash</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -MD5AuthenticationKey $hash
```

<span data-ttu-id="76fd4-112">Aggiorna l'hash MD5 per la prima connessione nell'oggetto peering in memoria.</span><span class="sxs-lookup"><span data-stu-id="76fd4-112">Updates the Md5 Hash for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="76fd4-113">Aggiornare l'indirizzo della sessione BGP</span><span class="sxs-lookup"><span data-stu-id="76fd4-113">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="76fd4-114">Aggiorna l'indirizzo di peering per la prima connessione nell'oggetto peering in memoria.</span><span class="sxs-lookup"><span data-stu-id="76fd4-114">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

## <span data-ttu-id="76fd4-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="76fd4-115">PARAMETERS</span></span>

### <span data-ttu-id="76fd4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76fd4-116">-DefaultProfile</span></span>
<span data-ttu-id="76fd4-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="76fd4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76fd4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76fd4-118">-InputObject</span></span>
<span data-ttu-id="76fd4-119">Oggetto connessione di Exchange</span><span class="sxs-lookup"><span data-stu-id="76fd4-119">The exchange connection object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76fd4-120">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="76fd4-120">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="76fd4-121">Il numero massimo di IPv4 pubblicizzato</span><span class="sxs-lookup"><span data-stu-id="76fd4-121">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fd4-122">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="76fd4-122">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="76fd4-123">Il numero massimo di IPv6 pubblicizzato</span><span class="sxs-lookup"><span data-stu-id="76fd4-123">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fd4-124">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="76fd4-124">-MD5AuthenticationKey</span></span>
<span data-ttu-id="76fd4-125">Chiave di autenticazione MD5 per Session.</span><span class="sxs-lookup"><span data-stu-id="76fd4-125">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: Md5Authentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fd4-126">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="76fd4-126">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="76fd4-127">Indirizzo IPv4 della sessione peer</span><span class="sxs-lookup"><span data-stu-id="76fd4-127">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fd4-128">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="76fd4-128">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="76fd4-129">Indirizzo IPv6 della sessione peer</span><span class="sxs-lookup"><span data-stu-id="76fd4-129">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fd4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76fd4-130">CommonParameters</span></span>
<span data-ttu-id="76fd4-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76fd4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76fd4-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76fd4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76fd4-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="76fd4-133">INPUTS</span></span>

### <span data-ttu-id="76fd4-134">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="76fd4-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="76fd4-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76fd4-135">OUTPUTS</span></span>

### <span data-ttu-id="76fd4-136">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="76fd4-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="76fd4-137">Note</span><span class="sxs-lookup"><span data-stu-id="76fd4-137">NOTES</span></span>

## <span data-ttu-id="76fd4-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76fd4-138">RELATED LINKS</span></span>
