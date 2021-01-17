---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 0b72cd501f9e003e39fc3dd4f4e90bbd85331180
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384621"
---
# <span data-ttu-id="b7a1b-101">Set-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="b7a1b-101">Set-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="b7a1b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="b7a1b-103">Imposta o aggiorna le informazioni di connessione diretta.</span><span class="sxs-lookup"><span data-stu-id="b7a1b-103">Sets or updates the Direct Connection information.</span></span> 

## <span data-ttu-id="b7a1b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7a1b-104">SYNTAX</span></span>

### <span data-ttu-id="b7a1b-105">Larghezza di banda (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b7a1b-105">Bandwidth (Default)</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -BandwidthInMbps <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7a1b-106">IPv4Prefix</span><span class="sxs-lookup"><span data-stu-id="b7a1b-106">IPv4Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV4 <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7a1b-107">IPv6Prefix</span><span class="sxs-lookup"><span data-stu-id="b7a1b-107">IPv6Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV6 <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7a1b-108">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="b7a1b-108">Md5Authentication</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7a1b-109">ParameterSetNameUseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="b7a1b-109">ParameterSetNameUseForPeeringService</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -UseForPeeringService <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7a1b-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7a1b-110">DESCRIPTION</span></span>
<span data-ttu-id="b7a1b-111">Usato in combinazione con Update-AzPeering, si tratta di un'operazione in memoria che verrà mantenuta solo con `Update-AzPeering` .</span><span class="sxs-lookup"><span data-stu-id="b7a1b-111">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="b7a1b-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7a1b-112">EXAMPLES</span></span>

### <span data-ttu-id="b7a1b-113">Larghezza di banda di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="b7a1b-113">Upgrade Bandwidth</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -BandwidthInMbps 30000
```

<span data-ttu-id="b7a1b-114">Aggiorna la larghezza di banda per la prima connessione nell'oggetto peering in memoria.</span><span class="sxs-lookup"><span data-stu-id="b7a1b-114">Upgrades the bandwidth for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="b7a1b-115">Aggiornare l'indirizzo della sessione BGP</span><span class="sxs-lookup"><span data-stu-id="b7a1b-115">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -SessionPrefixV4 "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="b7a1b-116">Aggiorna l'indirizzo di peering per la prima connessione nell'oggetto peering in memoria.</span><span class="sxs-lookup"><span data-stu-id="b7a1b-116">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="b7a1b-117">Aggiornare l'uso per il servizio peering</span><span class="sxs-lookup"><span data-stu-id="b7a1b-117">Update Use for peering service</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -UseForPeeringService $true

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 16c24fd5-89aa-48d7-a101-38ca68a4ce6d
BandwidthInMbps        : 30000
```

<span data-ttu-id="b7a1b-118">Aggiorna la connessione per l'utilizzo con il servizio peering</span><span class="sxs-lookup"><span data-stu-id="b7a1b-118">Updates the connection for use with peering service</span></span>

## <span data-ttu-id="b7a1b-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7a1b-119">PARAMETERS</span></span>

### <span data-ttu-id="b7a1b-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="b7a1b-120">-BandwidthInMbps</span></span>
<span data-ttu-id="b7a1b-121">Larghezza di banda offerta in questa posizione in Mbps.</span><span class="sxs-lookup"><span data-stu-id="b7a1b-121">The Bandwidth offered at this location in Mbps.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Bandwidth
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7a1b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7a1b-122">-DefaultProfile</span></span>
<span data-ttu-id="b7a1b-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7a1b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7a1b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7a1b-124">-InputObject</span></span>
<span data-ttu-id="b7a1b-125">Oggetto connessione diretta</span><span class="sxs-lookup"><span data-stu-id="b7a1b-125">The direct connection Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a1b-126">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="b7a1b-126">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="b7a1b-127">Il numero massimo di IPv4 pubblicizzato</span><span class="sxs-lookup"><span data-stu-id="b7a1b-127">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7a1b-128">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="b7a1b-128">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="b7a1b-129">Il numero massimo di IPv6 pubblicizzato</span><span class="sxs-lookup"><span data-stu-id="b7a1b-129">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7a1b-130">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="b7a1b-130">-MD5AuthenticationKey</span></span>
<span data-ttu-id="b7a1b-131">Chiave di autenticazione MD5 per Session.</span><span class="sxs-lookup"><span data-stu-id="b7a1b-131">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="b7a1b-132">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="b7a1b-132">-SessionPrefixV4</span></span>
<span data-ttu-id="b7a1b-133">Indirizzo IPv4 della sessione peer</span><span class="sxs-lookup"><span data-stu-id="b7a1b-133">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Prefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7a1b-134">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="b7a1b-134">-SessionPrefixV6</span></span>
<span data-ttu-id="b7a1b-135">Indirizzo IPv6 della sessione peer</span><span class="sxs-lookup"><span data-stu-id="b7a1b-135">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Prefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7a1b-136">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="b7a1b-136">-UseForPeeringService</span></span>
<span data-ttu-id="b7a1b-137">Enable per l'uso con Microsoft peering Service (MPS).</span><span class="sxs-lookup"><span data-stu-id="b7a1b-137">Enable for use with Microsoft Peering Service (MPS).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: ParameterSetNameUseForPeeringService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7a1b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7a1b-138">CommonParameters</span></span>
<span data-ttu-id="b7a1b-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7a1b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7a1b-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7a1b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7a1b-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7a1b-141">INPUTS</span></span>

### <span data-ttu-id="b7a1b-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="b7a1b-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="b7a1b-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7a1b-143">OUTPUTS</span></span>

### <span data-ttu-id="b7a1b-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="b7a1b-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="b7a1b-145">Note</span><span class="sxs-lookup"><span data-stu-id="b7a1b-145">NOTES</span></span>

## <span data-ttu-id="b7a1b-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7a1b-146">RELATED LINKS</span></span>
