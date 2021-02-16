---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 3d58834dbd80549aed52104e84099544a427fa1d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184031"
---
# <span data-ttu-id="dcc57-101">New-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="dcc57-101">New-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="dcc57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcc57-102">SYNOPSIS</span></span>
<span data-ttu-id="dcc57-103">Crea un OGGETTO PSObject in memoria da usare per creare o modificare un peering.</span><span class="sxs-lookup"><span data-stu-id="dcc57-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="dcc57-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dcc57-104">SYNTAX</span></span>

### <span data-ttu-id="dcc57-105">IPv4PrefixIPv6Prefix (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dcc57-105">IPv4PrefixIPv6Prefix (Default)</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-SessionPrefixV4 <String>]
 [-SessionPrefixV6 <String>] -BandwidthInMbps <Int32> [-UseForPeeringService]
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcc57-106">ParameterSetNameMicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="dcc57-106">ParameterSetNameMicrosoftProvidedIPAddress</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-MicrosoftProvidedIPAddress]
 -BandwidthInMbps <Int32> [-UseForPeeringService] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dcc57-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dcc57-107">DESCRIPTION</span></span>
<span data-ttu-id="dcc57-108">Crea un oggetto PSObject in memoria</span><span class="sxs-lookup"><span data-stu-id="dcc57-108">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="dcc57-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dcc57-109">EXAMPLES</span></span>

### <span data-ttu-id="dcc57-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dcc57-110">Example 1</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000 -SessionPrefixV4 192.168.1.0/31 -SessionPrefixV6 fe01::0/127 -MaxPrefixesAdvertisedIPv4 20000 -MaxPrefixesAdvertisedIPv6 2000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId    : 99999
UseForPeeringService   : False
SessionAddressProvider : Peer
SessionPrefixV4        : 192.168.1.0/31
ConnectionIdentifier   : 6d771cef-7169-4b0a-b028-c7270054bd31
SessionPrefixV6        : fe01::0/127
BandwidthInMbps        : 30000
Md5AuthenticationKey   : 25234523452123411fd234qdwfas3234
SessionStateV4         :
SessionStateV6         :
```

<span data-ttu-id="dcc57-111">Nuova connessione locale</span><span class="sxs-lookup"><span data-stu-id="dcc57-111">New local connection</span></span>

### <span data-ttu-id="dcc57-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="dcc57-112">Example 2</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -MicrosoftProvidedIPAddress -BandwidthInMbps 30000 -UseForPeeringService

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 1de364bf-74ea-4088-ad17-bb79c16cfa81
BandwidthInMbps        : 30000
```

<span data-ttu-id="dcc57-113">Creare una connessione peering diretta con l'uso per il servizio di peering abilitato e indirizzi IP forniti da Microsoft</span><span class="sxs-lookup"><span data-stu-id="dcc57-113">Create direct peering connection with use for peering service enabled and Microsoft provided IP addresses</span></span>

### <span data-ttu-id="dcc57-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="dcc57-114">Example 3</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000 -SessionPrefixV4 192.168.1.0/31 -SessionPrefixV6 fe01::0/127 -UseForPeeringService

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Peer
SessionPrefixV4        : 192.168.1.0/31
ConnectionIdentifier   : 74ea6eab-5625-4170-a642-822e85d97566
SessionPrefixV6        : fe01::0/127
BandwidthInMbps        : 30000
SessionStateV4         :
SessionStateV6         :
```

<span data-ttu-id="dcc57-115">Creare una connessione peering diretta con l'uso per il servizio di peering abilitato e gli indirizzi IP forniti dal peer</span><span class="sxs-lookup"><span data-stu-id="dcc57-115">Create direct peering connection with use for peering service enabled and peer provided IP Addresses</span></span>

### <span data-ttu-id="dcc57-116">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="dcc57-116">Example 4</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000

PeeringDBFacilityId    : 99999
UseForPeeringService   : False
SessionAddressProvider : Peer
ConnectionIdentifier   : 920f128a-c9d8-4514-a2e0-c533ab1a550c
BandwidthInMbps        : 30000
```

