---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: 9f4ceb2ac0bc84198e7fcfb71114c12e48a5616e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189374"
---
# <span data-ttu-id="e2e56-101">Set-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="e2e56-101">Set-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="e2e56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2e56-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e56-103">Imposta o aggiorna le informazioni di connessione di Exchange.</span><span class="sxs-lookup"><span data-stu-id="e2e56-103">Sets or updates the Exchange Connection information.</span></span> 

## <span data-ttu-id="e2e56-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2e56-104">SYNTAX</span></span>

### <span data-ttu-id="e2e56-105">IPv4Address (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e2e56-105">IPv4Address (Default)</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2e56-106">IPv6Address</span><span class="sxs-lookup"><span data-stu-id="e2e56-106">IPv6Address</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2e56-107">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="e2e56-107">Md5Authentication</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2e56-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e2e56-108">DESCRIPTION</span></span>
<span data-ttu-id="e2e56-109">Usata in combinazione con Update-Az Queste operazioni sono in memoria e vengono mantenute solo con `Update-AzPeering` .</span><span class="sxs-lookup"><span data-stu-id="e2e56-109">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="e2e56-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2e56-110">EXAMPLES</span></span>

### <span data-ttu-id="e2e56-111">Aggiornare l'hash Md5</span><span class="sxs-lookup"><span data-stu-id="e2e56-111">Update Md5 Hash</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -MD5AuthenticationKey $hash
```

<span data-ttu-id="e2e56-112">Aggiorna l'hash Md5 per la prima connessione nell'oggetto peering in memoria.</span><span class="sxs-lookup"><span data-stu-id="e2e56-112">Updates the Md5 Hash for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="e2e56-113">Aggiornare l'indirizzo della sessione Bgp</span><span class="sxs-lookup"><span data-stu-id="e2e56-113">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="e2e56-114">Aggiorna l'indirizzo di peering per la prima connessione nell'oggetto peering in memoria.</span><span class="sxs-lookup"><span data-stu-id="e2e56-114">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

## <span data-ttu-id="e2e56-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2e56-115">PARAMETERS</span></span>

### <span data-ttu-id="e2e56-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2e56-116">-DefaultProfile</span></span>
<span data-ttu-id="e2e56-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e2e56-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2e56-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2e56-118">-InputObject</span></span>
<span data-ttu-id="e2e56-119">Oggetto connessione Exchange</span><span class="sxs-lookup"><span data-stu-id="e2e56-119">The exchange connection object</span></span>

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

### <span data-ttu-id="e2e56-120">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="e2e56-120">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="e2e56-121">Il numero massimo di IPv4 annunciati</span><span class="sxs-lookup"><span data-stu-id="e2e56-121">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="e2e56-122">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="e2e56-122">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="e2e56-123">Il numero massimo di IPv6 annunciati</span><span class="sxs-lookup"><span data-stu-id="e2e56-123">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="e2e56-124">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="e2e56-124">-MD5AuthenticationKey</span></span>
<span data-ttu-id="e2e56-125">Chiave di autenticazione MD5 per la sessione.</span><span class="sxs-lookup"><span data-stu-id="e2e56-125">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="e2e56-126">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="e2e56-126">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="e2e56-127">Indirizzo IPv4 della sessione peer</span><span class="sxs-lookup"><span data-stu-id="e2e56-127">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="e2e56-128">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="e2e56-128">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="e2e56-129">Indirizzo IPv6 della sessione peer</span><span class="sxs-lookup"><span data-stu-id="e2e56-129">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="e2e56-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e56-130">CommonParameters</span></span>
<span data-ttu-id="e2e56-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2e56-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e56-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e2e56-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e56-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="e2e56-133">INPUTS</span></span>

### <span data-ttu-id="e2e56-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="e2e56-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="e2e56-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2e56-135">OUTPUTS</span></span>

### <span data-ttu-id="e2e56-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="e2e56-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="e2e56-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="e2e56-137">NOTES</span></span>

## <span data-ttu-id="e2e56-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2e56-138">RELATED LINKS</span></span>
