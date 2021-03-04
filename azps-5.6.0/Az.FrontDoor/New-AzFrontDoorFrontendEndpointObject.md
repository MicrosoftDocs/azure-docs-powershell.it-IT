---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: a106295a883cc6729ddf7c5d4235a87ff036f066
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971070"
---
# <span data-ttu-id="87ae5-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="87ae5-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="87ae5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87ae5-102">SYNOPSIS</span></span>
<span data-ttu-id="87ae5-103">Creare un oggetto PSFrontendEndpoint per la creazione della porta anteriore</span><span class="sxs-lookup"><span data-stu-id="87ae5-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="87ae5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="87ae5-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <String>] [-MinimumTlsVersion <String>]
 [-ProtocolType <String>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87ae5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="87ae5-105">DESCRIPTION</span></span>
<span data-ttu-id="87ae5-106">Creare un oggetto PSFrontendEndpoint per la creazione della porta anteriore</span><span class="sxs-lookup"><span data-stu-id="87ae5-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="87ae5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="87ae5-107">EXAMPLES</span></span>

### <span data-ttu-id="87ae5-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="87ae5-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorFrontendEndpointObject -Name "frontendendpoint1" -HostName "frontendendpoint1"


HostName                         : frontendendpoint1
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     :
CustomHttpsProvisioningSubstate  :
CertificateSource                :
MinimumTlsVersion                : 1.2
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    :
Id                               :
Name                             : frontendendpoint1
Type                             :
ProtocolType                     : ServerNameIndication
```

<span data-ttu-id="87ae5-109">Creare un oggetto PSFrontendEndpoint per la creazione della porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="87ae5-109">Create a PSFrontendEndpoint Object for Front Door creation.</span></span>

## <span data-ttu-id="87ae5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87ae5-110">PARAMETERS</span></span>

### <span data-ttu-id="87ae5-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="87ae5-111">-CertificateSource</span></span>
<span data-ttu-id="87ae5-112">Origine del certificato SSL</span><span class="sxs-lookup"><span data-stu-id="87ae5-112">The source of the SSL certificate</span></span>

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

### <span data-ttu-id="87ae5-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="87ae5-113">-CertificateType</span></span>
<span data-ttu-id="87ae5-114">il tipo di certificato usato per le connessioni sicure a frontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="87ae5-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

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

### <span data-ttu-id="87ae5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87ae5-115">-DefaultProfile</span></span>
<span data-ttu-id="87ae5-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="87ae5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87ae5-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="87ae5-117">-HostName</span></span>
<span data-ttu-id="87ae5-118">Nome host del frontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="87ae5-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="87ae5-119">Deve essere un nome di dominio.</span><span class="sxs-lookup"><span data-stu-id="87ae5-119">Must be a domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ae5-120">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="87ae5-120">-MinimumTlsVersion</span></span>
<span data-ttu-id="87ae5-121">La versione minima di TLS richiesta dai client per stabilire un handshake SSL con Front Door.</span><span class="sxs-lookup"><span data-stu-id="87ae5-121">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="87ae5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="87ae5-122">-Name</span></span>
<span data-ttu-id="87ae5-123">Nome dell'endpoint frontend.</span><span class="sxs-lookup"><span data-stu-id="87ae5-123">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ae5-124">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="87ae5-124">-ProtocolType</span></span>
<span data-ttu-id="87ae5-125">Protocollo di estensione TLS usato per il recapito sicuro</span><span class="sxs-lookup"><span data-stu-id="87ae5-125">The TLS extension protocol that is used for secure delivery</span></span>

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

### <span data-ttu-id="87ae5-126">-SecretName</span><span class="sxs-lookup"><span data-stu-id="87ae5-126">-SecretName</span></span>
<span data-ttu-id="87ae5-127">Nome del segreto del Vault delle chiavi che rappresenta il certificato completo PFX</span><span class="sxs-lookup"><span data-stu-id="87ae5-127">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="87ae5-128">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="87ae5-128">-SecretVersion</span></span>
<span data-ttu-id="87ae5-129">Versione del segreto del Vault delle chiavi che rappresenta il certificato completo PFX</span><span class="sxs-lookup"><span data-stu-id="87ae5-129">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="87ae5-130">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="87ae5-130">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="87ae5-131">Se consentire l'affinità di sessione in questo host.</span><span class="sxs-lookup"><span data-stu-id="87ae5-131">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="87ae5-132">Il valore predefinito è Disabilitato</span><span class="sxs-lookup"><span data-stu-id="87ae5-132">Default value is Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ae5-133">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="87ae5-133">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="87ae5-134">Il TTL da usare in secondi per l'affinità di sessione, se applicabile.</span><span class="sxs-lookup"><span data-stu-id="87ae5-134">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="87ae5-135">Il valore predefinito è 0</span><span class="sxs-lookup"><span data-stu-id="87ae5-135">Default value is 0</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ae5-136">-Vault</span><span class="sxs-lookup"><span data-stu-id="87ae5-136">-Vault</span></span>
<span data-ttu-id="87ae5-137">Il Vault delle chiavi che contiene il certificato SSL</span><span class="sxs-lookup"><span data-stu-id="87ae5-137">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="87ae5-138">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="87ae5-138">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="87ae5-139">ID risorsa dei criteri di Firewall applicazione Web per ogni host (se applicabile)</span><span class="sxs-lookup"><span data-stu-id="87ae5-139">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="87ae5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87ae5-140">CommonParameters</span></span>
<span data-ttu-id="87ae5-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87ae5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87ae5-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="87ae5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87ae5-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="87ae5-143">INPUTS</span></span>

### <span data-ttu-id="87ae5-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="87ae5-144">None</span></span>
## <span data-ttu-id="87ae5-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="87ae5-145">OUTPUTS</span></span>

### <span data-ttu-id="87ae5-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="87ae5-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="87ae5-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="87ae5-147">NOTES</span></span>

## <span data-ttu-id="87ae5-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="87ae5-148">RELATED LINKS</span></span>

<span data-ttu-id="87ae5-149">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="87ae5-149">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
