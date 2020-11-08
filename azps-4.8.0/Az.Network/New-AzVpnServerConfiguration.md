---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: 10feda31a97582ef56300b570ce2768c3ea0e277
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192758"
---
# <span data-ttu-id="17a4a-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="17a4a-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="17a4a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="17a4a-102">SYNOPSIS</span></span>
<span data-ttu-id="17a4a-103">Creare un nuovo VpnServerConfiguration per la connettività punto a sito.</span><span class="sxs-lookup"><span data-stu-id="17a4a-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="17a4a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="17a4a-104">SYNTAX</span></span>

### <span data-ttu-id="17a4a-105">ByVpnServerConfigurationNameByCertificateAuthentication (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="17a4a-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="17a4a-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="17a4a-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17a4a-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="17a4a-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>]
 [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17a4a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17a4a-108">DESCRIPTION</span></span>
<span data-ttu-id="17a4a-109">Il cmdlet **New-AzVpnServerConfiguration** consente di creare un nuovo VpnServerConfiguration con diversi VpnProtocols, VpnAuthenticationTypes, IpsecPolicies e di impostare i parametri correlati del tipo di autenticazione VPN selezionati in base al requisito del cliente per il punto di connessione al sito.</span><span class="sxs-lookup"><span data-stu-id="17a4a-109">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="17a4a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="17a4a-110">EXAMPLES</span></span>

### <span data-ttu-id="17a4a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="17a4a-111">Example 1</span></span>
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

<span data-ttu-id="17a4a-112">Il comando precedente creerà un nuovo VpnServerConfiguration con VpnAuthenticationType come certificato.</span><span class="sxs-lookup"><span data-stu-id="17a4a-112">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

### <span data-ttu-id="17a4a-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="17a4a-113">Example 2</span></span>

<span data-ttu-id="17a4a-114">Creare un nuovo VpnServerConfiguration per la connettività punto a sito.</span><span class="sxs-lookup"><span data-stu-id="17a4a-114">Create a new VpnServerConfiguration for point to site connectivity.</span></span> <span data-ttu-id="17a4a-115">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="17a4a-115">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnServerConfiguration -AadAudience <String> -AadIssuer <String> -AadTenant <String> -Location 'westus' -Name 'test1config' -ResourceGroupName 'P2SCortexGATesting' -VpnAuthenticationType Certificate -VpnProtocol IkeV2
```

## <span data-ttu-id="17a4a-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="17a4a-116">PARAMETERS</span></span>

### <span data-ttu-id="17a4a-117">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="17a4a-117">-AadAudience</span></span>
<span data-ttu-id="17a4a-118">Utenti AAD per l'autenticazione P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="17a4a-118">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a4a-119">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="17a4a-119">-AadIssuer</span></span>
<span data-ttu-id="17a4a-120">Emittente AAD per l'autenticazione P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="17a4a-120">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a4a-121">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="17a4a-121">-AadTenant</span></span>
<span data-ttu-id="17a4a-122">Tenant per l'autenticazione AAD di P2S.</span><span class="sxs-lookup"><span data-stu-id="17a4a-122">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a4a-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17a4a-123">-AsJob</span></span>
<span data-ttu-id="17a4a-124">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="17a4a-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="17a4a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17a4a-125">-DefaultProfile</span></span>
<span data-ttu-id="17a4a-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="17a4a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17a4a-127">-Posizione</span><span class="sxs-lookup"><span data-stu-id="17a4a-127">-Location</span></span>
<span data-ttu-id="17a4a-128">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="17a4a-128">The resource location.</span></span>

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

### <span data-ttu-id="17a4a-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="17a4a-129">-Name</span></span>
<span data-ttu-id="17a4a-130">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="17a4a-130">The resource name.</span></span>

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

### <span data-ttu-id="17a4a-131">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="17a4a-131">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="17a4a-132">Elenco dei percorsi di file di RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="17a4a-132">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a4a-133">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="17a4a-133">-RadiusServerAddress</span></span>
<span data-ttu-id="17a4a-134">Indirizzo del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="17a4a-134">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a4a-135">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="17a4a-135">-RadiusServerList</span></span>
<span data-ttu-id="17a4a-136">P2S più server RADIUS esterni.</span><span class="sxs-lookup"><span data-stu-id="17a4a-136">P2S External multiple radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a4a-137">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="17a4a-137">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="17a4a-138">Elenco dei percorsi di file di RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="17a4a-138">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a4a-139">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="17a4a-139">-RadiusServerSecret</span></span>
<span data-ttu-id="17a4a-140">Segreto del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="17a4a-140">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a4a-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17a4a-141">-ResourceGroupName</span></span>
<span data-ttu-id="17a4a-142">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="17a4a-142">The resource group name.</span></span>

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

### <span data-ttu-id="17a4a-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="17a4a-143">-Tag</span></span>
<span data-ttu-id="17a4a-144">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="17a4a-144">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="17a4a-145">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="17a4a-145">-VpnAuthenticationType</span></span>
<span data-ttu-id="17a4a-146">Elenco dei protocolli di tunneling client VPN di P2S.</span><span class="sxs-lookup"><span data-stu-id="17a4a-146">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="17a4a-147">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="17a4a-147">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="17a4a-148">Elenco dei criteri IPSec per VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="17a4a-148">A list of IPSec policies for VpnServerConfiguration.</span></span>

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

### <span data-ttu-id="17a4a-149">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="17a4a-149">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="17a4a-150">Elenco dei percorsi di file revocati da VpnClientCertificates</span><span class="sxs-lookup"><span data-stu-id="17a4a-150">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a4a-151">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="17a4a-151">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="17a4a-152">Elenco dei percorsi di VpnClientRootCertificates da aggiungere ai file</span><span class="sxs-lookup"><span data-stu-id="17a4a-152">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17a4a-153">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="17a4a-153">-VpnProtocol</span></span>
<span data-ttu-id="17a4a-154">Elenco dei protocolli di tunneling client VPN di P2S.</span><span class="sxs-lookup"><span data-stu-id="17a4a-154">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="17a4a-155">-Confermare</span><span class="sxs-lookup"><span data-stu-id="17a4a-155">-Confirm</span></span>
<span data-ttu-id="17a4a-156">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17a4a-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17a4a-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17a4a-157">-WhatIf</span></span>
<span data-ttu-id="17a4a-158">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="17a4a-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17a4a-159">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="17a4a-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17a4a-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17a4a-160">CommonParameters</span></span>
<span data-ttu-id="17a4a-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17a4a-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17a4a-162">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17a4a-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17a4a-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="17a4a-163">INPUTS</span></span>

### <span data-ttu-id="17a4a-164">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="17a4a-164">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="17a4a-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="17a4a-165">OUTPUTS</span></span>

### <span data-ttu-id="17a4a-166">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="17a4a-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="17a4a-167">Note</span><span class="sxs-lookup"><span data-stu-id="17a4a-167">NOTES</span></span>

## <span data-ttu-id="17a4a-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="17a4a-168">RELATED LINKS</span></span>
