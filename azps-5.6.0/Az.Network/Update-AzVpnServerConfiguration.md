---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: e5bd6c612cb78d2c6d38a1484452c814ecdf714c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951438"
---
# <span data-ttu-id="9fb3a-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fb3a-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="9fb3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fb3a-102">SYNOPSIS</span></span>
<span data-ttu-id="9fb3a-103">Aggiorna una VpnServerConfiguration esistente.</span><span class="sxs-lookup"><span data-stu-id="9fb3a-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="9fb3a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9fb3a-104">SYNTAX</span></span>

### <span data-ttu-id="9fb3a-105">ByVpnServerConfigurationName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9fb3a-105">ByVpnServerConfigurationName (Default)</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9fb3a-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="9fb3a-106">ByVpnServerConfigurationObject</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9fb3a-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="9fb3a-107">ByVpnServerConfigurationResourceId</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9fb3a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9fb3a-108">DESCRIPTION</span></span>
<span data-ttu-id="9fb3a-109">Il cmdlet **Update-AzVpnServerConfiguration** consente di aggiornare la vpnServerConfiguration esistente con vpnprotocols, VpnAuthenticationTypes, IpsecPolicies e di impostare i parametri correlati al tipo di autenticazione VPN in base ai requisiti del cliente per la connettività tra siti.</span><span class="sxs-lookup"><span data-stu-id="9fb3a-109">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="9fb3a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9fb3a-110">EXAMPLES</span></span>

### <span data-ttu-id="9fb3a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9fb3a-111">Example 1</span></span>
```powershell
PS C:\> Update-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2

PS C:\> New-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2 -VpnAuthenticationType Certificate -VpnClientRootCertificateFilesList $listOfCerts -VpnClientRevokedCertificateFilesList $listOfCerts -Location "westus"
ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2}
VpnAuthenticationTypes       : {Certificate}
VpnClientRootCertificates    :
VpnClientRevokedCertificates : [
                                 {
                                   "Name": "cert2",
                                   "Thumbprint": "83FFBFC8848B5A5836C94D0112367E16148A286F"
                                 }
                               ]
RadiusServerAddress          :
RadiusServerRootCertificates : []
RadiusClientRootCertificates : []
VpnClientIpsecPolicies       : []
AadAuthenticationParameters  : null
P2sVpnGateways               : []
Type                         : Microsoft.Network/vpnServerConfigurations
ProvisioningState            : Succeeded
```

<span data-ttu-id="9fb3a-112">Il comando precedente aggiornerà una VpnServerConfiguration esistente con VpnProtocol come IkeV2.</span><span class="sxs-lookup"><span data-stu-id="9fb3a-112">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="9fb3a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9fb3a-113">PARAMETERS</span></span>

