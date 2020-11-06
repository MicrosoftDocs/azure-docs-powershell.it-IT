---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: 638617cfe55e01121b46c7fe283d3664948e76b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507447"
---
# <span data-ttu-id="a5eea-101">New-AzureRmFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="a5eea-101">New-AzureRmFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="a5eea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a5eea-102">SYNOPSIS</span></span>
<span data-ttu-id="a5eea-103">Creare un oggetto PSFrontendEndpoint per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="a5eea-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5eea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5eea-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <PSCertificateSource>]
 [-ProtocolType <PSProtocolType>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <PSCertificateType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5eea-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5eea-105">DESCRIPTION</span></span>
<span data-ttu-id="a5eea-106">Creare un oggetto PSFrontendEndpoint per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="a5eea-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="a5eea-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5eea-107">EXAMPLES</span></span>

### <span data-ttu-id="a5eea-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a5eea-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorFrontendEndpointObject -Name "frontendendpoint1" -HostName $hostName


HostName                         : frontdoor5.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     :
CustomHttpsProvisioningSubstate  :
CertificateSource                : AzureKeyVault
ProtocolType                     : ServerNameIndication
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  : Shared
ResourceState                    :
Id                               :
Name                             : frontendendpoint1
Type                             :
```

<span data-ttu-id="a5eea-109">Creare un oggetto PSFrontendEndpoint per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="a5eea-109">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="a5eea-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a5eea-110">PARAMETERS</span></span>

### <span data-ttu-id="a5eea-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="a5eea-111">-CertificateSource</span></span>
<span data-ttu-id="a5eea-112">Origine del certificato SSL</span><span class="sxs-lookup"><span data-stu-id="a5eea-112">The source of the SSL certificate</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCertificateSource
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, FrontDoor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5eea-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="a5eea-113">-CertificateType</span></span>
<span data-ttu-id="a5eea-114">tipo del certificato usato per le connessioni sicure a un frontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="a5eea-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCertificateType
Parameter Sets: (All)
Aliases:
Accepted values: Shared, Dedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5eea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5eea-115">-DefaultProfile</span></span>
<span data-ttu-id="a5eea-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a5eea-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5eea-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="a5eea-117">-HostName</span></span>
<span data-ttu-id="a5eea-118">Nome host di frontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a5eea-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="a5eea-119">Deve essere un nome di dominio.</span><span class="sxs-lookup"><span data-stu-id="a5eea-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="a5eea-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5eea-120">-Name</span></span>
<span data-ttu-id="a5eea-121">Nome endpoint frontend.</span><span class="sxs-lookup"><span data-stu-id="a5eea-121">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="a5eea-122">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="a5eea-122">-ProtocolType</span></span>
<span data-ttu-id="a5eea-123">Protocollo di estensione TLS usato per il recapito sicuro</span><span class="sxs-lookup"><span data-stu-id="a5eea-123">The TLS extension protocol that is used for secure delivery</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocolType
Parameter Sets: (All)
Aliases:
Accepted values: ServerNameIndication, IPBased

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5eea-124">-Secretname</span><span class="sxs-lookup"><span data-stu-id="a5eea-124">-SecretName</span></span>
<span data-ttu-id="a5eea-125">Nome del segreto del Vault chiave che rappresenta il PFX completo del certificato</span><span class="sxs-lookup"><span data-stu-id="a5eea-125">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="a5eea-126">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="a5eea-126">-SecretVersion</span></span>
<span data-ttu-id="a5eea-127">La versione del segreto del Vault Key che rappresenta il PFX completo del certificato</span><span class="sxs-lookup"><span data-stu-id="a5eea-127">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="a5eea-128">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="a5eea-128">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="a5eea-129">Se consentire l'affinità della sessione in questo host.</span><span class="sxs-lookup"><span data-stu-id="a5eea-129">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="a5eea-130">Il valore predefinito è Disabled</span><span class="sxs-lookup"><span data-stu-id="a5eea-130">Default value is Disabled</span></span>

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

### <span data-ttu-id="a5eea-131">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="a5eea-131">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="a5eea-132">Il TTL da usare in secondi per l'affinità della sessione, se applicabile.</span><span class="sxs-lookup"><span data-stu-id="a5eea-132">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="a5eea-133">Il valore predefinito è 0</span><span class="sxs-lookup"><span data-stu-id="a5eea-133">Default value is 0</span></span>

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

### <span data-ttu-id="a5eea-134">-Vault</span><span class="sxs-lookup"><span data-stu-id="a5eea-134">-Vault</span></span>
<span data-ttu-id="a5eea-135">Il Vault Key contenente il certificato SSL</span><span class="sxs-lookup"><span data-stu-id="a5eea-135">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="a5eea-136">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="a5eea-136">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="a5eea-137">ID risorsa dei criteri di firewall delle applicazioni Web per ogni host (se applicabile)</span><span class="sxs-lookup"><span data-stu-id="a5eea-137">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="a5eea-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5eea-138">CommonParameters</span></span>
<span data-ttu-id="a5eea-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5eea-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5eea-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5eea-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5eea-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a5eea-141">INPUTS</span></span>

### <span data-ttu-id="a5eea-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a5eea-142">None</span></span>

## <span data-ttu-id="a5eea-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5eea-143">OUTPUTS</span></span>

### <span data-ttu-id="a5eea-144">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="a5eea-144">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="a5eea-145">Note</span><span class="sxs-lookup"><span data-stu-id="a5eea-145">NOTES</span></span>

## <span data-ttu-id="a5eea-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5eea-146">RELATED LINKS</span></span>

<span data-ttu-id="a5eea-147">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="a5eea-147">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
