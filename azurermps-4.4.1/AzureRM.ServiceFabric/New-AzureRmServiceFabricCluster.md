---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
ms.openlocfilehash: c1f6dea6c4fb103107a052d64a82ad81eafdb8c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521525"
---
# <span data-ttu-id="418d7-101">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="418d7-101">New-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="418d7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="418d7-102">SYNOPSIS</span></span>
<span data-ttu-id="418d7-103">Questo comando usa i certificati forniti dai certificati autofirmati o generati dal sistema per configurare un nuovo cluster di servizi in tessuto.</span><span class="sxs-lookup"><span data-stu-id="418d7-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="418d7-104">Può usare un modello predefinito o un modello personalizzato che fornisci.</span><span class="sxs-lookup"><span data-stu-id="418d7-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="418d7-105">È possibile specificare una cartella in cui esportare i certificati autofirmati o recuperarli in un secondo momento dall'archivio chiavi.</span><span class="sxs-lookup"><span data-stu-id="418d7-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="418d7-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="418d7-106">SYNTAX</span></span>

### <span data-ttu-id="418d7-107">ByDefaultArmTemplate (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="418d7-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="418d7-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="418d7-108">ByExistingKeyVault</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="418d7-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="418d7-109">ByNewPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>]
 [-KeyVaultName <String>] [-CertificateSubjectName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="418d7-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="418d7-110">ByExistingPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="418d7-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="418d7-111">DESCRIPTION</span></span>
<span data-ttu-id="418d7-112">Il comando **New-AzureRmServiceFabricCluster** usa i certificati forniti o i certificati autofirmati generati dal sistema per configurare un nuovo cluster di servizi in tessuto.</span><span class="sxs-lookup"><span data-stu-id="418d7-112">The **New-AzureRmServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="418d7-113">Il modello usato può essere un modello predefinito o un modello personalizzato che fornisci.</span><span class="sxs-lookup"><span data-stu-id="418d7-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="418d7-114">È possibile specificare una cartella per esportare i certificati autofirmati o recuperarli in un secondo momento dall'archivio chiavi.</span><span class="sxs-lookup"><span data-stu-id="418d7-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>

<span data-ttu-id="418d7-115">Se si specifica un modello e un file di parametro personalizzati, non è necessario specificare le informazioni sul certificato nel file di parametro, il sistema compilerà questi parametri.</span><span class="sxs-lookup"><span data-stu-id="418d7-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>

<span data-ttu-id="418d7-116">Le quattro opzioni sono descritte di seguito.</span><span class="sxs-lookup"><span data-stu-id="418d7-116">The four options are detailed below.</span></span> <span data-ttu-id="418d7-117">Scorrere verso il basso per le spiegazioni di ogni parametro.</span><span class="sxs-lookup"><span data-stu-id="418d7-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="418d7-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="418d7-118">EXAMPLES</span></span>

### <span data-ttu-id="418d7-119">Esempio 1: specificare solo le dimensioni del cluster, il nome dell'oggetto CERT e il sistema operativo per distribuire un cluster.</span><span class="sxs-lookup"><span data-stu-id="418d7-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test01"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.cloudapp.azure.com" -f $RGname, $clusterloc
$pfxfolder="~\Documents"

Write-Output "create cluster in " $clusterloc "subject name for cert " $subname "and output the cert into " $pfxfolder

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -Location $clusterloc -ClusterSize 3 -VmPassword $pwd -CertificateSubjectName $subname -CertificateOutputFolder $pfxfolder -CertificatePassword $pwd -OS WindowsServer2016Datacenter
```

<span data-ttu-id="418d7-120">Questo comando specifica solo le dimensioni del cluster, il nome dell'oggetto CERT e il sistema operativo per la distribuzione di un cluster.</span><span class="sxs-lookup"><span data-stu-id="418d7-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="418d7-121">Esempio 2: specificare una risorsa di certificato esistente in un Vault chiave e un modello personalizzato per distribuire un cluster</span><span class="sxs-lookup"><span data-stu-id="418d7-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>
```
$RGname="test20"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secertId="https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -SecretIdentifier $secertId
```

<span data-ttu-id="418d7-122">Questo comando specifica una risorsa di certificato esistente in un Vault chiave e un modello personalizzato per la distribuzione di un cluster.</span><span class="sxs-lookup"><span data-stu-id="418d7-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="418d7-123">Esempio 3: creare un nuovo cluster usando un modello personalizzato.</span><span class="sxs-lookup"><span data-stu-id="418d7-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="418d7-124">Specificare il nome RG diverso per il Vault chiave e far caricare al sistema il certificato</span><span class="sxs-lookup"><span data-stu-id="418d7-124">Specify the different RG name for the key vault and have the system upload the certificate to it</span></span>
```
$pwd="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.$clusterloc.cloudapp.azure.com" -f $RGName, $clusterloc
$pfxfolder="~\Documents"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secertId="https://test1.vault.azure.net:443/secrets/testcertificate4/55ec7c4dc61a462bbc645ffc9b4b225f"
$thumprint="C2D7E11DD35153A702A51D10A424A3014B9B6E8B"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateOutputFolder $pfxfolder -CertificatePassword $pwd -KeyVaultResouceGroupName $keyVaultRG  -KeyVaultName $keyVault -CertificateSubjectName $subname
```

<span data-ttu-id="418d7-125">Questo comando crea un nuovo cluster usando un modello personalizzato.</span><span class="sxs-lookup"><span data-stu-id="418d7-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="418d7-126">Specificare il nome RG diverso per il Vault chiave e far caricare il certificato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="418d7-126">Specify the different RG name for the key vault and have the system upload the certificate to it.</span></span>

### <span data-ttu-id="418d7-127">Esempio 4: creare un nuovo gruppo di certificati e un modello personalizzato</span><span class="sxs-lookup"><span data-stu-id="418d7-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>
```
$certPwd="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$clusterloc="SouthCentralUS"
$pfxsourcefile="c:\Mycertificates\my2017Prodcert.pfx"
$templateParmfile="~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateSourceFile $pfxsourcefile -CertificatePassword $certpwd -KeyVaultResouceGroupName $keyVaultRG -KeyVaultName $keyVault
```

<span data-ttu-id="418d7-128">Questo comando consente di creare un nuovo modello di certificato e personalizzato.</span><span class="sxs-lookup"><span data-stu-id="418d7-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="418d7-129">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="418d7-129">PARAMETERS</span></span>

### <span data-ttu-id="418d7-130">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="418d7-130">-CertificateFile</span></span>
<span data-ttu-id="418d7-131">Percorso del file di certificato esistente per il certificato del cluster principale.</span><span class="sxs-lookup"><span data-stu-id="418d7-131">The existing certificate file path for the primary cluster certificate.</span></span>

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

### <span data-ttu-id="418d7-132">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="418d7-132">-CertificateOutputFolder</span></span>
<span data-ttu-id="418d7-133">Cartella del nuovo file di certificato da creare.</span><span class="sxs-lookup"><span data-stu-id="418d7-133">The folder of the new certificate file to be created.</span></span>

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

### <span data-ttu-id="418d7-134">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="418d7-134">-CertificatePassword</span></span>
<span data-ttu-id="418d7-135">La password del file di certificato.</span><span class="sxs-lookup"><span data-stu-id="418d7-135">The password of the certificate file.</span></span>

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

### <span data-ttu-id="418d7-136">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="418d7-136">-CertificateSubjectName</span></span>
<span data-ttu-id="418d7-137">Nome dell'oggetto del certificato da creare.</span><span class="sxs-lookup"><span data-stu-id="418d7-137">The subject name of the certificate to be created.</span></span>

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

### <span data-ttu-id="418d7-138">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="418d7-138">-ClusterSize</span></span>
<span data-ttu-id="418d7-139">Numero di nodi nel cluster.</span><span class="sxs-lookup"><span data-stu-id="418d7-139">The number of nodes in the cluster.</span></span> <span data-ttu-id="418d7-140">Le impostazioni predefinite sono 5 nodi.</span><span class="sxs-lookup"><span data-stu-id="418d7-140">Default are 5 nodes.</span></span>

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

### <span data-ttu-id="418d7-141">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="418d7-141">-KeyVaultName</span></span>
<span data-ttu-id="418d7-142">Nome del Vault della chiave di Azure.</span><span class="sxs-lookup"><span data-stu-id="418d7-142">Azure key vault name.</span></span> <span data-ttu-id="418d7-143">Se non viene assegnato, verrà impostato come predefinito nel nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="418d7-143">If not given, it will be defaulted to the resource group name.</span></span>

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

### <span data-ttu-id="418d7-144">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="418d7-144">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="418d7-145">Nome del gruppo di risorse di Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="418d7-145">Azure key vault resource group name.</span></span> <span data-ttu-id="418d7-146">Se non è stato assegnato, verrà impostato sul nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="418d7-146">If not given, it will be defaulted to resource group name.</span></span>

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

### <span data-ttu-id="418d7-147">-Posizione</span><span class="sxs-lookup"><span data-stu-id="418d7-147">-Location</span></span>
<span data-ttu-id="418d7-148">Posizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="418d7-148">The resource group location.</span></span>

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

### <span data-ttu-id="418d7-149">-Nome</span><span class="sxs-lookup"><span data-stu-id="418d7-149">-Name</span></span>
<span data-ttu-id="418d7-150">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="418d7-150">Specify the name of the cluster.</span></span> <span data-ttu-id="418d7-151">Se non è specificata, sarà uguale al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="418d7-151">If not given, it will be same as resource group name.</span></span>

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

### <span data-ttu-id="418d7-152">-OS</span><span class="sxs-lookup"><span data-stu-id="418d7-152">-OS</span></span>
<span data-ttu-id="418d7-153">Sistema operativo delle macchine virtuali che costituiscono il cluster.</span><span class="sxs-lookup"><span data-stu-id="418d7-153">The Operating System of the VMs that make up the cluster.</span></span>

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

### <span data-ttu-id="418d7-154">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="418d7-154">-ParameterFile</span></span>
<span data-ttu-id="418d7-155">Percorso del file del parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="418d7-155">The path to the template parameter file.</span></span>

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

### <span data-ttu-id="418d7-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="418d7-156">-ResourceGroupName</span></span>
<span data-ttu-id="418d7-157">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="418d7-157">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="418d7-158">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="418d7-158">-SecondaryCertificateFile</span></span>
<span data-ttu-id="418d7-159">Percorso del file di certificato esistente per il certificato del cluster secondario.</span><span class="sxs-lookup"><span data-stu-id="418d7-159">The existing certificate file path for the secondary cluster certificate.</span></span>

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

### <span data-ttu-id="418d7-160">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="418d7-160">-SecondaryCertificatePassword</span></span>
<span data-ttu-id="418d7-161">La password del file di certificato.</span><span class="sxs-lookup"><span data-stu-id="418d7-161">The password of the certificate file.</span></span>

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

### <span data-ttu-id="418d7-162">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="418d7-162">-SecretIdentifier</span></span>
<span data-ttu-id="418d7-163">URL segreto del Vault Key di Azure esistente, ad esempio:' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '.</span><span class="sxs-lookup"><span data-stu-id="418d7-163">The existing Azure key vault secret URL, for example: 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'.</span></span>

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

### <span data-ttu-id="418d7-164">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="418d7-164">-TemplateFile</span></span>
<span data-ttu-id="418d7-165">Percorso del file del modello.</span><span class="sxs-lookup"><span data-stu-id="418d7-165">The path to the template file.</span></span>

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

### <span data-ttu-id="418d7-166">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="418d7-166">-VmPassword</span></span>
<span data-ttu-id="418d7-167">La password della VM.</span><span class="sxs-lookup"><span data-stu-id="418d7-167">The password of the Vm.</span></span>

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

### <span data-ttu-id="418d7-168">-VmSku</span><span class="sxs-lookup"><span data-stu-id="418d7-168">-VmSku</span></span>
<span data-ttu-id="418d7-169">SKU VM.</span><span class="sxs-lookup"><span data-stu-id="418d7-169">The Vm Sku.</span></span>

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

### <span data-ttu-id="418d7-170">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="418d7-170">-VmUserName</span></span>
<span data-ttu-id="418d7-171">Nome utente per la registrazione in VM.</span><span class="sxs-lookup"><span data-stu-id="418d7-171">The user name for logging to Vm.</span></span>

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

### <span data-ttu-id="418d7-172">-Confermare</span><span class="sxs-lookup"><span data-stu-id="418d7-172">-Confirm</span></span>
<span data-ttu-id="418d7-173">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="418d7-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="418d7-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="418d7-174">-WhatIf</span></span>
<span data-ttu-id="418d7-175">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="418d7-175">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="418d7-176">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="418d7-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="418d7-177">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="418d7-177">-DefaultProfile</span></span>
<span data-ttu-id="418d7-178">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="418d7-178">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="418d7-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="418d7-179">CommonParameters</span></span>
<span data-ttu-id="418d7-180">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="418d7-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="418d7-181">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="418d7-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="418d7-182">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="418d7-182">INPUTS</span></span>

### <span data-ttu-id="418d7-183">System. String</span><span class="sxs-lookup"><span data-stu-id="418d7-183">System.String</span></span>
<span data-ttu-id="418d7-184">System. Security. SecureString System. Int32 Microsoft. Azure. Commands. ServiceFabric. Models. OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="418d7-184">System.Security.SecureString System.Int32 Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="418d7-185">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="418d7-185">OUTPUTS</span></span>

### <span data-ttu-id="418d7-186">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="418d7-186">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="418d7-187">Note</span><span class="sxs-lookup"><span data-stu-id="418d7-187">NOTES</span></span>

## <span data-ttu-id="418d7-188">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="418d7-188">RELATED LINKS</span></span>

