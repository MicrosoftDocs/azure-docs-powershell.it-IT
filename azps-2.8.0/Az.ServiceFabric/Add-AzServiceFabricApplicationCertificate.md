---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricapplicationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
ms.openlocfilehash: 62298a5747a8bb5b4f01458cac611f5e86869ee7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856121"
---
# <span data-ttu-id="f9b79-101">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="f9b79-101">Add-AzServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="f9b79-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f9b79-102">SYNOPSIS</span></span>
<span data-ttu-id="f9b79-103">Aggiungere un nuovo certificato ai set di scale della macchina virtuale che compongono il cluster.</span><span class="sxs-lookup"><span data-stu-id="f9b79-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="f9b79-104">Il certificato è destinato a essere usato come certificato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f9b79-104">The certificate is intended to be used as an application certificate.</span></span>

## <span data-ttu-id="f9b79-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9b79-105">SYNTAX</span></span>

### <span data-ttu-id="f9b79-106">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="f9b79-106">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9b79-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="f9b79-107">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9b79-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="f9b79-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9b79-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9b79-109">DESCRIPTION</span></span>
<span data-ttu-id="f9b79-110">Usare **Add-AzServiceFabricApplicationCertificate** per installare un certificato in tutti i nodi del cluster.</span><span class="sxs-lookup"><span data-stu-id="f9b79-110">Use **Add-AzServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="f9b79-111">Puoi specificare un certificato che hai già o avere il sistema per generarne uno nuovo e caricarlo in un Vault di chiave di Azure nuovo o esistente.</span><span class="sxs-lookup"><span data-stu-id="f9b79-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="f9b79-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9b79-112">EXAMPLES</span></span>

### <span data-ttu-id="f9b79-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f9b79-113">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="f9b79-114">Questo comando aggiungerà un certificato dall'archivio di chiavi di Azure esistente a tutti i tipi di nodo del cluster.</span><span class="sxs-lookup"><span data-stu-id="f9b79-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="f9b79-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f9b79-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="f9b79-116">Questo comando creerà un certificato autofirmato nel Vault di chiave di Azure con il nome del gruppo di risorse del Vault chiave e il nome della chiave del Vault, viene installato in tutti i tipi di nodo del cluster e Scarica il certificato nella cartella "c:\test".</span><span class="sxs-lookup"><span data-stu-id="f9b79-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="f9b79-117">Il nome del certificato scaricato è uguale al nome del certificato di volta chiave.</span><span class="sxs-lookup"><span data-stu-id="f9b79-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="f9b79-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f9b79-118">PARAMETERS</span></span>

### <span data-ttu-id="f9b79-119">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="f9b79-119">-CertificateCommonName</span></span>
<span data-ttu-id="f9b79-120">Nome comune del certificato</span><span class="sxs-lookup"><span data-stu-id="f9b79-120">Certificate common name</span></span>

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

### <span data-ttu-id="f9b79-121">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="f9b79-121">-CertificateFile</span></span>
<span data-ttu-id="f9b79-122">Percorso del certificato esistente</span><span class="sxs-lookup"><span data-stu-id="f9b79-122">The path to the existing certificate</span></span>

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

### <span data-ttu-id="f9b79-123">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="f9b79-123">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="f9b79-124">Identificazione personale dell'autorità di certificazione, separate da virgole se più di una</span><span class="sxs-lookup"><span data-stu-id="f9b79-124">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="f9b79-125">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="f9b79-125">-CertificateOutputFolder</span></span>
<span data-ttu-id="f9b79-126">Cartella in cui deve essere scaricato il nuovo certificato.</span><span class="sxs-lookup"><span data-stu-id="f9b79-126">The folder where the new certificate needs to be downloaded.</span></span>

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

### <span data-ttu-id="f9b79-127">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="f9b79-127">-CertificatePassword</span></span>
<span data-ttu-id="f9b79-128">Password del certificato</span><span class="sxs-lookup"><span data-stu-id="f9b79-128">The password of the certificate</span></span>

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

### <span data-ttu-id="f9b79-129">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="f9b79-129">-CertificateSubjectName</span></span>
<span data-ttu-id="f9b79-130">Nome oggetto del certificato</span><span class="sxs-lookup"><span data-stu-id="f9b79-130">The subject name of the certificate</span></span>

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

### <span data-ttu-id="f9b79-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9b79-131">-DefaultProfile</span></span>
<span data-ttu-id="f9b79-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f9b79-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9b79-133">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="f9b79-133">-KeyVaultName</span></span>
<span data-ttu-id="f9b79-134">Nome del Vault di Azure Key, se non assegnato, verrà impostato come predefinito nel nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f9b79-134">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="f9b79-135">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9b79-135">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="f9b79-136">Nome del gruppo di risorse di Azure Key Vault, se non assegnato, verrà impostato come nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f9b79-136">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

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

### <span data-ttu-id="f9b79-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9b79-137">-Name</span></span>
<span data-ttu-id="f9b79-138">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="f9b79-138">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="f9b79-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9b79-139">-ResourceGroupName</span></span>
<span data-ttu-id="f9b79-140">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f9b79-140">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="f9b79-141">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="f9b79-141">-SecretIdentifier</span></span>
<span data-ttu-id="f9b79-142">URL segreto del Vault Key di Azure esistente, ad esempio ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="f9b79-142">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="f9b79-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f9b79-143">-Confirm</span></span>
<span data-ttu-id="f9b79-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9b79-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9b79-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9b79-145">-WhatIf</span></span>
<span data-ttu-id="f9b79-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9b79-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9b79-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9b79-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9b79-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9b79-148">CommonParameters</span></span>
<span data-ttu-id="f9b79-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9b79-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9b79-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9b79-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9b79-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f9b79-151">INPUTS</span></span>

### <span data-ttu-id="f9b79-152">System. String</span><span class="sxs-lookup"><span data-stu-id="f9b79-152">System.String</span></span>

### <span data-ttu-id="f9b79-153">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="f9b79-153">System.Security.SecureString</span></span>

## <span data-ttu-id="f9b79-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9b79-154">OUTPUTS</span></span>

### <span data-ttu-id="f9b79-155">Microsoft. Azure. Commands. ServiceFabric. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="f9b79-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="f9b79-156">Note</span><span class="sxs-lookup"><span data-stu-id="f9b79-156">NOTES</span></span>

## <span data-ttu-id="f9b79-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9b79-157">RELATED LINKS</span></span>

[<span data-ttu-id="f9b79-158">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="f9b79-158">Add-AzServiceFabricClusterCertificate</span></span>](./Add-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="f9b79-159">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="f9b79-159">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
