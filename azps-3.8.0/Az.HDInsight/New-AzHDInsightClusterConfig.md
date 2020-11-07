---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 38dc23c2bebe3c608833e55bcb4ffb2d687f9041
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865457"
---
# <span data-ttu-id="77f79-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="77f79-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="77f79-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="77f79-102">SYNOPSIS</span></span>
<span data-ttu-id="77f79-103">Crea un oggetto di configurazione cluster non persistente che descrive una configurazione cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="77f79-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="77f79-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77f79-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [[-DefaultStorageAccountType] <StorageType>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>] [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>]
 [[-EdgeNodeSize] <String>] [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>] [[-ClusterTier] <Tier>]
 [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>] [[-CertificateFileContents] <Byte[]>]
 [[-CertificateFilePath] <String>] [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>]
 [[-MinSupportedTlsVersion] <String>] [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77f79-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77f79-105">DESCRIPTION</span></span>
<span data-ttu-id="77f79-106">Il cmdlet **New-AzHDInsightClusterConfig** crea un oggetto non persistente che descrive una configurazione del cluster Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="77f79-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="77f79-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77f79-107">EXAMPLES</span></span>

### <span data-ttu-id="77f79-108">Esempio 1: creare un oggetto di configurazione del cluster</span><span class="sxs-lookup"><span data-stu-id="77f79-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="77f79-109">Questo comando crea un oggetto di configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="77f79-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="77f79-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="77f79-110">PARAMETERS</span></span>

### <span data-ttu-id="77f79-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="77f79-111">-AadTenantId</span></span>
<span data-ttu-id="77f79-112">Specifica l'ID tenant di Azure AD che verrà usato quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="77f79-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="77f79-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="77f79-113">-ApplicationId</span></span>
<span data-ttu-id="77f79-114">Ottiene o imposta l'ID dell'applicazione Principal del servizio per l'accesso a Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="77f79-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="77f79-115">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="77f79-115">-CertificateFileContents</span></span>
<span data-ttu-id="77f79-116">Specifica il contenuto del file del certificato che verrà usato quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="77f79-116">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="77f79-117">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="77f79-117">-CertificateFilePath</span></span>
<span data-ttu-id="77f79-118">Specifica il percorso del file del certificato che verrà usato per l'autenticazione come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="77f79-118">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="77f79-119">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="77f79-119">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="77f79-120">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="77f79-120">-CertificatePassword</span></span>
<span data-ttu-id="77f79-121">Specifica la password per il certificato che verrà usato per l'autenticazione come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="77f79-121">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="77f79-122">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="77f79-122">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="77f79-123">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="77f79-123">-ClusterTier</span></span>
<span data-ttu-id="77f79-124">Specifica il livello del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="77f79-124">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="77f79-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="77f79-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="77f79-126">Standard</span><span class="sxs-lookup"><span data-stu-id="77f79-126">Standard</span></span>
- <span data-ttu-id="77f79-127">Premium il valore predefinito è standard.</span><span class="sxs-lookup"><span data-stu-id="77f79-127">Premium The default value is Standard.</span></span>
<span data-ttu-id="77f79-128">Il livello Premium può essere usato solo con i cluster Linux e consente l'uso di alcune nuove funzionalità.</span><span class="sxs-lookup"><span data-stu-id="77f79-128">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="77f79-129">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="77f79-129">-ClusterType</span></span>
<span data-ttu-id="77f79-130">Specifica il tipo di cluster da creare.</span><span class="sxs-lookup"><span data-stu-id="77f79-130">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="77f79-131">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="77f79-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="77f79-132">Hadoop</span><span class="sxs-lookup"><span data-stu-id="77f79-132">Hadoop</span></span>
- <span data-ttu-id="77f79-133">HBase</span><span class="sxs-lookup"><span data-stu-id="77f79-133">HBase</span></span>
- <span data-ttu-id="77f79-134">Tempesta</span><span class="sxs-lookup"><span data-stu-id="77f79-134">Storm</span></span>
- <span data-ttu-id="77f79-135">Scintilla</span><span class="sxs-lookup"><span data-stu-id="77f79-135">Spark</span></span>
- <span data-ttu-id="77f79-136">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="77f79-136">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="77f79-137">Kafka</span><span class="sxs-lookup"><span data-stu-id="77f79-137">Kafka</span></span>
- <span data-ttu-id="77f79-138">RServer</span><span class="sxs-lookup"><span data-stu-id="77f79-138">RServer</span></span>

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

### <span data-ttu-id="77f79-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77f79-139">-DefaultProfile</span></span>
<span data-ttu-id="77f79-140">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="77f79-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77f79-141">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="77f79-141">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="77f79-142">Specifica la chiave dell'account per l'account di archiviazione di Azure predefinito che verrà usato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="77f79-142">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="77f79-143">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="77f79-143">-DefaultStorageAccountName</span></span>
<span data-ttu-id="77f79-144">Specifica il nome dell'account di archiviazione predefinito che verrà usato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="77f79-144">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="77f79-145">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="77f79-145">-DefaultStorageAccountType</span></span>
<span data-ttu-id="77f79-146">Specifica il tipo di account di archiviazione predefinito che verrà usato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="77f79-146">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="77f79-147">I valori possibili sono AzureStorage e AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="77f79-147">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="77f79-148">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="77f79-148">-EdgeNodeSize</span></span>
<span data-ttu-id="77f79-149">Specifica le dimensioni della macchina virtuale per il nodo Edge.</span><span class="sxs-lookup"><span data-stu-id="77f79-149">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="77f79-150">Usare Get-AzVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="77f79-150">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="77f79-151">Questo parametro è valido solo per i cluster RServer.</span><span class="sxs-lookup"><span data-stu-id="77f79-151">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="77f79-152">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="77f79-152">-HeadNodeSize</span></span>
<span data-ttu-id="77f79-153">Specifica le dimensioni della macchina virtuale per il nodo head.</span><span class="sxs-lookup"><span data-stu-id="77f79-153">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="77f79-154">Usare Get-AzVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="77f79-154">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="77f79-155">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="77f79-155">-HiveMetastore</span></span>
<span data-ttu-id="77f79-156">Specifica il Metastore per archiviare i metadati hive.</span><span class="sxs-lookup"><span data-stu-id="77f79-156">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="77f79-157">In alternativa, puoi usare il cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="77f79-157">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="77f79-158">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="77f79-158">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="77f79-159">Ottiene o imposta la versione di TLS supportata minima.</span><span class="sxs-lookup"><span data-stu-id="77f79-159">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="77f79-160">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="77f79-160">-ObjectId</span></span>
<span data-ttu-id="77f79-161">Specifica l'ID oggetto Azure AD (GUID) dell'entità servizio Azure AD che rappresenta il cluster.</span><span class="sxs-lookup"><span data-stu-id="77f79-161">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="77f79-162">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="77f79-162">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="77f79-163">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="77f79-163">-OozieMetastore</span></span>
<span data-ttu-id="77f79-164">Specifica il Metastore per archiviare i metadati di oozie.</span><span class="sxs-lookup"><span data-stu-id="77f79-164">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="77f79-165">In alternativa, puoi usare il cmdlet **Add-AzHDInsightMetastore** .</span><span class="sxs-lookup"><span data-stu-id="77f79-165">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="77f79-166">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="77f79-166">-WorkerNodeSize</span></span>
<span data-ttu-id="77f79-167">Specifica le dimensioni della macchina virtuale per il nodo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="77f79-167">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="77f79-168">Usare Get-AzVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="77f79-168">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="77f79-169">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="77f79-169">-ZookeeperNodeSize</span></span>
<span data-ttu-id="77f79-170">Specifica le dimensioni della macchina virtuale per il nodo Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="77f79-170">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="77f79-171">Usare Get-AzVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="77f79-171">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="77f79-172">Questo parametro è valido solo per i cluster HBase o Storm.</span><span class="sxs-lookup"><span data-stu-id="77f79-172">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="77f79-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77f79-173">CommonParameters</span></span>
<span data-ttu-id="77f79-174">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77f79-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77f79-175">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77f79-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77f79-176">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="77f79-176">INPUTS</span></span>

### <span data-ttu-id="77f79-177">Nessuno</span><span class="sxs-lookup"><span data-stu-id="77f79-177">None</span></span>

## <span data-ttu-id="77f79-178">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77f79-178">OUTPUTS</span></span>

### <span data-ttu-id="77f79-179">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="77f79-179">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="77f79-180">Note</span><span class="sxs-lookup"><span data-stu-id="77f79-180">NOTES</span></span>

## <span data-ttu-id="77f79-181">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77f79-181">RELATED LINKS</span></span>

[<span data-ttu-id="77f79-182">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="77f79-182">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