### <span data-ttu-id="9fb3a-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="9fb3a-114">-AadAudience</span></span>
<span data-ttu-id="9fb3a-115">Gruppo di destinatari AAD per l'autenticazione AAD P2S.</span><span class="sxs-lookup"><span data-stu-id="9fb3a-115">AAD audience for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="9fb3a-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="9fb3a-116">-AadIssuer</span></span>
<span data-ttu-id="9fb3a-117">Autorità emittente di AAD per l'autenticazione AAD P2S.</span><span class="sxs-lookup"><span data-stu-id="9fb3a-117">AAD issuer for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="9fb3a-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="9fb3a-118">-AadTenant</span></span>
<span data-ttu-id="9fb3a-119">Tenant AAD per l'autenticazione AAD P2S.</span><span class="sxs-lookup"><span data-stu-id="9fb3a-119">AAD tenant for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="9fb3a-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9fb3a-120">-AsJob</span></span>
<span data-ttu-id="9fb3a-121">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9fb3a-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9fb3a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fb3a-122">-DefaultProfile</span></span>
<span data-ttu-id="9fb3a-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9fb3a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fb3a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fb3a-124">-InputObject</span></span>
<span data-ttu-id="9fb3a-125">Oggetto di configurazione del server VPN da modificare</span><span class="sxs-lookup"><span data-stu-id="9fb3a-125">The vpn server configuration object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObject
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3a-126">-Name</span><span class="sxs-lookup"><span data-stu-id="9fb3a-126">-Name</span></span>
<span data-ttu-id="9fb3a-127">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9fb3a-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationName
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3a-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="9fb3a-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="9fb3a-129">Elenco dei percorsi dei file RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9fb3a-129">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3a-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="9fb3a-130">-RadiusServerAddress</span></span>
<span data-ttu-id="9fb3a-131">Indirizzo server raggio esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="9fb3a-131">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="9fb3a-132">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="9fb3a-132">-RadiusServerList</span></span>
<span data-ttu-id="9fb3a-133">P2S External multiple radius servers.</span><span class="sxs-lookup"><span data-stu-id="9fb3a-133">P2S External multiple radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3a-134">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="9fb3a-134">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="9fb3a-135">Elenco dei percorsi dei file RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9fb3a-135">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3a-136">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="9fb3a-136">-RadiusServerSecret</span></span>
<span data-ttu-id="9fb3a-137">Segreto server raggio esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="9fb3a-137">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fb3a-138">-ResourceGroupName</span></span>
<span data-ttu-id="9fb3a-139">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9fb3a-139">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3a-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fb3a-140">-ResourceId</span></span>
<span data-ttu-id="9fb3a-141">ID risorsa di Azure per la configurazione del server VPN.</span><span class="sxs-lookup"><span data-stu-id="9fb3a-141">The Azure resource ID for the vpn server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationResourceId
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3a-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="9fb3a-142">-Tag</span></span>
<span data-ttu-id="9fb3a-143">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="9fb3a-143">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3a-144">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="9fb3a-144">-VpnAuthenticationType</span></span>
<span data-ttu-id="9fb3a-145">L'elenco dei protocolli di tunneling del client VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="9fb3a-145">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Certificate, Radius, AAD

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3a-146">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="9fb3a-146">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="9fb3a-147">Elenco dei criteri IPSec per VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9fb3a-147">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3a-148">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="9fb3a-148">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="9fb3a-149">Elenco di VpnClientCertificates da revocare per i percorsi dei file</span><span class="sxs-lookup"><span data-stu-id="9fb3a-149">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3a-150">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="9fb3a-150">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="9fb3a-151">Elenco di VpnClientRootCertificates da aggiungere ai percorsi dei file</span><span class="sxs-lookup"><span data-stu-id="9fb3a-151">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3a-152">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="9fb3a-152">-VpnProtocol</span></span>
<span data-ttu-id="9fb3a-153">L'elenco dei protocolli di tunneling del client VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="9fb3a-153">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3a-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9fb3a-154">-Confirm</span></span>
<span data-ttu-id="9fb3a-155">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fb3a-155">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3a-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fb3a-156">-WhatIf</span></span>
<span data-ttu-id="9fb3a-157">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9fb3a-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fb3a-158">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9fb3a-158">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3a-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fb3a-159">CommonParameters</span></span>
<span data-ttu-id="9fb3a-160">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fb3a-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fb3a-161">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9fb3a-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fb3a-162">INPUT</span><span class="sxs-lookup"><span data-stu-id="9fb3a-162">INPUTS</span></span>

### <span data-ttu-id="9fb3a-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fb3a-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="9fb3a-164">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="9fb3a-164">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="9fb3a-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9fb3a-165">OUTPUTS</span></span>

### <span data-ttu-id="9fb3a-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fb3a-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="9fb3a-167">NOTE</span><span class="sxs-lookup"><span data-stu-id="9fb3a-167">NOTES</span></span>

## <span data-ttu-id="9fb3a-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9fb3a-168">RELATED LINKS</span></span>
