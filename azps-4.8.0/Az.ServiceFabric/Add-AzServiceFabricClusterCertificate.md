---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: c3ddf8373b467b3f7821d9470f67f2b864201949
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031052"
---
# <span data-ttu-id="240d0-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="240d0-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="240d0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="240d0-102">SYNOPSIS</span></span>
<span data-ttu-id="240d0-103">Aggiungere un certificato di cluster secondario al cluster.</span><span class="sxs-lookup"><span data-stu-id="240d0-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="240d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="240d0-104">SYNTAX</span></span>

### <span data-ttu-id="240d0-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="240d0-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-Thumbprint <String>] [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="240d0-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="240d0-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="240d0-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="240d0-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="240d0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="240d0-108">DESCRIPTION</span></span>
<span data-ttu-id="240d0-109">Usare **Add-AzServiceFabricClusterCertificate** per aggiungere un certificato di cluster secondario, da un Vault di una chiave di Azure esistente o creare un nuovo Vault di chiave di Azure usando un certificato esistente fornito o da un nuovo certificato autofirmato creato.</span><span class="sxs-lookup"><span data-stu-id="240d0-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="240d0-110">Verrà eseguito l'override del cluster secondario, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="240d0-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="240d0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="240d0-111">EXAMPLES</span></span>

### <span data-ttu-id="240d0-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="240d0-112">Example 1</span></span>
```powershell
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="240d0-113">Questo comando aggiungerà un certificato nell'archivio di chiavi di Azure esistente come certificato di cluster secondario.</span><span class="sxs-lookup"><span data-stu-id="240d0-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="240d0-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="240d0-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="240d0-115">Questo comando creerà un certificato autofirmato nel Vault di Azure Key e aggiornerà il cluster per usarlo come certificato di cluster secondario.</span><span class="sxs-lookup"><span data-stu-id="240d0-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="240d0-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="240d0-116">PARAMETERS</span></span>

### <span data-ttu-id="240d0-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="240d0-117">-CertificateCommonName</span></span>
<span data-ttu-id="240d0-118">Nome comune del certificato</span><span class="sxs-lookup"><span data-stu-id="240d0-118">Certificate common name</span></span>

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

### <span data-ttu-id="240d0-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="240d0-119">-CertificateFile</span></span>
<span data-ttu-id="240d0-120">Percorso del certificato esistente</span><span class="sxs-lookup"><span data-stu-id="240d0-120">The path to the existing certificate</span></span>

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

### <span data-ttu-id="240d0-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="240d0-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="240d0-122">Identificazione personale dell'autorità di certificazione, separate da virgole se più di una</span><span class="sxs-lookup"><span data-stu-id="240d0-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="240d0-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="240d0-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="240d0-124">Cartella in cui deve essere scaricato il nuovo certificato.</span><span class="sxs-lookup"><span data-stu-id="240d0-124">The folder where the new certificate needs to be downloaded.</span></span>

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

### <span data-ttu-id="240d0-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="240d0-125">-CertificatePassword</span></span>
<span data-ttu-id="240d0-126">Password del certificato</span><span class="sxs-lookup"><span data-stu-id="240d0-126">The password of the certificate</span></span>

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

### <span data-ttu-id="240d0-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="240d0-127">-CertificateSubjectName</span></span>
<span data-ttu-id="240d0-128">Nome oggetto del certificato</span><span class="sxs-lookup"><span data-stu-id="240d0-128">The subject name of the certificate</span></span>

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

### <span data-ttu-id="240d0-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="240d0-129">-DefaultProfile</span></span>
<span data-ttu-id="240d0-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="240d0-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="240d0-131">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="240d0-131">-KeyVaultName</span></span>
<span data-ttu-id="240d0-132">Nome del Vault di Azure Key, se non assegnato, verrà impostato come predefinito nel nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="240d0-132">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="240d0-133">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="240d0-133">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="240d0-134">Nome del gruppo di risorse di Azure Key Vault, se non assegnato, verrà impostato come nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="240d0-134">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

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

### <span data-ttu-id="240d0-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="240d0-135">-Name</span></span>
<span data-ttu-id="240d0-136">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="240d0-136">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="240d0-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="240d0-137">-ResourceGroupName</span></span>
<span data-ttu-id="240d0-138">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="240d0-138">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="240d0-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="240d0-139">-SecretIdentifier</span></span>
<span data-ttu-id="240d0-140">URL segreto del Vault Key di Azure esistente, ad esempio ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="240d0-140">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="240d0-141">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="240d0-141">-Thumbprint</span></span>
<span data-ttu-id="240d0-142">Identificazione personale del certificato correspoinding in SecretIdentifier.</span><span class="sxs-lookup"><span data-stu-id="240d0-142">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="240d0-143">Usa questa operazione se il certificato non viene gestito come volta chiave, il certificato verrà archiviato solo come segreto e il cmdlet non potrà recuperare l'identificazione personale.</span><span class="sxs-lookup"><span data-stu-id="240d0-143">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

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

### <span data-ttu-id="240d0-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="240d0-144">-Confirm</span></span>
<span data-ttu-id="240d0-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="240d0-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="240d0-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="240d0-146">-WhatIf</span></span>
<span data-ttu-id="240d0-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="240d0-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="240d0-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="240d0-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="240d0-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="240d0-149">CommonParameters</span></span>
<span data-ttu-id="240d0-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="240d0-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="240d0-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="240d0-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="240d0-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="240d0-152">INPUTS</span></span>

### <span data-ttu-id="240d0-153">System. String</span><span class="sxs-lookup"><span data-stu-id="240d0-153">System.String</span></span>

### <span data-ttu-id="240d0-154">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="240d0-154">System.Security.SecureString</span></span>

## <span data-ttu-id="240d0-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="240d0-155">OUTPUTS</span></span>

### <span data-ttu-id="240d0-156">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="240d0-156">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="240d0-157">Note</span><span class="sxs-lookup"><span data-stu-id="240d0-157">NOTES</span></span>

## <span data-ttu-id="240d0-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="240d0-158">RELATED LINKS</span></span>

[<span data-ttu-id="240d0-159">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="240d0-159">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="240d0-160">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="240d0-160">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
