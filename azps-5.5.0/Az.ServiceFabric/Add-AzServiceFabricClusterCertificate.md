---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: c3ddf8373b467b3f7821d9470f67f2b864201949
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178575"
---
# <span data-ttu-id="496ba-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="496ba-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="496ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="496ba-102">SYNOPSIS</span></span>
<span data-ttu-id="496ba-103">Aggiungere un certificato cluster secondario al cluster.</span><span class="sxs-lookup"><span data-stu-id="496ba-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="496ba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="496ba-104">SYNTAX</span></span>

### <span data-ttu-id="496ba-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="496ba-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-Thumbprint <String>] [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="496ba-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="496ba-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="496ba-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="496ba-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="496ba-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="496ba-108">DESCRIPTION</span></span>
<span data-ttu-id="496ba-109">Usare **Add-AzServiceFabricClusterCertificate** per aggiungere un certificato cluster secondario, da un vault della chiave di Azure esistente o creando un nuovo vault delle chiavi di Azure con un certificato esistente fornito o da un nuovo certificato autofirmato creato.</span><span class="sxs-lookup"><span data-stu-id="496ba-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="496ba-110">L'eventuale cluster secondario verrà sovrascritto.</span><span class="sxs-lookup"><span data-stu-id="496ba-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="496ba-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="496ba-111">EXAMPLES</span></span>

### <span data-ttu-id="496ba-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="496ba-112">Example 1</span></span>
```powershell
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="496ba-113">Questo comando aggiungerà un certificato nell'insieme di credenziali di Azure esistente come certificato cluster secondario.</span><span class="sxs-lookup"><span data-stu-id="496ba-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="496ba-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="496ba-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="496ba-115">Questo comando crea un certificato autofirmato nel vault della chiave di Azure e aggiorna il cluster per usarlo come certificato cluster secondario.</span><span class="sxs-lookup"><span data-stu-id="496ba-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="496ba-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="496ba-116">PARAMETERS</span></span>

### <span data-ttu-id="496ba-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="496ba-117">-CertificateCommonName</span></span>
<span data-ttu-id="496ba-118">Nome comune certificato</span><span class="sxs-lookup"><span data-stu-id="496ba-118">Certificate common name</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByExistingPfxAndVaultName
Aliases: CertCommonName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496ba-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="496ba-119">-CertificateFile</span></span>
<span data-ttu-id="496ba-120">Percorso del certificato esistente</span><span class="sxs-lookup"><span data-stu-id="496ba-120">The path to the existing certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: Source

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="496ba-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="496ba-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="496ba-122">Pollice dell'autorità di certificazione emittente, separata da virgole se più di una</span><span class="sxs-lookup"><span data-stu-id="496ba-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByExistingPfxAndVaultName
Aliases: CertIssuerThumbprint

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="496ba-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="496ba-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="496ba-124">La cartella in cui deve essere scaricato il nuovo certificato.</span><span class="sxs-lookup"><span data-stu-id="496ba-124">The folder where the new certificate needs to be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="496ba-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="496ba-125">-CertificatePassword</span></span>
<span data-ttu-id="496ba-126">Password del certificato</span><span class="sxs-lookup"><span data-stu-id="496ba-126">The password of the certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="496ba-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="496ba-127">-CertificateSubjectName</span></span>
<span data-ttu-id="496ba-128">Il nome dell'oggetto del certificato</span><span class="sxs-lookup"><span data-stu-id="496ba-128">The subject name of the certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Subject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="496ba-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="496ba-129">-DefaultProfile</span></span>
<span data-ttu-id="496ba-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="496ba-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="496ba-131">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="496ba-131">-KeyVaultName</span></span>
<span data-ttu-id="496ba-132">Nome del vault della chiave di Azure, se non è assegnato verrà utilizzato per impostazione predefinita con il nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="496ba-132">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="496ba-133">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="496ba-133">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="496ba-134">Nome del gruppo di risorse del vault della chiave di Azure, se non è assegnato verrà utilizzato per impostazione predefinita sul nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="496ba-134">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: KeyVaultResouceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="496ba-135">-Name</span><span class="sxs-lookup"><span data-stu-id="496ba-135">-Name</span></span>
<span data-ttu-id="496ba-136">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="496ba-136">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="496ba-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="496ba-137">-ResourceGroupName</span></span>
<span data-ttu-id="496ba-138">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="496ba-138">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="496ba-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="496ba-139">-SecretIdentifier</span></span>
<span data-ttu-id="496ba-140">L'URL segreto vault della chiave di Azure esistente, ad esempio ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="496ba-140">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="496ba-141">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="496ba-141">-Thumbprint</span></span>
<span data-ttu-id="496ba-142">L'impronta digitale del certificato correspoinding al SecretIdentifier.</span><span class="sxs-lookup"><span data-stu-id="496ba-142">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="496ba-143">Usare questa opzione se il certificato non viene gestito come vault della chiave con un solo certificato archiviato come segreto e il cmdlet non è in grado di individuare nuovamente l'immagine thumbprint.</span><span class="sxs-lookup"><span data-stu-id="496ba-143">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="496ba-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="496ba-144">-Confirm</span></span>
<span data-ttu-id="496ba-145">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="496ba-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="496ba-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="496ba-146">-WhatIf</span></span>
<span data-ttu-id="496ba-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="496ba-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="496ba-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="496ba-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="496ba-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="496ba-149">CommonParameters</span></span>
<span data-ttu-id="496ba-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="496ba-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="496ba-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="496ba-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="496ba-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="496ba-152">INPUTS</span></span>

### <span data-ttu-id="496ba-153">System.String</span><span class="sxs-lookup"><span data-stu-id="496ba-153">System.String</span></span>

### <span data-ttu-id="496ba-154">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="496ba-154">System.Security.SecureString</span></span>

## <span data-ttu-id="496ba-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="496ba-155">OUTPUTS</span></span>

### <span data-ttu-id="496ba-156">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="496ba-156">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="496ba-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="496ba-157">NOTES</span></span>

## <span data-ttu-id="496ba-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="496ba-158">RELATED LINKS</span></span>

[<span data-ttu-id="496ba-159">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="496ba-159">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="496ba-160">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="496ba-160">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
