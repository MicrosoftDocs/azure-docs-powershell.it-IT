---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
ms.openlocfilehash: 1f6a6d05bff2c012ca3b32abd16dca01cbe1707b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512608"
---
# <span data-ttu-id="93190-101">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="93190-101">New-AzureRmHDInsightClusterConfig</span></span>

## <span data-ttu-id="93190-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="93190-102">SYNOPSIS</span></span>
<span data-ttu-id="93190-103">Crea un oggetto di configurazione cluster non persistente che descrive una configurazione cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="93190-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93190-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93190-104">SYNTAX</span></span>

```
New-AzureRmHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93190-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93190-105">DESCRIPTION</span></span>
<span data-ttu-id="93190-106">Il cmdlet **New-AzureRmHDInsightClusterConfig** crea un oggetto non persistente che descrive una configurazione del cluster Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="93190-106">The **New-AzureRmHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="93190-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93190-107">EXAMPLES</span></span>

### <span data-ttu-id="93190-108">Esempio 1: creare un oggetto di configurazione del cluster</span><span class="sxs-lookup"><span data-stu-id="93190-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
            | New-AzureRmHDInsightCluster `
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

<span data-ttu-id="93190-109">Questo comando crea un oggetto di configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="93190-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="93190-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="93190-110">PARAMETERS</span></span>

