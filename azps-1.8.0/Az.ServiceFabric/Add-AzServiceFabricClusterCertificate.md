---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: bf96b4a21e12e41ce067d669b50c05831a162a8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677083"
---
# <span data-ttu-id="622c1-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="622c1-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="622c1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="622c1-102">SYNOPSIS</span></span>
<span data-ttu-id="622c1-103">Aggiungere un certificato di cluster secondario al cluster.</span><span class="sxs-lookup"><span data-stu-id="622c1-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="622c1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="622c1-104">SYNTAX</span></span>

### <span data-ttu-id="622c1-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="622c1-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="622c1-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="622c1-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="622c1-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="622c1-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="622c1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="622c1-108">DESCRIPTION</span></span>
<span data-ttu-id="622c1-109">Usare **Add-AzServiceFabricClusterCertificate** per aggiungere un certificato di cluster secondario, da un Vault di una chiave di Azure esistente o creare un nuovo Vault di chiave di Azure usando un certificato esistente fornito o da un nuovo certificato autofirmato creato.</span><span class="sxs-lookup"><span data-stu-id="622c1-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="622c1-110">Verrà eseguito l'override del cluster secondario, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="622c1-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="622c1-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="622c1-111">EXAMPLES</span></span>

### <span data-ttu-id="622c1-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="622c1-112">Example 1</span></span>
```
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="622c1-113">Questo comando aggiungerà un certificato nell'archivio di chiavi di Azure esistente come certificato di cluster secondario.</span><span class="sxs-lookup"><span data-stu-id="622c1-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="622c1-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="622c1-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="622c1-115">Questo comando creerà un certificato autofirmato nel Vault di Azure Key e aggiornerà il cluster per usarlo come certificato di cluster secondario.</span><span class="sxs-lookup"><span data-stu-id="622c1-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="622c1-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="622c1-116">PARAMETERS</span></span>

### <span data-ttu-id="622c1-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="622c1-117">-CertificateCommonName</span></span>
<span data-ttu-id="622c1-118">Nome comune del certificato</span><span class="sxs-lookup"><span data-stu-id="622c1-118">Certificate common name</span></span>

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

### <span data-ttu-id="622c1-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="622c1-119">-CertificateFile</span></span>
<span data-ttu-id="622c1-120">Percorso del file del certificato esistente.</span><span class="sxs-lookup"><span data-stu-id="622c1-120">The existing certificate file path.</span></span>

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

### <span data-ttu-id="622c1-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="622c1-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="622c1-122">Identificazione personale dell'autorità di certificazione, separate da virgole se più di una</span><span class="sxs-lookup"><span data-stu-id="622c1-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="622c1-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="622c1-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="622c1-124">Cartella del nuovo certificato da creare.</span><span class="sxs-lookup"><span data-stu-id="622c1-124">The folder of the new certificate to be created.</span></span>

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

### <span data-ttu-id="622c1-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="622c1-125">-CertificatePassword</span></span>
<span data-ttu-id="622c1-126">La password del file di certificato.</span><span class="sxs-lookup"><span data-stu-id="622c1-126">The password of the certificate file.</span></span>

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

### <span data-ttu-id="622c1-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="622c1-127">-CertificateSubjectName</span></span>
<span data-ttu-id="622c1-128">Nome DNS del certificato da creare.</span><span class="sxs-lookup"><span data-stu-id="622c1-128">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="622c1-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="622c1-129">-DefaultProfile</span></span>
<span data-ttu-id="622c1-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="622c1-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="622c1-131">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="622c1-131">-KeyVaultName</span></span>
<span data-ttu-id="622c1-132">Nome del Vault della chiave di Azure.</span><span class="sxs-lookup"><span data-stu-id="622c1-132">Azure key vault name.</span></span>

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

### <span data-ttu-id="622c1-133">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="622c1-133">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="622c1-134">Nome del gruppo di risorse di Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="622c1-134">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="622c1-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="622c1-135">-Name</span></span>
<span data-ttu-id="622c1-136">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="622c1-136">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="622c1-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="622c1-137">-ResourceGroupName</span></span>
<span data-ttu-id="622c1-138">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="622c1-138">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="622c1-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="622c1-139">-SecretIdentifier</span></span>
<span data-ttu-id="622c1-140">URL segreto del Vault Key di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="622c1-140">The existing Azure key vault secret Url.</span></span>

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

### <span data-ttu-id="622c1-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="622c1-141">-Confirm</span></span>
<span data-ttu-id="622c1-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="622c1-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="622c1-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="622c1-143">-WhatIf</span></span>
<span data-ttu-id="622c1-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="622c1-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="622c1-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="622c1-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="622c1-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="622c1-146">CommonParameters</span></span>
<span data-ttu-id="622c1-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="622c1-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="622c1-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="622c1-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="622c1-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="622c1-149">INPUTS</span></span>

### <span data-ttu-id="622c1-150">System. String</span><span class="sxs-lookup"><span data-stu-id="622c1-150">System.String</span></span>

### <span data-ttu-id="622c1-151">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="622c1-151">System.Security.SecureString</span></span>

## <span data-ttu-id="622c1-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="622c1-152">OUTPUTS</span></span>

### <span data-ttu-id="622c1-153">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="622c1-153">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="622c1-154">Note</span><span class="sxs-lookup"><span data-stu-id="622c1-154">NOTES</span></span>

## <span data-ttu-id="622c1-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="622c1-155">RELATED LINKS</span></span>

[<span data-ttu-id="622c1-156">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="622c1-156">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="622c1-157">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="622c1-157">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)

[<span data-ttu-id="622c1-158">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="622c1-158">Add-AzServiceFabricApplicationCertificate</span></span>](./Add-AzServiceFabricApplicationCertificate.md)
