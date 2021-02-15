---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: b46f346c1aa58b8c6f155ad9a742271fa121f630
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202668"
---
# <span data-ttu-id="2360c-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="2360c-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="2360c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2360c-102">SYNOPSIS</span></span>
<span data-ttu-id="2360c-103">Creare una nuova VpnServerConfiguration per la connettività del sito punto a punto.</span><span class="sxs-lookup"><span data-stu-id="2360c-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="2360c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2360c-104">SYNTAX</span></span>

```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2360c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2360c-105">DESCRIPTION</span></span>
<span data-ttu-id="2360c-106">Il cmdlet **New-AzVpnServerConfiguration** consente di creare una nuova VpnServerConfiguration con vpnProtocols, VpnAuthenticationTypes, IpsecPolicies e di impostare i parametri correlati al tipo di autenticazione vpn in base ai requisiti del cliente per la connettività punto a sito.</span><span class="sxs-lookup"><span data-stu-id="2360c-106">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="2360c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2360c-107">EXAMPLES</span></span>

### <span data-ttu-id="2360c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2360c-108">Example 1</span></span>
```powershell
PS C:\> $VpnServerConfigCertFilePath = Join-Path -Path $basedir -ChildPath "\ScenarioTests\Data\ApplicationGatewayAuthCert.cer"
PS C:\> $listOfCerts = New-Object "System.Collections.Generic.List[String]"
PS C:\> $listOfCerts.Add($VpnServerConfigCertFilePath)
PS C:\> New-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2 -VpnAuthenticationType Certificate -VpnClientRootCertificateFilesList $listOfCerts -VpnClientRevokedCertificateFilesList $listOfCerts -Location "westus"
ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2, OpenVPN}
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

<span data-ttu-id="2360c-109">Il comando precedente creerà una nuova VpnServerConfiguration con VpnAuthenticationType come certificato.</span><span class="sxs-lookup"><span data-stu-id="2360c-109">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

### <span data-ttu-id="2360c-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2360c-110">Example 2</span></span>

<span data-ttu-id="2360c-111">Creare una nuova VpnServerConfiguration per la connettività del sito punto a punto.</span><span class="sxs-lookup"><span data-stu-id="2360c-111">Create a new VpnServerConfiguration for point to site connectivity.</span></span> <span data-ttu-id="2360c-112">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="2360c-112">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzVpnServerConfiguration -AadAudience <String> -AadIssuer <String> -AadTenant <String> -Location 'westus' -Name 'test1config' -ResourceGroupName 'P2SCortexGATesting' -VpnAuthenticationType Certificate -VpnProtocol IkeV2
```

## <span data-ttu-id="2360c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2360c-113">PARAMETERS</span></span>

### <span data-ttu-id="2360c-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="2360c-114">-AadAudience</span></span>
<span data-ttu-id="2360c-115">Gruppo di destinatari AAD per l'autenticazione AAD P2S.</span><span class="sxs-lookup"><span data-stu-id="2360c-115">AAD audience for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="2360c-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="2360c-116">-AadIssuer</span></span>
<span data-ttu-id="2360c-117">Autorità emittente AAD per l'autenticazione AAD P2S.</span><span class="sxs-lookup"><span data-stu-id="2360c-117">AAD issuer for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="2360c-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="2360c-118">-AadTenant</span></span>
<span data-ttu-id="2360c-119">Tenant AAD per l'autenticazione AAD P2S.</span><span class="sxs-lookup"><span data-stu-id="2360c-119">AAD tenant for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="2360c-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2360c-120">-AsJob</span></span>
<span data-ttu-id="2360c-121">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="2360c-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2360c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2360c-122">-DefaultProfile</span></span>
<span data-ttu-id="2360c-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2360c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2360c-124">-Location</span><span class="sxs-lookup"><span data-stu-id="2360c-124">-Location</span></span>
<span data-ttu-id="2360c-125">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2360c-125">The resource location.</span></span>

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

### <span data-ttu-id="2360c-126">-Name</span><span class="sxs-lookup"><span data-stu-id="2360c-126">-Name</span></span>
<span data-ttu-id="2360c-127">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2360c-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2360c-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="2360c-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="2360c-129">Elenco dei percorsi di file RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2360c-129">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="2360c-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="2360c-130">-RadiusServerAddress</span></span>
<span data-ttu-id="2360c-131">Indirizzo server raggio esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="2360c-131">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="2360c-132">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="2360c-132">-RadiusServerList</span></span>
<span data-ttu-id="2360c-133">P2S External multiple radius servers.</span><span class="sxs-lookup"><span data-stu-id="2360c-133">P2S External multiple radius servers.</span></span>

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

### <span data-ttu-id="2360c-134">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="2360c-134">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="2360c-135">Elenco dei percorsi di file RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2360c-135">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="2360c-136">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="2360c-136">-RadiusServerSecret</span></span>
<span data-ttu-id="2360c-137">Segreto server raggio esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="2360c-137">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="2360c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2360c-138">-ResourceGroupName</span></span>
<span data-ttu-id="2360c-139">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2360c-139">The resource group name.</span></span>

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

### <span data-ttu-id="2360c-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="2360c-140">-Tag</span></span>
<span data-ttu-id="2360c-141">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="2360c-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="2360c-142">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="2360c-142">-VpnAuthenticationType</span></span>
<span data-ttu-id="2360c-143">L'elenco dei protocolli di tunneling del client VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="2360c-143">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="2360c-144">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="2360c-144">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="2360c-145">Elenco di criteri IPSec per VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2360c-145">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2360c-146">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="2360c-146">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="2360c-147">Elenco di VpnClientCertificates a cui revocare i percorsi dei file</span><span class="sxs-lookup"><span data-stu-id="2360c-147">A list of VpnClientCertificates to be revoked files' paths</span></span>

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

### <span data-ttu-id="2360c-148">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="2360c-148">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="2360c-149">Elenco di VpnClientRootCertificates da aggiungere ai percorsi dei file</span><span class="sxs-lookup"><span data-stu-id="2360c-149">A list of VpnClientRootCertificates to be added files' paths</span></span>

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

### <span data-ttu-id="2360c-150">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="2360c-150">-VpnProtocol</span></span>
<span data-ttu-id="2360c-151">L'elenco dei protocolli di tunneling del client VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="2360c-151">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="2360c-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2360c-152">-Confirm</span></span>
<span data-ttu-id="2360c-153">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2360c-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2360c-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2360c-154">-WhatIf</span></span>
<span data-ttu-id="2360c-155">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2360c-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2360c-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2360c-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2360c-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2360c-157">CommonParameters</span></span>
<span data-ttu-id="2360c-158">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2360c-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2360c-159">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2360c-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2360c-160">INPUT</span><span class="sxs-lookup"><span data-stu-id="2360c-160">INPUTS</span></span>

### <span data-ttu-id="2360c-161">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="2360c-161">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="2360c-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2360c-162">OUTPUTS</span></span>

### <span data-ttu-id="2360c-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="2360c-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="2360c-164">NOTE</span><span class="sxs-lookup"><span data-stu-id="2360c-164">NOTES</span></span>

## <span data-ttu-id="2360c-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2360c-165">RELATED LINKS</span></span>
