---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: de0806585cee16eed19291766ab29696a9a1b960
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865034"
---
# <span data-ttu-id="21c13-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="21c13-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="21c13-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="21c13-102">SYNOPSIS</span></span>
<span data-ttu-id="21c13-103">Creare un nuovo VpnServerConfiguration per la connettività punto a sito.</span><span class="sxs-lookup"><span data-stu-id="21c13-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="21c13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21c13-104">SYNTAX</span></span>

### <span data-ttu-id="21c13-105">ByVpnServerConfigurationNameByCertificateAuthentication (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="21c13-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21c13-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="21c13-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21c13-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="21c13-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>]
 [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21c13-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21c13-108">DESCRIPTION</span></span>
<span data-ttu-id="21c13-109">Il cmdlet **New-AzVpnServerConfiguration** consente di creare un nuovo VpnServerConfiguration con diversi VpnProtocols, VpnAuthenticationTypes, IpsecPolicies e di impostare i parametri correlati del tipo di autenticazione VPN selezionati in base al requisito del cliente per il punto di connessione al sito.</span><span class="sxs-lookup"><span data-stu-id="21c13-109">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="21c13-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21c13-110">EXAMPLES</span></span>

### <span data-ttu-id="21c13-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="21c13-111">Example 1</span></span>
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

<span data-ttu-id="21c13-112">Il comando precedente creerà un nuovo VpnServerConfiguration con VpnAuthenticationType come certificato.</span><span class="sxs-lookup"><span data-stu-id="21c13-112">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

## <span data-ttu-id="21c13-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="21c13-113">PARAMETERS</span></span>

### <span data-ttu-id="21c13-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="21c13-114">-AadAudience</span></span>
<span data-ttu-id="21c13-115">Utenti AAD per l'autenticazione P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="21c13-115">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="21c13-116">-AadIssuer</span></span>
<span data-ttu-id="21c13-117">Emittente AAD per l'autenticazione P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="21c13-117">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="21c13-118">-AadTenant</span></span>
<span data-ttu-id="21c13-119">Tenant per l'autenticazione AAD di P2S.</span><span class="sxs-lookup"><span data-stu-id="21c13-119">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21c13-120">-AsJob</span></span>
<span data-ttu-id="21c13-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="21c13-121">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21c13-122">-DefaultProfile</span></span>
<span data-ttu-id="21c13-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="21c13-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="21c13-124">-Location</span></span>
<span data-ttu-id="21c13-125">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="21c13-125">The resource location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="21c13-126">-Name</span></span>
<span data-ttu-id="21c13-127">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="21c13-127">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="21c13-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="21c13-129">Elenco dei percorsi di file di RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="21c13-129">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="21c13-130">-RadiusServerAddress</span></span>
<span data-ttu-id="21c13-131">Indirizzo del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="21c13-131">P2S External Radius server address.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-132">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="21c13-132">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="21c13-133">Elenco dei percorsi di file di RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="21c13-133">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-134">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="21c13-134">-RadiusServerSecret</span></span>
<span data-ttu-id="21c13-135">Segreto del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="21c13-135">P2S External Radius server secret.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21c13-136">-ResourceGroupName</span></span>
<span data-ttu-id="21c13-137">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="21c13-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="21c13-138">-Tag</span></span>
<span data-ttu-id="21c13-139">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="21c13-139">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-140">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="21c13-140">-VpnAuthenticationType</span></span>
<span data-ttu-id="21c13-141">Elenco dei protocolli di tunneling client VPN di P2S.</span><span class="sxs-lookup"><span data-stu-id="21c13-141">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Certificate, Radius, AAD

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-142">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="21c13-142">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="21c13-143">Elenco dei criteri IPSec per VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="21c13-143">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-144">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="21c13-144">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="21c13-145">Elenco dei percorsi di file revocati da VpnClientCertificates</span><span class="sxs-lookup"><span data-stu-id="21c13-145">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-146">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="21c13-146">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="21c13-147">Elenco dei percorsi di VpnClientRootCertificates da aggiungere ai file</span><span class="sxs-lookup"><span data-stu-id="21c13-147">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-148">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="21c13-148">-VpnProtocol</span></span>
<span data-ttu-id="21c13-149">Elenco dei protocolli di tunneling client VPN di P2S.</span><span class="sxs-lookup"><span data-stu-id="21c13-149">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="21c13-150">-Confirm</span></span>
<span data-ttu-id="21c13-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21c13-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21c13-152">-WhatIf</span></span>
<span data-ttu-id="21c13-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21c13-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21c13-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21c13-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c13-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21c13-155">CommonParameters</span></span>
<span data-ttu-id="21c13-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21c13-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21c13-157">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21c13-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21c13-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="21c13-158">INPUTS</span></span>

### <span data-ttu-id="21c13-159">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="21c13-159">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="21c13-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21c13-160">OUTPUTS</span></span>

### <span data-ttu-id="21c13-161">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="21c13-161">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="21c13-162">Note</span><span class="sxs-lookup"><span data-stu-id="21c13-162">NOTES</span></span>

## <span data-ttu-id="21c13-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21c13-163">RELATED LINKS</span></span>