<span data-ttu-id="dcc57-117">Creare una connessione peering diretta senza indirizzi IP della sessione bgp.</span><span class="sxs-lookup"><span data-stu-id="dcc57-117">Create direct peering connection without bgp session IP addresses.</span></span> <span data-ttu-id="dcc57-118">Il peer dovrà impostare gli indirizzi IP prima di configurare la sessione bgp.</span><span class="sxs-lookup"><span data-stu-id="dcc57-118">The peer will have to set the IP addresses before the bgp session can be configured.</span></span>

## <span data-ttu-id="dcc57-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcc57-119">PARAMETERS</span></span>

### <span data-ttu-id="dcc57-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="dcc57-120">-BandwidthInMbps</span></span>
<span data-ttu-id="dcc57-121">La larghezza di banda disponibile in questa posizione in Mbps.</span><span class="sxs-lookup"><span data-stu-id="dcc57-121">The Bandwidth offered at this location in Mbps.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc57-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcc57-122">-DefaultProfile</span></span>
<span data-ttu-id="dcc57-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dcc57-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcc57-124">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="dcc57-124">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="dcc57-125">Il numero massimo di IPv4 annunciati</span><span class="sxs-lookup"><span data-stu-id="dcc57-125">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc57-126">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="dcc57-126">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="dcc57-127">Il numero massimo di IPv6 annunciati</span><span class="sxs-lookup"><span data-stu-id="dcc57-127">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc57-128">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="dcc57-128">-MD5AuthenticationKey</span></span>
<span data-ttu-id="dcc57-129">Chiave di autenticazione MD5 per la sessione.</span><span class="sxs-lookup"><span data-stu-id="dcc57-129">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc57-130">-MicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="dcc57-130">-MicrosoftProvidedIPAddress</span></span>
<span data-ttu-id="dcc57-131">Abilitare il contrassegno che indica a Microsoft di fornire gli indirizzi di sessione BGP.</span><span class="sxs-lookup"><span data-stu-id="dcc57-131">Enable flag that tells Microsoft to provide the BGP session addresses.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ParameterSetNameMicrosoftProvidedIPAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc57-132">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="dcc57-132">-PeeringDBFacilityId</span></span>
<span data-ttu-id="dcc57-133">ID della struttura di peering trovato in https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="dcc57-133">The peering facility Id found on https://peeringdb.com</span></span>

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

### <span data-ttu-id="dcc57-134">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="dcc57-134">-SessionPrefixV4</span></span>
<span data-ttu-id="dcc57-135">Indirizzo IPv4 della sessione peer</span><span class="sxs-lookup"><span data-stu-id="dcc57-135">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc57-136">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="dcc57-136">-SessionPrefixV6</span></span>
<span data-ttu-id="dcc57-137">Indirizzo IPv6 della sessione peer</span><span class="sxs-lookup"><span data-stu-id="dcc57-137">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc57-138">-UseForServingService</span><span class="sxs-lookup"><span data-stu-id="dcc57-138">-UseForPeeringService</span></span>
<span data-ttu-id="dcc57-139">Abilita per l'uso con il servizio di peering Microsoft (MPS).</span><span class="sxs-lookup"><span data-stu-id="dcc57-139">Enable for use with Microsoft Peering Service (MPS).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc57-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcc57-140">CommonParameters</span></span>
<span data-ttu-id="dcc57-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcc57-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcc57-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dcc57-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcc57-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="dcc57-143">INPUTS</span></span>

### <span data-ttu-id="dcc57-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="dcc57-144">None</span></span>

## <span data-ttu-id="dcc57-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dcc57-145">OUTPUTS</span></span>

### <span data-ttu-id="dcc57-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="dcc57-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="dcc57-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="dcc57-147">NOTES</span></span>

## <span data-ttu-id="dcc57-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dcc57-148">RELATED LINKS</span></span>
