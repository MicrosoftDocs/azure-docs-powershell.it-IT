---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricapplicationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
ms.openlocfilehash: 58547205bc0edae3ea1ab9ff56d3df1ef71214f8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677084"
---
# <span data-ttu-id="113d8-101">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="113d8-101">Add-AzServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="113d8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="113d8-102">SYNOPSIS</span></span>
<span data-ttu-id="113d8-103">Aggiungere un nuovo certificato ai set di scale della macchina virtuale che compongono il cluster.</span><span class="sxs-lookup"><span data-stu-id="113d8-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="113d8-104">Il certificato è destinato a essere usato come certificato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="113d8-104">The certificate is intended to be used as an application certificate.</span></span>

## <span data-ttu-id="113d8-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="113d8-105">SYNTAX</span></span>

### <span data-ttu-id="113d8-106">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="113d8-106">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="113d8-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="113d8-107">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="113d8-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="113d8-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="113d8-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="113d8-109">DESCRIPTION</span></span>
<span data-ttu-id="113d8-110">Usare **Add-AzServiceFabricApplicationCertificate** per installare un certificato in tutti i nodi del cluster.</span><span class="sxs-lookup"><span data-stu-id="113d8-110">Use **Add-AzServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="113d8-111">Puoi specificare un certificato che hai già o avere il sistema per generarne uno nuovo e caricarlo in un Vault di chiave di Azure nuovo o esistente.</span><span class="sxs-lookup"><span data-stu-id="113d8-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="113d8-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="113d8-112">EXAMPLES</span></span>

### <span data-ttu-id="113d8-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="113d8-113">Example 1</span></span>
```
PS c:> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="113d8-114">Questo comando aggiungerà un certificato dall'archivio di chiavi di Azure esistente a tutti i tipi di nodo del cluster.</span><span class="sxs-lookup"><span data-stu-id="113d8-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="113d8-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="113d8-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="113d8-116">Questo comando creerà un certificato autofirmato nel Vault di chiave di Azure con il nome del gruppo di risorse del Vault chiave e il nome della chiave del Vault, viene installato in tutti i tipi di nodo del cluster e Scarica il certificato nella cartella "c:\test".</span><span class="sxs-lookup"><span data-stu-id="113d8-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="113d8-117">Il nome del certificato scaricato è uguale al nome del certificato di volta chiave.</span><span class="sxs-lookup"><span data-stu-id="113d8-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="113d8-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="113d8-118">PARAMETERS</span></span>

### <span data-ttu-id="113d8-119">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="113d8-119">-CertificateCommonName</span></span>
<span data-ttu-id="113d8-120">Nome comune del certificato</span><span class="sxs-lookup"><span data-stu-id="113d8-120">Certificate common name</span></span>

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

### <span data-ttu-id="113d8-121">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="113d8-121">-CertificateFile</span></span>
<span data-ttu-id="113d8-122">Percorso del file del certificato esistente.</span><span class="sxs-lookup"><span data-stu-id="113d8-122">The existing certificate file path.</span></span>

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

### <span data-ttu-id="113d8-123">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="113d8-123">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="113d8-124">Identificazione personale dell'autorità di certificazione, separate da virgole se più di una</span><span class="sxs-lookup"><span data-stu-id="113d8-124">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="113d8-125">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="113d8-125">-CertificateOutputFolder</span></span>
<span data-ttu-id="113d8-126">Percorso cartella del nuovo certificato da creare.</span><span class="sxs-lookup"><span data-stu-id="113d8-126">The folder path of the new certificate to be created.</span></span>

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

### <span data-ttu-id="113d8-127">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="113d8-127">-CertificatePassword</span></span>
<span data-ttu-id="113d8-128">La password del file PFX.</span><span class="sxs-lookup"><span data-stu-id="113d8-128">The password of the pfx file.</span></span>

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

### <span data-ttu-id="113d8-129">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="113d8-129">-CertificateSubjectName</span></span>
<span data-ttu-id="113d8-130">Nome DNS del certificato da creare.</span><span class="sxs-lookup"><span data-stu-id="113d8-130">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="113d8-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="113d8-131">-DefaultProfile</span></span>
<span data-ttu-id="113d8-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="113d8-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="113d8-133">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="113d8-133">-KeyVaultName</span></span>
<span data-ttu-id="113d8-134">Nome del Vault della chiave di Azure.</span><span class="sxs-lookup"><span data-stu-id="113d8-134">Azure key vault name.</span></span>

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

### <span data-ttu-id="113d8-135">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="113d8-135">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="113d8-136">Nome del gruppo di risorse di Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="113d8-136">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="113d8-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="113d8-137">-Name</span></span>
<span data-ttu-id="113d8-138">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="113d8-138">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="113d8-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="113d8-139">-ResourceGroupName</span></span>
<span data-ttu-id="113d8-140">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="113d8-140">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="113d8-141">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="113d8-141">-SecretIdentifier</span></span>
<span data-ttu-id="113d8-142">URI segreto del Vault Key di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="113d8-142">The existing Azure key vault secret uri.</span></span>

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

### <span data-ttu-id="113d8-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="113d8-143">-Confirm</span></span>
<span data-ttu-id="113d8-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="113d8-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="113d8-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="113d8-145">-WhatIf</span></span>
<span data-ttu-id="113d8-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="113d8-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="113d8-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="113d8-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="113d8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="113d8-148">CommonParameters</span></span>
<span data-ttu-id="113d8-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="113d8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="113d8-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="113d8-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="113d8-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="113d8-151">INPUTS</span></span>

### <span data-ttu-id="113d8-152">System. String</span><span class="sxs-lookup"><span data-stu-id="113d8-152">System.String</span></span>

### <span data-ttu-id="113d8-153">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="113d8-153">System.Security.SecureString</span></span>

## <span data-ttu-id="113d8-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="113d8-154">OUTPUTS</span></span>

### <span data-ttu-id="113d8-155">Microsoft. Azure. Commands. ServiceFabric. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="113d8-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="113d8-156">Note</span><span class="sxs-lookup"><span data-stu-id="113d8-156">NOTES</span></span>

## <span data-ttu-id="113d8-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="113d8-157">RELATED LINKS</span></span>

[<span data-ttu-id="113d8-158">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="113d8-158">Add-AzServiceFabricClusterCertificate</span></span>](./Add-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="113d8-159">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="113d8-159">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