### <span data-ttu-id="93190-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="93190-111">-AadTenantId</span></span>
<span data-ttu-id="93190-112">Specifica l'ID tenant di Azure AD che verrà usato quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="93190-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93190-113">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="93190-113">-CertificateFileContents</span></span>
<span data-ttu-id="93190-114">Specifica il contenuto del file del certificato che verrà usato quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="93190-114">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Byte[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93190-115">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="93190-115">-CertificateFilePath</span></span>
<span data-ttu-id="93190-116">Specifica il percorso del file del certificato che verrà usato per l'autenticazione come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="93190-116">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="93190-117">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="93190-117">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93190-118">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="93190-118">-CertificatePassword</span></span>
<span data-ttu-id="93190-119">Specifica la password per il certificato che verrà usato per l'autenticazione come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="93190-119">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="93190-120">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="93190-120">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93190-121">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="93190-121">-ClusterTier</span></span>
<span data-ttu-id="93190-122">Specifica il livello del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="93190-122">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="93190-123">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="93190-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="93190-124">Standard</span><span class="sxs-lookup"><span data-stu-id="93190-124">Standard</span></span>
- <span data-ttu-id="93190-125">Premium</span><span class="sxs-lookup"><span data-stu-id="93190-125">Premium</span></span>

<span data-ttu-id="93190-126">Il valore predefinito è standard.</span><span class="sxs-lookup"><span data-stu-id="93190-126">The default value is Standard.</span></span>
<span data-ttu-id="93190-127">Il livello Premium può essere usato solo con i cluster Linux e consente l'uso di alcune nuove funzionalità.</span><span class="sxs-lookup"><span data-stu-id="93190-127">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

```yaml
Type: Tier
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93190-128">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="93190-128">-ClusterType</span></span>
<span data-ttu-id="93190-129">Specifica il tipo di cluster da creare.</span><span class="sxs-lookup"><span data-stu-id="93190-129">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="93190-130">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="93190-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="93190-131">Hadoop</span><span class="sxs-lookup"><span data-stu-id="93190-131">Hadoop</span></span>
- <span data-ttu-id="93190-132">HBase</span><span class="sxs-lookup"><span data-stu-id="93190-132">HBase</span></span>
- <span data-ttu-id="93190-133">Tempesta</span><span class="sxs-lookup"><span data-stu-id="93190-133">Storm</span></span>
- <span data-ttu-id="93190-134">Scintilla</span><span class="sxs-lookup"><span data-stu-id="93190-134">Spark</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93190-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93190-135">-DefaultProfile</span></span>
<span data-ttu-id="93190-136">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="93190-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93190-137">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="93190-137">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="93190-138">Specifica la chiave dell'account per l'account di archiviazione di Azure predefinito che verrà usato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="93190-138">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93190-139">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="93190-139">-DefaultStorageAccountName</span></span>
<span data-ttu-id="93190-140">Specifica il nome dell'account di archiviazione predefinito che verrà usato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="93190-140">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93190-141">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="93190-141">-DefaultStorageAccountType</span></span>
<span data-ttu-id="93190-142">Specifica il tipo di account di archiviazione predefinito che verrà usato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="93190-142">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="93190-143">I valori possibili sono AzureStorage e AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="93190-143">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

```yaml
Type: StorageType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93190-144">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="93190-144">-EdgeNodeSize</span></span>
<span data-ttu-id="93190-145">Specifica le dimensioni della macchina virtuale per il nodo Edge.</span><span class="sxs-lookup"><span data-stu-id="93190-145">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="93190-146">Usare Get-AzureRmVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="93190-146">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="93190-147">Questo parametro è valido solo per i cluster RServer.</span><span class="sxs-lookup"><span data-stu-id="93190-147">This parameter is valid only for RServer clusters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93190-148">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="93190-148">-HeadNodeSize</span></span>
<span data-ttu-id="93190-149">Specifica le dimensioni della macchina virtuale per il nodo head.</span><span class="sxs-lookup"><span data-stu-id="93190-149">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="93190-150">Usare Get-AzureRMVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="93190-150">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93190-151">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="93190-151">-HiveMetastore</span></span>
<span data-ttu-id="93190-152">Specifica il Metastore per archiviare i metadati hive.</span><span class="sxs-lookup"><span data-stu-id="93190-152">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="93190-153">In alternativa, puoi usare il cmdlet Add-AzureRmHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="93190-153">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

```yaml
Type: AzureHDInsightMetastore
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93190-154">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="93190-154">-ObjectId</span></span>
<span data-ttu-id="93190-155">Specifica l'ID oggetto Azure AD (GUID) dell'entità servizio Azure AD che rappresenta il cluster.</span><span class="sxs-lookup"><span data-stu-id="93190-155">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="93190-156">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="93190-156">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93190-157">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="93190-157">-OozieMetastore</span></span>
<span data-ttu-id="93190-158">Specifica il Metastore per archiviare i metadati di oozie.</span><span class="sxs-lookup"><span data-stu-id="93190-158">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="93190-159">In alternativa, puoi usare il cmdlet **Add-AzureRmHDInsightMetastore** .</span><span class="sxs-lookup"><span data-stu-id="93190-159">You can alternatively use the **Add-AzureRmHDInsightMetastore** cmdlet.</span></span>

```yaml
Type: AzureHDInsightMetastore
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93190-160">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="93190-160">-WorkerNodeSize</span></span>
<span data-ttu-id="93190-161">Specifica le dimensioni della macchina virtuale per il nodo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="93190-161">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="93190-162">Usare Get-AzureRMVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="93190-162">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93190-163">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="93190-163">-ZookeeperNodeSize</span></span>
<span data-ttu-id="93190-164">Specifica le dimensioni della macchina virtuale per il nodo Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="93190-164">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="93190-165">Usare Get-AzureRMVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="93190-165">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="93190-166">Questo parametro è valido solo per i cluster HBase o Storm.</span><span class="sxs-lookup"><span data-stu-id="93190-166">This parameter is valid only for HBase or Storm clusters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93190-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93190-167">CommonParameters</span></span>
<span data-ttu-id="93190-168">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93190-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93190-169">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93190-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93190-170">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="93190-170">INPUTS</span></span>

### <span data-ttu-id="93190-171">Nessuno</span><span class="sxs-lookup"><span data-stu-id="93190-171">None</span></span>
<span data-ttu-id="93190-172">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="93190-172">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="93190-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93190-173">OUTPUTS</span></span>

### <span data-ttu-id="93190-174">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="93190-174">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="93190-175">Note</span><span class="sxs-lookup"><span data-stu-id="93190-175">NOTES</span></span>

## <span data-ttu-id="93190-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93190-176">RELATED LINKS</span></span>

[<span data-ttu-id="93190-177">Add-AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="93190-177">Add-AzureRmHDInsightStorage</span></span>](./Add-AzureRmHDInsightStorage.md)


