---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: b5ae1de58a7c3862379e73e852d7b367063c3629
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009022"
---
# <span data-ttu-id="3d27e-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="3d27e-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="3d27e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d27e-102">SYNOPSIS</span></span>
<span data-ttu-id="3d27e-103">Crea un oggetto di configurazione cluster non persistente che descrive una configurazione cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3d27e-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="3d27e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d27e-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-StorageAccountResourceId <String>] [-StorageAccountKey <String>]
 [-StorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-MinSupportedTlsVersion <String>]
 [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d27e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3d27e-105">DESCRIPTION</span></span>
<span data-ttu-id="3d27e-106">Il cmdlet **New-AzHDInsightClusterConfig crea** un oggetto non persistente che descrive una configurazione del cluster Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3d27e-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="3d27e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d27e-107">EXAMPLES</span></span>

### <span data-ttu-id="3d27e-108">Esempio 1: Creare un oggetto configurazione cluster</span><span class="sxs-lookup"><span data-stu-id="3d27e-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageaccountname"
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
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

<span data-ttu-id="3d27e-109">Questo comando crea un oggetto configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="3d27e-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="3d27e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d27e-110">PARAMETERS</span></span>

### <span data-ttu-id="3d27e-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="3d27e-111">-AadTenantId</span></span>
<span data-ttu-id="3d27e-112">Specifica l'ID tenant di Azure AD che verrà usato quando si accede ad Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3d27e-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3d27e-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3d27e-113">-ApplicationId</span></span>
<span data-ttu-id="3d27e-114">Ottiene o imposta l'ID applicazione entità servizio per l'accesso ad Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="3d27e-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="3d27e-115">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="3d27e-115">-AssignedIdentity</span></span>
<span data-ttu-id="3d27e-116">Ottiene o imposta l'identità assegnata.</span><span class="sxs-lookup"><span data-stu-id="3d27e-116">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="3d27e-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="3d27e-117">-CertificateFileContents</span></span>
<span data-ttu-id="3d27e-118">Specifica il contenuto del file del certificato che verrà usato quando si accede ad Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3d27e-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3d27e-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="3d27e-119">-CertificateFilePath</span></span>
<span data-ttu-id="3d27e-120">Specifica il percorso del file del certificato che verrà usato per l'autenticazione come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="3d27e-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="3d27e-121">Il cluster userà questa impostazione per l'accesso ad Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3d27e-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3d27e-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="3d27e-122">-CertificatePassword</span></span>
<span data-ttu-id="3d27e-123">Specifica la password per il certificato che verrà usato per l'autenticazione come entità servizio.</span><span class="sxs-lookup"><span data-stu-id="3d27e-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="3d27e-124">Il cluster userà questa impostazione per l'accesso ad Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3d27e-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3d27e-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="3d27e-125">-ClusterTier</span></span>
<span data-ttu-id="3d27e-126">Specifica il livello cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3d27e-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="3d27e-127">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="3d27e-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3d27e-128">Standard</span><span class="sxs-lookup"><span data-stu-id="3d27e-128">Standard</span></span>
- <span data-ttu-id="3d27e-129">Premium Il valore predefinito è Standard.</span><span class="sxs-lookup"><span data-stu-id="3d27e-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="3d27e-130">Il livello Premium può essere usato solo con cluster Linux e consente l'uso di alcune nuove funzionalità.</span><span class="sxs-lookup"><span data-stu-id="3d27e-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="3d27e-131">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="3d27e-131">-ClusterType</span></span>
<span data-ttu-id="3d27e-132">Specifica il tipo di cluster da creare.</span><span class="sxs-lookup"><span data-stu-id="3d27e-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="3d27e-133">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="3d27e-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3d27e-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="3d27e-134">Hadoop</span></span>
- <span data-ttu-id="3d27e-135">HBase</span><span class="sxs-lookup"><span data-stu-id="3d27e-135">HBase</span></span>
- <span data-ttu-id="3d27e-136">Temporale</span><span class="sxs-lookup"><span data-stu-id="3d27e-136">Storm</span></span>
- <span data-ttu-id="3d27e-137">Grafico spark</span><span class="sxs-lookup"><span data-stu-id="3d27e-137">Spark</span></span>
- <span data-ttu-id="3d27e-138">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="3d27e-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="3d27e-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="3d27e-139">Kafka</span></span>
- <span data-ttu-id="3d27e-140">RServer</span><span class="sxs-lookup"><span data-stu-id="3d27e-140">RServer</span></span>

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

### <span data-ttu-id="3d27e-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d27e-141">-DefaultProfile</span></span>
<span data-ttu-id="3d27e-142">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3d27e-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d27e-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="3d27e-143">-EdgeNodeSize</span></span>
<span data-ttu-id="3d27e-144">Specifica le dimensioni della macchina virtuale per il nodo Edge.</span><span class="sxs-lookup"><span data-stu-id="3d27e-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="3d27e-145">Usa Get-AzVMSize per dimensioni accettabili di VM e consulta la pagina dei prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3d27e-145">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="3d27e-146">Questo parametro è valido solo per i cluster RServer.</span><span class="sxs-lookup"><span data-stu-id="3d27e-146">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="3d27e-147">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="3d27e-147">-EncryptionAlgorithm</span></span>
<span data-ttu-id="3d27e-148">Ottiene o imposta l'algoritmo di crittografia.</span><span class="sxs-lookup"><span data-stu-id="3d27e-148">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="3d27e-149">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="3d27e-149">-EncryptionAtHost</span></span>
<span data-ttu-id="3d27e-150">Ottiene o imposta il flag che indica se abilitare o meno la crittografia nell'host.</span><span class="sxs-lookup"><span data-stu-id="3d27e-150">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="3d27e-151">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="3d27e-151">-EncryptionInTransit</span></span>
<span data-ttu-id="3d27e-152">Ottiene o imposta il flag che indica se abilitare o meno la crittografia in transito.</span><span class="sxs-lookup"><span data-stu-id="3d27e-152">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="3d27e-153">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="3d27e-153">-EncryptionKeyName</span></span>
<span data-ttu-id="3d27e-154">Ottiene o imposta il nome della chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="3d27e-154">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="3d27e-155">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="3d27e-155">-EncryptionKeyVersion</span></span>
<span data-ttu-id="3d27e-156">Ottiene o imposta la versione della chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="3d27e-156">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="3d27e-157">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="3d27e-157">-EncryptionVaultUri</span></span>
<span data-ttu-id="3d27e-158">Ottiene o imposta l'URI del vault di crittografia.</span><span class="sxs-lookup"><span data-stu-id="3d27e-158">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="3d27e-159">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="3d27e-159">-HeadNodeSize</span></span>
<span data-ttu-id="3d27e-160">Specifica le dimensioni della macchina virtuale per il nodo Head.</span><span class="sxs-lookup"><span data-stu-id="3d27e-160">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="3d27e-161">Usa Get-AzVMSize per dimensioni accettabili di VM e consulta la pagina dei prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3d27e-161">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="3d27e-162">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="3d27e-162">-HiveMetastore</span></span>
<span data-ttu-id="3d27e-163">Specifica il metastore in cui archiviare i metadati Hive.</span><span class="sxs-lookup"><span data-stu-id="3d27e-163">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="3d27e-164">In alternativa, è possibile usare Add-AzHDInsightMetastore cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d27e-164">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="3d27e-165">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="3d27e-165">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="3d27e-166">Ottiene o imposta la versione minima di TLS supportata.</span><span class="sxs-lookup"><span data-stu-id="3d27e-166">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="3d27e-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3d27e-167">-ObjectId</span></span>
<span data-ttu-id="3d27e-168">Specifica l'ID oggetto di Azure AD (un GUID) dell'entità servizio di Azure AD che rappresenta il cluster.</span><span class="sxs-lookup"><span data-stu-id="3d27e-168">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="3d27e-169">Il cluster userà questa impostazione per l'accesso ad Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3d27e-169">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3d27e-170">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="3d27e-170">-OozieMetastore</span></span>
<span data-ttu-id="3d27e-171">Specifica il metastore in cui archiviare i metadati di Oozie.</span><span class="sxs-lookup"><span data-stu-id="3d27e-171">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="3d27e-172">In alternativa, è possibile usare il cmdlet **Add-AzHDInsightMetastore.**</span><span class="sxs-lookup"><span data-stu-id="3d27e-172">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="3d27e-173">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3d27e-173">-StorageAccountKey</span></span>
<span data-ttu-id="3d27e-174">Ottiene o imposta la chiave di accesso dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3d27e-174">Gets or sets the storage account access key.</span></span>

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

### <span data-ttu-id="3d27e-175">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="3d27e-175">-StorageAccountResourceId</span></span>
<span data-ttu-id="3d27e-176">Ottiene o imposta l'ID risorsa dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3d27e-176">Gets or sets the storage account resource id.</span></span>

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

### <span data-ttu-id="3d27e-177">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="3d27e-177">-StorageAccountType</span></span>
<span data-ttu-id="3d27e-178">Ottiene o imposta il tipo di account di archiviazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="3d27e-178">Gets or sets the type of the default storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d27e-179">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="3d27e-179">-WorkerNodeSize</span></span>
<span data-ttu-id="3d27e-180">Specifica le dimensioni della macchina virtuale per il nodo Worker.</span><span class="sxs-lookup"><span data-stu-id="3d27e-180">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="3d27e-181">Usa Get-AzVMSize per dimensioni accettabili di VM e consulta la pagina dei prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3d27e-181">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="3d27e-182">-MetriakeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="3d27e-182">-ZookeeperNodeSize</span></span>
<span data-ttu-id="3d27e-183">Specifica le dimensioni della macchina virtuale per il nodo Guardiano.</span><span class="sxs-lookup"><span data-stu-id="3d27e-183">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="3d27e-184">Usa Get-AzVMSize per dimensioni accettabili di VM e consulta la pagina dei prezzi di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3d27e-184">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="3d27e-185">Questo parametro è valido solo per cluster HBase o Storm.</span><span class="sxs-lookup"><span data-stu-id="3d27e-185">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="3d27e-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d27e-186">CommonParameters</span></span>
<span data-ttu-id="3d27e-187">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d27e-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d27e-188">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3d27e-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d27e-189">INPUT</span><span class="sxs-lookup"><span data-stu-id="3d27e-189">INPUTS</span></span>

### <span data-ttu-id="3d27e-190">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3d27e-190">None</span></span>

## <span data-ttu-id="3d27e-191">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d27e-191">OUTPUTS</span></span>

### <span data-ttu-id="3d27e-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="3d27e-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="3d27e-193">NOTE</span><span class="sxs-lookup"><span data-stu-id="3d27e-193">NOTES</span></span>

## <span data-ttu-id="3d27e-194">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d27e-194">RELATED LINKS</span></span>

[<span data-ttu-id="3d27e-195">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="3d27e-195">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


