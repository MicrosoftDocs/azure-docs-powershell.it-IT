---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
ms.openlocfilehash: e78912d2a8ab0ce4f5e990e69e236853a85019c6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677078"
---
# <span data-ttu-id="a9b5a-101">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="a9b5a-101">New-AzServiceFabricCluster</span></span>

## <span data-ttu-id="a9b5a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a9b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="a9b5a-103">Questo comando usa i certificati forniti dai certificati autofirmati o generati dal sistema per configurare un nuovo cluster di servizi in tessuto.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="a9b5a-104">Può usare un modello predefinito o un modello personalizzato che fornisci.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="a9b5a-105">È possibile specificare una cartella in cui esportare i certificati autofirmati o recuperarli in un secondo momento dall'archivio chiavi.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

## <span data-ttu-id="a9b5a-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9b5a-106">SYNTAX</span></span>

### <span data-ttu-id="a9b5a-107">ByDefaultArmTemplate (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a9b5a-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9b5a-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="a9b5a-108">ByExistingKeyVault</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9b5a-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="a9b5a-109">ByNewPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>]
 [-KeyVaultName <String>] [-CertificateSubjectName <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9b5a-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="a9b5a-110">ByExistingPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9b5a-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9b5a-111">DESCRIPTION</span></span>
<span data-ttu-id="a9b5a-112">Il comando **New-AzServiceFabricCluster** usa i certificati forniti o i certificati autofirmati generati dal sistema per configurare un nuovo cluster di servizi in tessuto.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-112">The **New-AzServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="a9b5a-113">Il modello usato può essere un modello predefinito o un modello personalizzato che fornisci.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="a9b5a-114">È possibile specificare una cartella per esportare i certificati autofirmati o recuperarli in un secondo momento dall'archivio chiavi.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>
<span data-ttu-id="a9b5a-115">Se si specifica un modello e un file di parametro personalizzati, non è necessario specificare le informazioni sul certificato nel file di parametro, il sistema compilerà questi parametri.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>
<span data-ttu-id="a9b5a-116">Le quattro opzioni sono descritte di seguito.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-116">The four options are detailed below.</span></span> <span data-ttu-id="a9b5a-117">Scorrere verso il basso per le spiegazioni di ogni parametro.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="a9b5a-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9b5a-118">EXAMPLES</span></span>

### <span data-ttu-id="a9b5a-119">Esempio 1: specificare solo le dimensioni del cluster, il nome dell'oggetto CERT e il sistema operativo per distribuire un cluster.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test01"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.cloudapp.azure.com" -f $RGname, $clusterloc
$pfxfolder="c:\certs"

Write-Output "Create cluster in '$clusterloc' with cert subject name '$subname' and cert output path '$pfxfolder'"

New-AzServiceFabricCluster -ResourceGroupName $RGname -Location $clusterloc -ClusterSize 5 -VmPassword $pass -CertificateSubjectName $subname -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="a9b5a-120">Questo comando specifica solo le dimensioni del cluster, il nome dell'oggetto CERT e il sistema operativo per la distribuzione di un cluster.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="a9b5a-121">Esempio 2: specificare una risorsa di certificato esistente in un Vault chiave e un modello personalizzato per distribuire un cluster</span><span class="sxs-lookup"><span data-stu-id="a9b5a-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>
```
$RGname="test20"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId="https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -SecretIdentifier $secretId
```

<span data-ttu-id="a9b5a-122">Questo comando specifica una risorsa di certificato esistente in un Vault chiave e un modello personalizzato per la distribuzione di un cluster.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="a9b5a-123">Esempio 3: creare un nuovo cluster usando un modello personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="a9b5a-124">Specificare un nome di gruppo di risorse diverso per il Vault chiave e far caricare al sistema un nuovo certificato</span><span class="sxs-lookup"><span data-stu-id="a9b5a-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.$clusterloc.cloudapp.azure.com" -f $RGName, $clusterloc
$pfxfolder="~\Documents"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -KeyVaultResouceGroupName $keyVaultRG  -KeyVaultName $keyVault -CertificateSubjectName $subname
```

<span data-ttu-id="a9b5a-125">Questo comando crea un nuovo cluster usando un modello personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="a9b5a-126">Specificare un nome di gruppo di risorse diverso per il Vault chiave e far caricare al sistema un nuovo certificato</span><span class="sxs-lookup"><span data-stu-id="a9b5a-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="a9b5a-127">Esempio 4: creare un nuovo gruppo di certificati e un modello personalizzato</span><span class="sxs-lookup"><span data-stu-id="a9b5a-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$pfxsourcefile="c:\Mycertificates\my2017Prodcert.pfx"
$templateParmfile="~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateFile $pfxsourcefile -CertificatePassword $pass -KeyVaultResouceGroupName $keyVaultRG -KeyVaultName $keyVault
```

<span data-ttu-id="a9b5a-128">Questo comando consente di creare un nuovo modello di certificato e personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="a9b5a-129">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a9b5a-129">PARAMETERS</span></span>

### <span data-ttu-id="a9b5a-130">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="a9b5a-130">-CertificateCommonName</span></span>
<span data-ttu-id="a9b5a-131">Nome comune del certificato</span><span class="sxs-lookup"><span data-stu-id="a9b5a-131">Certificate common name</span></span>

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

### <span data-ttu-id="a9b5a-132">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="a9b5a-132">-CertificateFile</span></span>
<span data-ttu-id="a9b5a-133">Percorso del file di certificato esistente per il certificato del cluster principale.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-133">The existing certificate file path for the primary cluster certificate.</span></span>

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

### <span data-ttu-id="a9b5a-134">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="a9b5a-134">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="a9b5a-135">Identificazione personale dell'autorità di certificazione, separate da virgole se più di una</span><span class="sxs-lookup"><span data-stu-id="a9b5a-135">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="a9b5a-136">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="a9b5a-136">-CertificateOutputFolder</span></span>
<span data-ttu-id="a9b5a-137">Cartella del nuovo file di certificato da creare.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-137">The folder of the new certificate file to be created.</span></span>

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

### <span data-ttu-id="a9b5a-138">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="a9b5a-138">-CertificatePassword</span></span>
<span data-ttu-id="a9b5a-139">La password del file di certificato.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-139">The password of the certificate file.</span></span>

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

### <span data-ttu-id="a9b5a-140">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="a9b5a-140">-CertificateSubjectName</span></span>
<span data-ttu-id="a9b5a-141">Nome dell'oggetto del certificato da creare.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-141">The subject name of the certificate to be created.</span></span>

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

### <span data-ttu-id="a9b5a-142">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="a9b5a-142">-ClusterSize</span></span>
<span data-ttu-id="a9b5a-143">Numero di nodi nel cluster.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-143">The number of nodes in the cluster.</span></span> <span data-ttu-id="a9b5a-144">Le impostazioni predefinite sono 5 nodi.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-144">Default are 5 nodes.</span></span>

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

### <span data-ttu-id="a9b5a-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9b5a-145">-DefaultProfile</span></span>
<span data-ttu-id="a9b5a-146">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9b5a-147">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="a9b5a-147">-KeyVaultName</span></span>
<span data-ttu-id="a9b5a-148">Nome del Vault della chiave di Azure.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-148">Azure key vault name.</span></span> <span data-ttu-id="a9b5a-149">Se non viene assegnato, verrà impostato come predefinito nel nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-149">If not given, it will be defaulted to the resource group name.</span></span>

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

### <span data-ttu-id="a9b5a-150">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9b5a-150">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="a9b5a-151">Nome del gruppo di risorse di Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-151">Azure key vault resource group name.</span></span> <span data-ttu-id="a9b5a-152">Se non è stato assegnato, verrà impostato sul nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-152">If not given, it will be defaulted to resource group name.</span></span>

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

### <span data-ttu-id="a9b5a-153">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a9b5a-153">-Location</span></span>
<span data-ttu-id="a9b5a-154">Posizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-154">The resource group location.</span></span>

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

### <span data-ttu-id="a9b5a-155">-Nome</span><span class="sxs-lookup"><span data-stu-id="a9b5a-155">-Name</span></span>
<span data-ttu-id="a9b5a-156">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-156">Specify the name of the cluster.</span></span> <span data-ttu-id="a9b5a-157">Se non è specificata, sarà uguale al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-157">If not given, it will be same as resource group name.</span></span>

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

### <span data-ttu-id="a9b5a-158">-OS</span><span class="sxs-lookup"><span data-stu-id="a9b5a-158">-OS</span></span>
<span data-ttu-id="a9b5a-159">Sistema operativo delle macchine virtuali che costituiscono il cluster.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-159">The Operating System of the VMs that make up the cluster.</span></span>

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

### <span data-ttu-id="a9b5a-160">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="a9b5a-160">-ParameterFile</span></span>
<span data-ttu-id="a9b5a-161">Percorso del file del parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-161">The path to the template parameter file.</span></span>

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

### <span data-ttu-id="a9b5a-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9b5a-162">-ResourceGroupName</span></span>
<span data-ttu-id="a9b5a-163">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-163">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a9b5a-164">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="a9b5a-164">-SecondaryCertificateFile</span></span>
<span data-ttu-id="a9b5a-165">Percorso del file di certificato esistente per il certificato del cluster secondario.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-165">The existing certificate file path for the secondary cluster certificate.</span></span>

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

### <span data-ttu-id="a9b5a-166">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="a9b5a-166">-SecondaryCertificatePassword</span></span>
<span data-ttu-id="a9b5a-167">La password del file di certificato.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-167">The password of the certificate file.</span></span>

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

### <span data-ttu-id="a9b5a-168">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="a9b5a-168">-SecretIdentifier</span></span>
<span data-ttu-id="a9b5a-169">URL segreto del Vault Key di Azure esistente, ad esempio:' https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-169">The existing Azure key vault secret URL, for example: 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'.</span></span>

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

### <span data-ttu-id="a9b5a-170">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="a9b5a-170">-TemplateFile</span></span>
<span data-ttu-id="a9b5a-171">Percorso del file del modello.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-171">The path to the template file.</span></span>

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

### <span data-ttu-id="a9b5a-172">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="a9b5a-172">-VmPassword</span></span>
<span data-ttu-id="a9b5a-173">La password della VM.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-173">The password of the Vm.</span></span>

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

### <span data-ttu-id="a9b5a-174">-VmSku</span><span class="sxs-lookup"><span data-stu-id="a9b5a-174">-VmSku</span></span>
<span data-ttu-id="a9b5a-175">SKU VM.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-175">The Vm Sku.</span></span>

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

### <span data-ttu-id="a9b5a-176">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="a9b5a-176">-VmUserName</span></span>
<span data-ttu-id="a9b5a-177">Nome utente per la registrazione in VM.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-177">The user name for logging to Vm.</span></span>

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

### <span data-ttu-id="a9b5a-178">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a9b5a-178">-Confirm</span></span>
<span data-ttu-id="a9b5a-179">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9b5a-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9b5a-180">-WhatIf</span></span>
<span data-ttu-id="a9b5a-181">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-181">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9b5a-182">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9b5a-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9b5a-183">CommonParameters</span></span>
<span data-ttu-id="a9b5a-184">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9b5a-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9b5a-185">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9b5a-185">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9b5a-186">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a9b5a-186">INPUTS</span></span>

### <span data-ttu-id="a9b5a-187">System. String</span><span class="sxs-lookup"><span data-stu-id="a9b5a-187">System.String</span></span>

### <span data-ttu-id="a9b5a-188">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="a9b5a-188">System.Security.SecureString</span></span>

### <span data-ttu-id="a9b5a-189">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a9b5a-189">System.Int32</span></span>

### <span data-ttu-id="a9b5a-190">Microsoft. Azure. Commands. ServiceFabric. Models. OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="a9b5a-190">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="a9b5a-191">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9b5a-191">OUTPUTS</span></span>

### <span data-ttu-id="a9b5a-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="a9b5a-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="a9b5a-193">Note</span><span class="sxs-lookup"><span data-stu-id="a9b5a-193">NOTES</span></span>

## <span data-ttu-id="a9b5a-194">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9b5a-194">RELATED LINKS</span></span>
