---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
ms.openlocfilehash: b603087063a763d63f986afa7568160a6623a22b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956621"
---
# <span data-ttu-id="b7a92-101">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="b7a92-101">New-AzServiceFabricCluster</span></span>

## <span data-ttu-id="b7a92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7a92-102">SYNOPSIS</span></span>

<span data-ttu-id="b7a92-103">Questo comando usa i certificati forniti dall'utente o i certificati autofirmati generati dal sistema per configurare un nuovo cluster di tessuto di servizio.</span><span class="sxs-lookup"><span data-stu-id="b7a92-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="b7a92-104">Può usare un modello predefinito o un modello personalizzato specificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b7a92-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="b7a92-105">È possibile specificare una cartella in cui esportare i certificati autofirmati o recuperarli in un secondo momento dal vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="b7a92-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

## <span data-ttu-id="b7a92-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7a92-106">SYNTAX</span></span>

### <span data-ttu-id="b7a92-107">ByDefaultArmTemplate (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b7a92-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7a92-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="b7a92-108">ByExistingKeyVault</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 -SecretIdentifier <String> [-Thumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7a92-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="b7a92-109">ByNewPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>]
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateSubjectName <String>]
 [-VmPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7a92-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="b7a92-110">ByExistingPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7a92-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b7a92-111">DESCRIPTION</span></span>

<span data-ttu-id="b7a92-112">Il **comando New-AzServiceFabricCluster** usa i certificati forniti dall'utente o i certificati autofirmati generati dal sistema per configurare un nuovo cluster di tessuto di servizio.</span><span class="sxs-lookup"><span data-stu-id="b7a92-112">The **New-AzServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="b7a92-113">Il modello usato può essere un modello predefinito o un modello personalizzato specificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b7a92-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="b7a92-114">È possibile specificare una cartella per esportare i certificati autofirmati o recuperarli in un secondo momento dal vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="b7a92-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>
<span data-ttu-id="b7a92-115">Se si specifica un modello personalizzato e un file di parametri, non è necessario fornire le informazioni sul certificato nel file dei parametri, il sistema popola questi parametri.</span><span class="sxs-lookup"><span data-stu-id="b7a92-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>
<span data-ttu-id="b7a92-116">Le quattro opzioni sono dettagliate di seguito.</span><span class="sxs-lookup"><span data-stu-id="b7a92-116">The four options are detailed below.</span></span> <span data-ttu-id="b7a92-117">Scorrere verso il basso per visualizzare le spiegazioni su ogni parametro.</span><span class="sxs-lookup"><span data-stu-id="b7a92-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="b7a92-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7a92-118">EXAMPLES</span></span>

### <span data-ttu-id="b7a92-119">Esempio 1: Specificare solo le dimensioni del cluster, il nome dell'oggetto del certificato e il sistema operativo per distribuire un cluster</span><span class="sxs-lookup"><span data-stu-id="b7a92-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "quickstart-sf-group"
$azureRegion = "southcentralus"
$clusterDnsName = "{0}.{1}.cloudapp.azure.com" -f $resourceGroupName, $azureRegion
$localCertificateFolder = "c:\certs"

Write-Output "Create cluster in '$azureRegion' with cert subject name '$clusterDnsName' and cert output path '$localCertificateFolder'"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -Location $azureRegion -ClusterSize 5 -VmPassword $password -CertificateSubjectName $clusterDnsName -CertificateOutputFolder $localCertificateFolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="b7a92-120">Questo comando specifica solo le dimensioni del cluster, il nome dell'oggetto del certificato e il sistema operativo per distribuire un cluster.</span><span class="sxs-lookup"><span data-stu-id="b7a92-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="b7a92-121">Esempio 2: Specificare una risorsa Certificato esistente in un vault chiave e un modello personalizzato per distribuire un cluster</span><span class="sxs-lookup"><span data-stu-id="b7a92-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>

```powershell
$resourceGroupName = "test20"
$templateParameterFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId = "https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -SecretIdentifier $secretId
```

<span data-ttu-id="b7a92-122">Questo comando specifica una risorsa Certificato esistente in un vault chiave e un modello personalizzato per distribuire un cluster.</span><span class="sxs-lookup"><span data-stu-id="b7a92-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="b7a92-123">Esempio 3: Creare un nuovo cluster usando un modello personalizzato.</span><span class="sxs-lookup"><span data-stu-id="b7a92-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="b7a92-124">Specificare un nome diverso per il gruppo di risorse per la chiave vault e fare in modo che il sistema carichi un nuovo certificato</span><span class="sxs-lookup"><span data-stu-id="b7a92-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "quickstart-sf-group"
$keyVaultResourceGroupName = " quickstart-kv-group"
$keyVaultName = "quickstart-kv"
$azureRegion = "southcentralus"
$clusterDnsName = "{0}.{1}.cloudapp.azure.com" -F $resourceGroupName, $azureRegion
$localCertificateFolder = "~\Documents"
$templateParameterFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -CertificateOutputFolder $localCertificateFolder -CertificatePassword $password -KeyVaultResourceGroupName $keyVaultResourceGroupName  -KeyVaultName $keyVaultName -CertificateSubjectName $clusterDnsName
```

<span data-ttu-id="b7a92-125">Questo comando crea un nuovo cluster usando un modello personalizzato.</span><span class="sxs-lookup"><span data-stu-id="b7a92-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="b7a92-126">Specificare un nome diverso per il gruppo di risorse per la chiave vault e fare in modo che il sistema carichi un nuovo certificato</span><span class="sxs-lookup"><span data-stu-id="b7a92-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="b7a92-127">Esempio 4: Portare il proprio certificato e un modello personalizzato e creare un nuovo cluster</span><span class="sxs-lookup"><span data-stu-id="b7a92-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "test20"
$keyVaultResourceGroupName = "test20kvrg"
$keyVaultName = "test20kv"
$localCertificateFile = "c:\Mycertificates\my2017Prodcert.pfx"
$templateParameterFile = "~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -CertificateFile $localCertificateFile -CertificatePassword $password -KeyVaultResourceGroupName $keyVaultResourceGroupName -KeyVaultName $keyVaultName
```

<span data-ttu-id="b7a92-128">Questo comando consente di creare un certificato e un modello personalizzato personalizzati e di creare un nuovo cluster.</span><span class="sxs-lookup"><span data-stu-id="b7a92-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="b7a92-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7a92-129">PARAMETERS</span></span>

### <span data-ttu-id="b7a92-130">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="b7a92-130">-CertificateCommonName</span></span>

<span data-ttu-id="b7a92-131">Nome comune certificato</span><span class="sxs-lookup"><span data-stu-id="b7a92-131">Certificate common name</span></span>

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

### <span data-ttu-id="b7a92-132">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b7a92-132">-CertificateFile</span></span>

<span data-ttu-id="b7a92-133">Percorso file del certificato esistente per il certificato del cluster primario</span><span class="sxs-lookup"><span data-stu-id="b7a92-133">The existing certificate file path for the primary cluster certificate</span></span>

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

### <span data-ttu-id="b7a92-134">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="b7a92-134">-CertificateIssuerThumbprint</span></span>

<span data-ttu-id="b7a92-135">Pollice dell'autorità di certificazione emittente, separata da virgole se più di una</span><span class="sxs-lookup"><span data-stu-id="b7a92-135">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="b7a92-136">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="b7a92-136">-CertificateOutputFolder</span></span>

<span data-ttu-id="b7a92-137">Cartella del nuovo file di certificato da creare</span><span class="sxs-lookup"><span data-stu-id="b7a92-137">The folder of the new certificate file to be created</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a92-138">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="b7a92-138">-CertificatePassword</span></span>

<span data-ttu-id="b7a92-139">Password del file di certificato</span><span class="sxs-lookup"><span data-stu-id="b7a92-139">The password of the certificate file</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a92-140">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="b7a92-140">-CertificateSubjectName</span></span>

<span data-ttu-id="b7a92-141">Il nome dell'oggetto del certificato da creare</span><span class="sxs-lookup"><span data-stu-id="b7a92-141">The subject name of the certificate to be created</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Subject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a92-142">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="b7a92-142">-ClusterSize</span></span>

<span data-ttu-id="b7a92-143">Numero di nodi nel cluster.</span><span class="sxs-lookup"><span data-stu-id="b7a92-143">The number of nodes in the cluster.</span></span>
<span data-ttu-id="b7a92-144">L'impostazione predefinita è 5 nodi</span><span class="sxs-lookup"><span data-stu-id="b7a92-144">Default are 5 nodes</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a92-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7a92-145">-DefaultProfile</span></span>

<span data-ttu-id="b7a92-146">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7a92-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7a92-147">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="b7a92-147">-KeyVaultName</span></span>

<span data-ttu-id="b7a92-148">Nome del vault della chiave di Azure, se non è assegnato verrà utilizzato per impostazione predefinita con il nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b7a92-148">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a92-149">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7a92-149">-KeyVaultResourceGroupName</span></span>

<span data-ttu-id="b7a92-150">Nome del gruppo di risorse del vault della chiave di Azure, se non è assegnato verrà utilizzato per impostazione predefinita sul nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b7a92-150">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: KeyVaultResouceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a92-151">-Location</span><span class="sxs-lookup"><span data-stu-id="b7a92-151">-Location</span></span>

<span data-ttu-id="b7a92-152">Posizione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b7a92-152">The resource group location</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a92-153">-Name</span><span class="sxs-lookup"><span data-stu-id="b7a92-153">-Name</span></span>

<span data-ttu-id="b7a92-154">Specificare il nome del cluster, se non gli viene assegnato sarà uguale al nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b7a92-154">Specify the name of the cluster, if not given it will be same as resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases: ClusterName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a92-155">-OS</span><span class="sxs-lookup"><span data-stu-id="b7a92-155">-OS</span></span>

<span data-ttu-id="b7a92-156">Sistema operativo delle macchine virtuali che costituiscono il cluster.</span><span class="sxs-lookup"><span data-stu-id="b7a92-156">The Operating System of the VMs that make up the cluster.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem
Parameter Sets: ByDefaultArmTemplate
Aliases: VmImage
Accepted values: WindowsServer2012R2Datacenter, WindowsServer2016Datacenter, WindowsServer2016DatacenterwithContainers, UbuntuServer1604

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a92-157">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="b7a92-157">-ParameterFile</span></span>

<span data-ttu-id="b7a92-158">Percorso del file dei parametri del modello.</span><span class="sxs-lookup"><span data-stu-id="b7a92-158">The path to the template parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a92-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7a92-159">-ResourceGroupName</span></span>

<span data-ttu-id="b7a92-160">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b7a92-160">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b7a92-161">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="b7a92-161">-SecondaryCertificateFile</span></span>

<span data-ttu-id="b7a92-162">Percorso file del certificato esistente per il certificato del cluster secondario</span><span class="sxs-lookup"><span data-stu-id="b7a92-162">The existing certificate file path for the secondary cluster certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecSource

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a92-163">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="b7a92-163">-SecondaryCertificatePassword</span></span>

<span data-ttu-id="b7a92-164">Password del file di certificato</span><span class="sxs-lookup"><span data-stu-id="b7a92-164">The password of the certificate file</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecCertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a92-165">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="b7a92-165">-SecretIdentifier</span></span>

<span data-ttu-id="b7a92-166">L'URL segreto del vault della chiave di Azure esistente, ad esempio ' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="b7a92-166">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="b7a92-167">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="b7a92-167">-TemplateFile</span></span>

<span data-ttu-id="b7a92-168">Il percorso del file modello.</span><span class="sxs-lookup"><span data-stu-id="b7a92-168">The path to the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a92-169">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="b7a92-169">-Thumbprint</span></span>
<span data-ttu-id="b7a92-170">L'impronta digitale del certificato correspoinding al SecretIdentifier.</span><span class="sxs-lookup"><span data-stu-id="b7a92-170">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="b7a92-171">Usare questa opzione se il certificato non viene gestito come vault della chiave conrebbe solo il certificato archiviato come segreto e il cmdlet non è in grado di individuare nuovamente l'immagine thumbprint.</span><span class="sxs-lookup"><span data-stu-id="b7a92-171">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

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

### <span data-ttu-id="b7a92-172">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="b7a92-172">-VmPassword</span></span>

<span data-ttu-id="b7a92-173">La password della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b7a92-173">The password of the Vm.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a92-174">-VmSku</span><span class="sxs-lookup"><span data-stu-id="b7a92-174">-VmSku</span></span>

<span data-ttu-id="b7a92-175">SKU della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="b7a92-175">The Vm Sku</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases: Sku

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a92-176">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="b7a92-176">-VmUserName</span></span>

<span data-ttu-id="b7a92-177">Nome utente per la registrazione alla macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="b7a92-177">The user name for logging to Vm</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a92-178">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7a92-178">-Confirm</span></span>

<span data-ttu-id="b7a92-179">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7a92-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7a92-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7a92-180">-WhatIf</span></span>

<span data-ttu-id="b7a92-181">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7a92-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7a92-182">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7a92-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7a92-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7a92-183">CommonParameters</span></span>
<span data-ttu-id="b7a92-184">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7a92-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7a92-185">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b7a92-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7a92-186">INPUT</span><span class="sxs-lookup"><span data-stu-id="b7a92-186">INPUTS</span></span>

### <span data-ttu-id="b7a92-187">System.String</span><span class="sxs-lookup"><span data-stu-id="b7a92-187">System.String</span></span>

### <span data-ttu-id="b7a92-188">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="b7a92-188">System.Security.SecureString</span></span>

### <span data-ttu-id="b7a92-189">System.Int32</span><span class="sxs-lookup"><span data-stu-id="b7a92-189">System.Int32</span></span>

### <span data-ttu-id="b7a92-190">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="b7a92-190">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="b7a92-191">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7a92-191">OUTPUTS</span></span>

### <span data-ttu-id="b7a92-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="b7a92-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="b7a92-193">NOTE</span><span class="sxs-lookup"><span data-stu-id="b7a92-193">NOTES</span></span>

## <span data-ttu-id="b7a92-194">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7a92-194">RELATED LINKS</span></span>
