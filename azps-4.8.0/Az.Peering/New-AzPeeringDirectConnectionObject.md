---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 3d58834dbd80549aed52104e84099544a427fa1d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190896"
---
# <span data-ttu-id="692e0-101">New-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="692e0-101">New-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="692e0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="692e0-102">SYNOPSIS</span></span>
<span data-ttu-id="692e0-103">Crea un PSObject in memoria da usare per creare o modificare un peering.</span><span class="sxs-lookup"><span data-stu-id="692e0-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="692e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="692e0-104">SYNTAX</span></span>

### <span data-ttu-id="692e0-105">IPv4PrefixIPv6Prefix (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="692e0-105">IPv4PrefixIPv6Prefix (Default)</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-SessionPrefixV4 <String>]
 [-SessionPrefixV6 <String>] -BandwidthInMbps <Int32> [-UseForPeeringService]
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="692e0-106">ParameterSetNameMicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="692e0-106">ParameterSetNameMicrosoftProvidedIPAddress</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-MicrosoftProvidedIPAddress]
 -BandwidthInMbps <Int32> [-UseForPeeringService] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="692e0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="692e0-107">DESCRIPTION</span></span>
<span data-ttu-id="692e0-108">Crea un PSObject in memoria</span><span class="sxs-lookup"><span data-stu-id="692e0-108">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="692e0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="692e0-109">EXAMPLES</span></span>

### <span data-ttu-id="692e0-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="692e0-110">Example 1</span></span>
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

<span data-ttu-id="692e0-111">Nuova connessione locale</span><span class="sxs-lookup"><span data-stu-id="692e0-111">New local connection</span></span>

### <span data-ttu-id="692e0-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="692e0-112">Example 2</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -MicrosoftProvidedIPAddress -BandwidthInMbps 30000 -UseForPeeringService

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 1de364bf-74ea-4088-ad17-bb79c16cfa81
BandwidthInMbps        : 30000
```

<span data-ttu-id="692e0-113">Creare una connessione diretta con peering con l'uso del servizio di peering abilitato e gli indirizzi IP forniti da Microsoft</span><span class="sxs-lookup"><span data-stu-id="692e0-113">Create direct peering connection with use for peering service enabled and Microsoft provided IP addresses</span></span>

### <span data-ttu-id="692e0-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="692e0-114">Example 3</span></span>
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

<span data-ttu-id="692e0-115">Creare una connessione diretta con peering con l'uso dei servizi di peering abilitati e degli indirizzi IP forniti peer</span><span class="sxs-lookup"><span data-stu-id="692e0-115">Create direct peering connection with use for peering service enabled and peer provided IP Addresses</span></span>

### <span data-ttu-id="692e0-116">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="692e0-116">Example 4</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000

PeeringDBFacilityId    : 99999
UseForPeeringService   : False
SessionAddressProvider : Peer
ConnectionIdentifier   : 920f128a-c9d8-4514-a2e0-c533ab1a550c
BandwidthInMbps        : 30000
```

<span data-ttu-id="692e0-117">Creare una connessione diretta peering senza indirizzi IP della sessione BGP.</span><span class="sxs-lookup"><span data-stu-id="692e0-117">Create direct peering connection without bgp session IP addresses.</span></span> <span data-ttu-id="692e0-118">Il peer dovrà impostare gli indirizzi IP prima che la sessione BGP possa essere configurata.</span><span class="sxs-lookup"><span data-stu-id="692e0-118">The peer will have to set the IP addresses before the bgp session can be configured.</span></span>

## <span data-ttu-id="692e0-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="692e0-119">PARAMETERS</span></span>

### <span data-ttu-id="692e0-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="692e0-120">-BandwidthInMbps</span></span>
<span data-ttu-id="692e0-121">Larghezza di banda offerta in questa posizione in Mbps.</span><span class="sxs-lookup"><span data-stu-id="692e0-121">The Bandwidth offered at this location in Mbps.</span></span>

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

### <span data-ttu-id="692e0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="692e0-122">-DefaultProfile</span></span>
<span data-ttu-id="692e0-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="692e0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="692e0-124">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="692e0-124">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="692e0-125">Il numero massimo di IPv4 pubblicizzato</span><span class="sxs-lookup"><span data-stu-id="692e0-125">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="692e0-126">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="692e0-126">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="692e0-127">Il numero massimo di IPv6 pubblicizzato</span><span class="sxs-lookup"><span data-stu-id="692e0-127">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="692e0-128">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="692e0-128">-MD5AuthenticationKey</span></span>
<span data-ttu-id="692e0-129">Chiave di autenticazione MD5 per Session.</span><span class="sxs-lookup"><span data-stu-id="692e0-129">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="692e0-130">-MicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="692e0-130">-MicrosoftProvidedIPAddress</span></span>
<span data-ttu-id="692e0-131">Abilita contrassegno che indica a Microsoft di specificare gli indirizzi di sessione BGP.</span><span class="sxs-lookup"><span data-stu-id="692e0-131">Enable flag that tells Microsoft to provide the BGP session addresses.</span></span>

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

### <span data-ttu-id="692e0-132">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="692e0-132">-PeeringDBFacilityId</span></span>
<span data-ttu-id="692e0-133">ID struttura peering disponibile in https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="692e0-133">The peering facility Id found on https://peeringdb.com</span></span>

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

### <span data-ttu-id="692e0-134">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="692e0-134">-SessionPrefixV4</span></span>
<span data-ttu-id="692e0-135">Indirizzo IPv4 della sessione peer</span><span class="sxs-lookup"><span data-stu-id="692e0-135">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="692e0-136">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="692e0-136">-SessionPrefixV6</span></span>
<span data-ttu-id="692e0-137">Indirizzo IPv6 della sessione peer</span><span class="sxs-lookup"><span data-stu-id="692e0-137">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="692e0-138">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="692e0-138">-UseForPeeringService</span></span>
<span data-ttu-id="692e0-139">Enable per l'uso con Microsoft peering Service (MPS).</span><span class="sxs-lookup"><span data-stu-id="692e0-139">Enable for use with Microsoft Peering Service (MPS).</span></span>

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

### <span data-ttu-id="692e0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="692e0-140">CommonParameters</span></span>
<span data-ttu-id="692e0-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="692e0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="692e0-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="692e0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="692e0-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="692e0-143">INPUTS</span></span>

### <span data-ttu-id="692e0-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="692e0-144">None</span></span>

## <span data-ttu-id="692e0-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="692e0-145">OUTPUTS</span></span>

### <span data-ttu-id="692e0-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="692e0-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="692e0-147">Note</span><span class="sxs-lookup"><span data-stu-id="692e0-147">NOTES</span></span>

## <span data-ttu-id="692e0-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="692e0-148">RELATED LINKS</span></span>
