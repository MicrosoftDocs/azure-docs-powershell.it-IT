---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 66857c9d12bb23ffdccb893b8fae8bfc7c6e0f4f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032537"
---
# <span data-ttu-id="0ed11-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="0ed11-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="0ed11-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0ed11-102">SYNOPSIS</span></span>
<span data-ttu-id="0ed11-103">Crea un oggetto di configurazione cluster non persistente che descrive una configurazione cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0ed11-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="0ed11-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ed11-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-MinSupportedTlsVersion <String>]
 [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>]
 [-OutboundPublicNetworkAccessType <String>] [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ed11-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ed11-105">DESCRIPTION</span></span>
<span data-ttu-id="0ed11-106">Il cmdlet **New-AzHDInsightClusterConfig** crea un oggetto non persistente che descrive una configurazione del cluster Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0ed11-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="0ed11-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ed11-107">EXAMPLES</span></span>

### <span data-ttu-id="0ed11-108">Esempio 1: creare un oggetto di configurazione del cluster</span><span class="sxs-lookup"><span data-stu-id="0ed11-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="0ed11-109">Questo comando crea un oggetto di configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="0ed11-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="0ed11-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0ed11-110">PARAMETERS</span></span>

### <span data-ttu-id="0ed11-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="0ed11-111">-AadTenantId</span></span>
<span data-ttu-id="0ed11-112">Specifica l'ID tenant di Azure AD che verrà usato quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0ed11-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="0ed11-113">-ApplicationId</span></span>
<span data-ttu-id="0ed11-114">Ottiene o imposta l'ID dell'applicazione Principal del servizio per l'accesso a Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="0ed11-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-115">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="0ed11-115">-AssignedIdentity</span></span>
<span data-ttu-id="0ed11-116">Ottiene o imposta l'identità assegnata.</span><span class="sxs-lookup"><span data-stu-id="0ed11-116">Gets or sets the assigned identity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="0ed11-117">-CertificateFileContents</span></span>
<span data-ttu-id="0ed11-118">Specifica il contenuto del file del certificato che verrà usato quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0ed11-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="0ed11-119">-CertificateFilePath</span></span>
<span data-ttu-id="0ed11-120">Specifica il percorso del file del certificato che verrà usato per l'autenticazione come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="0ed11-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="0ed11-121">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0ed11-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="0ed11-122">-CertificatePassword</span></span>
<span data-ttu-id="0ed11-123">Specifica la password per il certificato che verrà usato per l'autenticazione come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="0ed11-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="0ed11-124">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0ed11-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="0ed11-125">-ClusterTier</span></span>
<span data-ttu-id="0ed11-126">Specifica il livello del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0ed11-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="0ed11-127">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0ed11-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0ed11-128">Standard</span><span class="sxs-lookup"><span data-stu-id="0ed11-128">Standard</span></span>
- <span data-ttu-id="0ed11-129">Premium il valore predefinito è standard.</span><span class="sxs-lookup"><span data-stu-id="0ed11-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="0ed11-130">Il livello Premium può essere usato solo con i cluster Linux e consente l'uso di alcune nuove funzionalità.</span><span class="sxs-lookup"><span data-stu-id="0ed11-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.Tier
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-131">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="0ed11-131">-ClusterType</span></span>
<span data-ttu-id="0ed11-132">Specifica il tipo di cluster da creare.</span><span class="sxs-lookup"><span data-stu-id="0ed11-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="0ed11-133">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0ed11-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0ed11-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="0ed11-134">Hadoop</span></span>
- <span data-ttu-id="0ed11-135">HBase</span><span class="sxs-lookup"><span data-stu-id="0ed11-135">HBase</span></span>
- <span data-ttu-id="0ed11-136">Tempesta</span><span class="sxs-lookup"><span data-stu-id="0ed11-136">Storm</span></span>
- <span data-ttu-id="0ed11-137">Scintilla</span><span class="sxs-lookup"><span data-stu-id="0ed11-137">Spark</span></span>
- <span data-ttu-id="0ed11-138">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="0ed11-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="0ed11-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="0ed11-139">Kafka</span></span>
- <span data-ttu-id="0ed11-140">RServer</span><span class="sxs-lookup"><span data-stu-id="0ed11-140">RServer</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ed11-141">-DefaultProfile</span></span>
<span data-ttu-id="0ed11-142">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0ed11-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ed11-143">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="0ed11-143">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="0ed11-144">Specifica la chiave dell'account per l'account di archiviazione di Azure predefinito che verrà usato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0ed11-144">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-145">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0ed11-145">-DefaultStorageAccountName</span></span>
<span data-ttu-id="0ed11-146">Specifica il nome dell'account di archiviazione predefinito che verrà usato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0ed11-146">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-147">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="0ed11-147">-DefaultStorageAccountType</span></span>
<span data-ttu-id="0ed11-148">Specifica il tipo di account di archiviazione predefinito che verrà usato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0ed11-148">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="0ed11-149">I valori possibili sono AzureStorage e AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="0ed11-149">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-150">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="0ed11-150">-EdgeNodeSize</span></span>
<span data-ttu-id="0ed11-151">Specifica le dimensioni della macchina virtuale per il nodo Edge.</span><span class="sxs-lookup"><span data-stu-id="0ed11-151">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="0ed11-152">Usare Get-AzVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0ed11-152">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="0ed11-153">Questo parametro è valido solo per i cluster RServer.</span><span class="sxs-lookup"><span data-stu-id="0ed11-153">This parameter is valid only for RServer clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-154">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="0ed11-154">-EncryptionAlgorithm</span></span>
<span data-ttu-id="0ed11-155">Ottiene o imposta l'algoritmo di crittografia.</span><span class="sxs-lookup"><span data-stu-id="0ed11-155">Gets or sets the encryption algorithm.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA-OAEP-256, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-156">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="0ed11-156">-EncryptionAtHost</span></span>
<span data-ttu-id="0ed11-157">Ottiene o imposta il contrassegno che indica se abilitare la crittografia in host o meno.</span><span class="sxs-lookup"><span data-stu-id="0ed11-157">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-158">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="0ed11-158">-EncryptionInTransit</span></span>
<span data-ttu-id="0ed11-159">Ottiene o imposta il contrassegno che indica se abilitare la crittografia in transito o meno.</span><span class="sxs-lookup"><span data-stu-id="0ed11-159">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-160">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="0ed11-160">-EncryptionKeyName</span></span>
<span data-ttu-id="0ed11-161">Ottiene o imposta il nome della chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="0ed11-161">Gets or sets the encryption key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-162">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="0ed11-162">-EncryptionKeyVersion</span></span>
<span data-ttu-id="0ed11-163">Ottiene o imposta la versione della chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="0ed11-163">Gets or sets the encryption key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-164">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="0ed11-164">-EncryptionVaultUri</span></span>
<span data-ttu-id="0ed11-165">Ottiene o imposta l'URI del Vault di crittografia.</span><span class="sxs-lookup"><span data-stu-id="0ed11-165">Gets or sets the encryption vault uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-166">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="0ed11-166">-HeadNodeSize</span></span>
<span data-ttu-id="0ed11-167">Specifica le dimensioni della macchina virtuale per il nodo head.</span><span class="sxs-lookup"><span data-stu-id="0ed11-167">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="0ed11-168">Usare Get-AzVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0ed11-168">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-169">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="0ed11-169">-HiveMetastore</span></span>
<span data-ttu-id="0ed11-170">Specifica il Metastore per archiviare i metadati hive.</span><span class="sxs-lookup"><span data-stu-id="0ed11-170">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="0ed11-171">In alternativa, puoi usare il cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="0ed11-171">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-172">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="0ed11-172">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="0ed11-173">Ottiene o imposta la versione di TLS supportata minima.</span><span class="sxs-lookup"><span data-stu-id="0ed11-173">Gets or sets the minimal supported TLS version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-174">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0ed11-174">-ObjectId</span></span>
<span data-ttu-id="0ed11-175">Specifica l'ID oggetto Azure AD (GUID) dell'entità servizio Azure AD che rappresenta il cluster.</span><span class="sxs-lookup"><span data-stu-id="0ed11-175">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="0ed11-176">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0ed11-176">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-177">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="0ed11-177">-OozieMetastore</span></span>
<span data-ttu-id="0ed11-178">Specifica il Metastore per archiviare i metadati di oozie.</span><span class="sxs-lookup"><span data-stu-id="0ed11-178">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="0ed11-179">In alternativa, puoi usare il cmdlet **Add-AzHDInsightMetastore** .</span><span class="sxs-lookup"><span data-stu-id="0ed11-179">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-180">-OutboundPublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="0ed11-180">-OutboundPublicNetworkAccessType</span></span>
<span data-ttu-id="0ed11-181">Ottiene o imposta il tipo di accesso in uscita alla rete pubblica.</span><span class="sxs-lookup"><span data-stu-id="0ed11-181">Gets or sets the outbound access type to the public network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PublicLoadBalancer, UDR

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-182">-PublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="0ed11-182">-PublicNetworkAccessType</span></span>
<span data-ttu-id="0ed11-183">Ottiene o imposta il tipo di accesso alla rete pubblica.</span><span class="sxs-lookup"><span data-stu-id="0ed11-183">Gets or sets the public network access type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: InboundAndOutbound, OutboundOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-184">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="0ed11-184">-WorkerNodeSize</span></span>
<span data-ttu-id="0ed11-185">Specifica le dimensioni della macchina virtuale per il nodo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0ed11-185">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="0ed11-186">Usare Get-AzVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0ed11-186">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-187">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="0ed11-187">-ZookeeperNodeSize</span></span>
<span data-ttu-id="0ed11-188">Specifica le dimensioni della macchina virtuale per il nodo Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="0ed11-188">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="0ed11-189">Usare Get-AzVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0ed11-189">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="0ed11-190">Questo parametro è valido solo per i cluster HBase o Storm.</span><span class="sxs-lookup"><span data-stu-id="0ed11-190">This parameter is valid only for HBase or Storm clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed11-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ed11-191">CommonParameters</span></span>
<span data-ttu-id="0ed11-192">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ed11-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ed11-193">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ed11-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ed11-194">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0ed11-194">INPUTS</span></span>

### <span data-ttu-id="0ed11-195">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0ed11-195">None</span></span>

## <span data-ttu-id="0ed11-196">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ed11-196">OUTPUTS</span></span>

### <span data-ttu-id="0ed11-197">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="0ed11-197">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="0ed11-198">Note</span><span class="sxs-lookup"><span data-stu-id="0ed11-198">NOTES</span></span>

## <span data-ttu-id="0ed11-199">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ed11-199">RELATED LINKS</span></span>

[<span data-ttu-id="0ed11-200">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="0ed11-200">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


