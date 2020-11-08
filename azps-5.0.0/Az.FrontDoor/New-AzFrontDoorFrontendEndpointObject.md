---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: efb32f3fa73fac50e5f96100ed895c2ca7d4a83e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200880"
---
# <span data-ttu-id="6a3d2-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="6a3d2-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="6a3d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a3d2-102">SYNOPSIS</span></span>
<span data-ttu-id="6a3d2-103">Creare un oggetto PSFrontendEndpoint per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="6a3d2-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="6a3d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a3d2-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <String>] [-MinimumTlsVersion <String>]
 [-ProtocolType <String>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a3d2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a3d2-105">DESCRIPTION</span></span>
<span data-ttu-id="6a3d2-106">Creare un oggetto PSFrontendEndpoint per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="6a3d2-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="6a3d2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a3d2-107">EXAMPLES</span></span>

### <span data-ttu-id="6a3d2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6a3d2-108">Example 1</span></span>
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

<span data-ttu-id="6a3d2-109">Crea un oggetto PSFrontendEndpoint per la creazione di porte anteriori.</span><span class="sxs-lookup"><span data-stu-id="6a3d2-109">Create a PSFrontendEndpoint Object for Front Door creation.</span></span>

## <span data-ttu-id="6a3d2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a3d2-110">PARAMETERS</span></span>

### <span data-ttu-id="6a3d2-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="6a3d2-111">-CertificateSource</span></span>
<span data-ttu-id="6a3d2-112">Origine del certificato SSL</span><span class="sxs-lookup"><span data-stu-id="6a3d2-112">The source of the SSL certificate</span></span>

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

### <span data-ttu-id="6a3d2-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="6a3d2-113">-CertificateType</span></span>
<span data-ttu-id="6a3d2-114">tipo del certificato usato per le connessioni sicure a un frontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="6a3d2-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

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

### <span data-ttu-id="6a3d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a3d2-115">-DefaultProfile</span></span>
<span data-ttu-id="6a3d2-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a3d2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a3d2-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="6a3d2-117">-HostName</span></span>
<span data-ttu-id="6a3d2-118">Nome host di frontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="6a3d2-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="6a3d2-119">Deve essere un nome di dominio.</span><span class="sxs-lookup"><span data-stu-id="6a3d2-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="6a3d2-120">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="6a3d2-120">-MinimumTlsVersion</span></span>
<span data-ttu-id="6a3d2-121">La versione minima di TLS richiesta dai client per stabilire un handshake SSL con porta principale.</span><span class="sxs-lookup"><span data-stu-id="6a3d2-121">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="6a3d2-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a3d2-122">-Name</span></span>
<span data-ttu-id="6a3d2-123">Nome endpoint frontend.</span><span class="sxs-lookup"><span data-stu-id="6a3d2-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="6a3d2-124">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="6a3d2-124">-ProtocolType</span></span>
<span data-ttu-id="6a3d2-125">Protocollo di estensione TLS usato per il recapito sicuro</span><span class="sxs-lookup"><span data-stu-id="6a3d2-125">The TLS extension protocol that is used for secure delivery</span></span>

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

### <span data-ttu-id="6a3d2-126">-Secretname</span><span class="sxs-lookup"><span data-stu-id="6a3d2-126">-SecretName</span></span>
<span data-ttu-id="6a3d2-127">Nome del segreto del Vault chiave che rappresenta il PFX completo del certificato</span><span class="sxs-lookup"><span data-stu-id="6a3d2-127">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="6a3d2-128">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="6a3d2-128">-SecretVersion</span></span>
<span data-ttu-id="6a3d2-129">La versione del segreto del Vault Key che rappresenta il PFX completo del certificato</span><span class="sxs-lookup"><span data-stu-id="6a3d2-129">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="6a3d2-130">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="6a3d2-130">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="6a3d2-131">Se consentire l'affinità della sessione in questo host.</span><span class="sxs-lookup"><span data-stu-id="6a3d2-131">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="6a3d2-132">Il valore predefinito è Disabled</span><span class="sxs-lookup"><span data-stu-id="6a3d2-132">Default value is Disabled</span></span>

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

### <span data-ttu-id="6a3d2-133">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="6a3d2-133">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="6a3d2-134">Il TTL da usare in secondi per l'affinità della sessione, se applicabile.</span><span class="sxs-lookup"><span data-stu-id="6a3d2-134">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="6a3d2-135">Il valore predefinito è 0</span><span class="sxs-lookup"><span data-stu-id="6a3d2-135">Default value is 0</span></span>

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

### <span data-ttu-id="6a3d2-136">-Vault</span><span class="sxs-lookup"><span data-stu-id="6a3d2-136">-Vault</span></span>
<span data-ttu-id="6a3d2-137">Il Vault Key contenente il certificato SSL</span><span class="sxs-lookup"><span data-stu-id="6a3d2-137">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="6a3d2-138">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="6a3d2-138">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="6a3d2-139">ID risorsa dei criteri di firewall delle applicazioni Web per ogni host (se applicabile)</span><span class="sxs-lookup"><span data-stu-id="6a3d2-139">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="6a3d2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a3d2-140">CommonParameters</span></span>
<span data-ttu-id="6a3d2-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a3d2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a3d2-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a3d2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a3d2-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a3d2-143">INPUTS</span></span>

### <span data-ttu-id="6a3d2-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6a3d2-144">None</span></span>
## <span data-ttu-id="6a3d2-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a3d2-145">OUTPUTS</span></span>

### <span data-ttu-id="6a3d2-146">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="6a3d2-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="6a3d2-147">Note</span><span class="sxs-lookup"><span data-stu-id="6a3d2-147">NOTES</span></span>

## <span data-ttu-id="6a3d2-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a3d2-148">RELATED LINKS</span></span>

<span data-ttu-id="6a3d2-149">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="6a3d2-149">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
