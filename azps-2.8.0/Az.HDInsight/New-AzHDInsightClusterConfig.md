---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: fad988977cf5fe24e440d654206e0f1a212be6b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674307"
---
# <span data-ttu-id="3598c-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="3598c-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="3598c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3598c-102">SYNOPSIS</span></span>
<span data-ttu-id="3598c-103">Crea un oggetto di configurazione cluster non persistente che descrive una configurazione cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3598c-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="3598c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3598c-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3598c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3598c-105">DESCRIPTION</span></span>
<span data-ttu-id="3598c-106">Il cmdlet **New-AzHDInsightClusterConfig** crea un oggetto non persistente che descrive una configurazione del cluster Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3598c-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="3598c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3598c-107">EXAMPLES</span></span>

### <span data-ttu-id="3598c-108">Esempio 1: creare un oggetto di configurazione del cluster</span><span class="sxs-lookup"><span data-stu-id="3598c-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="3598c-109">Questo comando crea un oggetto di configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="3598c-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="3598c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3598c-110">PARAMETERS</span></span>

### <span data-ttu-id="3598c-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="3598c-111">-AadTenantId</span></span>
<span data-ttu-id="3598c-112">Specifica l'ID tenant di Azure AD che verrà usato quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3598c-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3598c-113">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="3598c-113">-CertificateFileContents</span></span>
<span data-ttu-id="3598c-114">Specifica il contenuto del file del certificato che verrà usato quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3598c-114">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3598c-115">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="3598c-115">-CertificateFilePath</span></span>
<span data-ttu-id="3598c-116">Specifica il percorso del file del certificato che verrà usato per l'autenticazione come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="3598c-116">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="3598c-117">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3598c-117">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3598c-118">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="3598c-118">-CertificatePassword</span></span>
<span data-ttu-id="3598c-119">Specifica la password per il certificato che verrà usato per l'autenticazione come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="3598c-119">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="3598c-120">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3598c-120">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3598c-121">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="3598c-121">-ClusterTier</span></span>
<span data-ttu-id="3598c-122">Specifica il livello del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3598c-122">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="3598c-123">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3598c-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3598c-124">Standard</span><span class="sxs-lookup"><span data-stu-id="3598c-124">Standard</span></span>
- <span data-ttu-id="3598c-125">Premium il valore predefinito è standard.</span><span class="sxs-lookup"><span data-stu-id="3598c-125">Premium The default value is Standard.</span></span>
<span data-ttu-id="3598c-126">Il livello Premium può essere usato solo con i cluster Linux e consente l'uso di alcune nuove funzionalità.</span><span class="sxs-lookup"><span data-stu-id="3598c-126">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="3598c-127">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="3598c-127">-ClusterType</span></span>
<span data-ttu-id="3598c-128">Specifica il tipo di cluster da creare.</span><span class="sxs-lookup"><span data-stu-id="3598c-128">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="3598c-129">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3598c-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3598c-130">Hadoop</span><span class="sxs-lookup"><span data-stu-id="3598c-130">Hadoop</span></span>
- <span data-ttu-id="3598c-131">HBase</span><span class="sxs-lookup"><span data-stu-id="3598c-131">HBase</span></span>
- <span data-ttu-id="3598c-132">Tempesta</span><span class="sxs-lookup"><span data-stu-id="3598c-132">Storm</span></span>
- <span data-ttu-id="3598c-133">Scintilla</span><span class="sxs-lookup"><span data-stu-id="3598c-133">Spark</span></span>

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

### <span data-ttu-id="3598c-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3598c-134">-DefaultProfile</span></span>
<span data-ttu-id="3598c-135">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3598c-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3598c-136">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3598c-136">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="3598c-137">Specifica la chiave dell'account per l'account di archiviazione di Azure predefinito che verrà usato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3598c-137">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="3598c-138">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3598c-138">-DefaultStorageAccountName</span></span>
<span data-ttu-id="3598c-139">Specifica il nome dell'account di archiviazione predefinito che verrà usato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3598c-139">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="3598c-140">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="3598c-140">-DefaultStorageAccountType</span></span>
<span data-ttu-id="3598c-141">Specifica il tipo di account di archiviazione predefinito che verrà usato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3598c-141">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="3598c-142">I valori possibili sono AzureStorage e AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="3598c-142">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="3598c-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="3598c-143">-EdgeNodeSize</span></span>
<span data-ttu-id="3598c-144">Specifica le dimensioni della macchina virtuale per il nodo Edge.</span><span class="sxs-lookup"><span data-stu-id="3598c-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="3598c-145">Usare Get-AzVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3598c-145">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="3598c-146">Questo parametro è valido solo per i cluster RServer.</span><span class="sxs-lookup"><span data-stu-id="3598c-146">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="3598c-147">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="3598c-147">-HeadNodeSize</span></span>
<span data-ttu-id="3598c-148">Specifica le dimensioni della macchina virtuale per il nodo head.</span><span class="sxs-lookup"><span data-stu-id="3598c-148">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="3598c-149">Usare Get-AzVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3598c-149">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="3598c-150">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="3598c-150">-HiveMetastore</span></span>
<span data-ttu-id="3598c-151">Specifica il Metastore per archiviare i metadati hive.</span><span class="sxs-lookup"><span data-stu-id="3598c-151">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="3598c-152">In alternativa, puoi usare il cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="3598c-152">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="3598c-153">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3598c-153">-ObjectId</span></span>
<span data-ttu-id="3598c-154">Specifica l'ID oggetto Azure AD (GUID) dell'entità servizio Azure AD che rappresenta il cluster.</span><span class="sxs-lookup"><span data-stu-id="3598c-154">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="3598c-155">Il cluster utilizzerà questo aspetto quando si accede a Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3598c-155">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3598c-156">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="3598c-156">-OozieMetastore</span></span>
<span data-ttu-id="3598c-157">Specifica il Metastore per archiviare i metadati di oozie.</span><span class="sxs-lookup"><span data-stu-id="3598c-157">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="3598c-158">In alternativa, puoi usare il cmdlet **Add-AzHDInsightMetastore** .</span><span class="sxs-lookup"><span data-stu-id="3598c-158">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="3598c-159">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="3598c-159">-WorkerNodeSize</span></span>
<span data-ttu-id="3598c-160">Specifica le dimensioni della macchina virtuale per il nodo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3598c-160">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="3598c-161">Usare Get-AzVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3598c-161">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="3598c-162">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="3598c-162">-ZookeeperNodeSize</span></span>
<span data-ttu-id="3598c-163">Specifica le dimensioni della macchina virtuale per il nodo Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="3598c-163">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="3598c-164">Usare Get-AzVMSize per le dimensioni VM accettabili e vedere la pagina relativa ai prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3598c-164">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="3598c-165">Questo parametro è valido solo per i cluster HBase o Storm.</span><span class="sxs-lookup"><span data-stu-id="3598c-165">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="3598c-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3598c-166">CommonParameters</span></span>
<span data-ttu-id="3598c-167">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3598c-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3598c-168">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3598c-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3598c-169">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3598c-169">INPUTS</span></span>

### <span data-ttu-id="3598c-170">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3598c-170">None</span></span>

## <span data-ttu-id="3598c-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3598c-171">OUTPUTS</span></span>

### <span data-ttu-id="3598c-172">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="3598c-172">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="3598c-173">Note</span><span class="sxs-lookup"><span data-stu-id="3598c-173">NOTES</span></span>

## <span data-ttu-id="3598c-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3598c-174">RELATED LINKS</span></span>

[<span data-ttu-id="3598c-175">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="3598c-175">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


