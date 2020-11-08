---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: 14f43ab66800969eb46554de898525ce8d687f5b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021169"
---
# <span data-ttu-id="372b9-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="372b9-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="372b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="372b9-102">SYNOPSIS</span></span>
<span data-ttu-id="372b9-103">Aggiorna un VpnServerConfiguration esistente.</span><span class="sxs-lookup"><span data-stu-id="372b9-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="372b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="372b9-104">SYNTAX</span></span>

### <span data-ttu-id="372b9-105">ByVpnServerConfigurationNameByCertificateAuthentication (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="372b9-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="372b9-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="372b9-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="372b9-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="372b9-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="372b9-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="372b9-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="372b9-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="372b9-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="372b9-110">ByVpnServerConfigurationObjectByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="372b9-110">ByVpnServerConfigurationObjectByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="372b9-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="372b9-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="372b9-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="372b9-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="372b9-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="372b9-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="372b9-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="372b9-114">DESCRIPTION</span></span>
<span data-ttu-id="372b9-115">Il cmdlet **Update-AzVpnServerConfiguration** consente di aggiornare il VpnServerConfiguration esistente con diversi VpnProtocols, VpnAuthenticationTypes, IpsecPolicies e di impostare i parametri correlati per il tipo di autenticazione VPN selezionati in base al requisito del cliente per la connettività punto a sito.</span><span class="sxs-lookup"><span data-stu-id="372b9-115">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="372b9-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="372b9-116">EXAMPLES</span></span>

### <span data-ttu-id="372b9-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="372b9-117">Example 1</span></span>
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

<span data-ttu-id="372b9-118">Il comando precedente aggiornerà un VpnServerConfiguration esistente con VpnProtocol come IkeV2.</span><span class="sxs-lookup"><span data-stu-id="372b9-118">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="372b9-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="372b9-119">PARAMETERS</span></span>

### <span data-ttu-id="372b9-120">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="372b9-120">-AadAudience</span></span>
<span data-ttu-id="372b9-121">Utenti AAD per l'autenticazione P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="372b9-121">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="372b9-122">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="372b9-122">-AadIssuer</span></span>
<span data-ttu-id="372b9-123">Emittente AAD per l'autenticazione P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="372b9-123">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="372b9-124">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="372b9-124">-AadTenant</span></span>
<span data-ttu-id="372b9-125">Tenant per l'autenticazione AAD di P2S.</span><span class="sxs-lookup"><span data-stu-id="372b9-125">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="372b9-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="372b9-126">-AsJob</span></span>
<span data-ttu-id="372b9-127">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="372b9-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="372b9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="372b9-128">-DefaultProfile</span></span>
<span data-ttu-id="372b9-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="372b9-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="372b9-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="372b9-130">-InputObject</span></span>
<span data-ttu-id="372b9-131">Oggetto di configurazione del server VPN da modificare</span><span class="sxs-lookup"><span data-stu-id="372b9-131">The vpn server configuration object to be modified</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationObjectByAadAuthentication
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="372b9-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="372b9-132">-Name</span></span>
<span data-ttu-id="372b9-133">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="372b9-133">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="372b9-134">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="372b9-134">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="372b9-135">Elenco dei percorsi di file di RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="372b9-135">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="372b9-136">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="372b9-136">-RadiusServerAddress</span></span>
<span data-ttu-id="372b9-137">Indirizzo del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="372b9-137">P2S External Radius server address.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="372b9-138">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="372b9-138">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="372b9-139">Elenco dei percorsi di file di RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="372b9-139">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="372b9-140">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="372b9-140">-RadiusServerSecret</span></span>
<span data-ttu-id="372b9-141">Segreto del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="372b9-141">P2S External Radius server secret.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="372b9-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="372b9-142">-ResourceGroupName</span></span>
<span data-ttu-id="372b9-143">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="372b9-143">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="372b9-144">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="372b9-144">-ResourceId</span></span>
<span data-ttu-id="372b9-145">ID risorsa Azure per la configurazione del server VPN.</span><span class="sxs-lookup"><span data-stu-id="372b9-145">The Azure resource ID for the vpn server configuration.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationResourceIdByCertificateAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="372b9-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="372b9-146">-Tag</span></span>
<span data-ttu-id="372b9-147">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="372b9-147">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="372b9-148">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="372b9-148">-VpnAuthenticationType</span></span>
<span data-ttu-id="372b9-149">Elenco dei protocolli di tunneling client VPN di P2S.</span><span class="sxs-lookup"><span data-stu-id="372b9-149">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="372b9-150">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="372b9-150">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="372b9-151">Elenco dei criteri IPSec per VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="372b9-151">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="372b9-152">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="372b9-152">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="372b9-153">Elenco dei percorsi di file revocati da VpnClientCertificates</span><span class="sxs-lookup"><span data-stu-id="372b9-153">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="372b9-154">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="372b9-154">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="372b9-155">Elenco dei percorsi di VpnClientRootCertificates da aggiungere ai file</span><span class="sxs-lookup"><span data-stu-id="372b9-155">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="372b9-156">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="372b9-156">-VpnProtocol</span></span>
<span data-ttu-id="372b9-157">Elenco dei protocolli di tunneling client VPN di P2S.</span><span class="sxs-lookup"><span data-stu-id="372b9-157">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="372b9-158">-Confermare</span><span class="sxs-lookup"><span data-stu-id="372b9-158">-Confirm</span></span>
<span data-ttu-id="372b9-159">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="372b9-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="372b9-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="372b9-160">-WhatIf</span></span>
<span data-ttu-id="372b9-161">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="372b9-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="372b9-162">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="372b9-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="372b9-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="372b9-163">CommonParameters</span></span>
<span data-ttu-id="372b9-164">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="372b9-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="372b9-165">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="372b9-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="372b9-166">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="372b9-166">INPUTS</span></span>

### <span data-ttu-id="372b9-167">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="372b9-167">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="372b9-168">System. String Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="372b9-168">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="372b9-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="372b9-169">OUTPUTS</span></span>

### <span data-ttu-id="372b9-170">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="372b9-170">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="372b9-171">Note</span><span class="sxs-lookup"><span data-stu-id="372b9-171">NOTES</span></span>

## <span data-ttu-id="372b9-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="372b9-172">RELATED LINKS</span></span>
