---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8BD3B8BD-DC87-4A94-9FCA-611D11D5E065
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightmetastore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightMetastore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightMetastore.md
ms.openlocfilehash: 8102a9ce8ef1117822426d6896edf95d21c46607
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185910"
---
# <span data-ttu-id="c5084-101">Add-AzHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="c5084-101">Add-AzHDInsightMetastore</span></span>

## <span data-ttu-id="c5084-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5084-102">SYNOPSIS</span></span>
<span data-ttu-id="c5084-103">Aggiunge un SQL dati da fungere da hive o metastore Oozie a un oggetto configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="c5084-103">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

## <span data-ttu-id="c5084-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5084-104">SYNTAX</span></span>

```
Add-AzHDInsightMetastore [-Config] <AzureHDInsightConfig> [-MetastoreType] <AzureHDInsightMetastoreType>
 [-SqlAzureServerName] <String> [-DatabaseName] <String> [-Credential] <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5084-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c5084-105">DESCRIPTION</span></span>
<span data-ttu-id="c5084-106">Il cmdlet **Add-AzHDInsightMetastore** aggiunge un metastore Hive o Oozie all'oggetto di configurazione HDInsight creato dal cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="c5084-106">The **Add-AzHDInsightMetastore** cmdlet adds a Hive or Oozie metastore to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="c5084-107">Un metastore è un SQL dati dati che può essere usato per archiviare i metadati per Hive, Oozie o entrambi.</span><span class="sxs-lookup"><span data-stu-id="c5084-107">A metastore is a SQL Database that can used to store metadata for Hive, Oozie, or both.</span></span>

## <span data-ttu-id="c5084-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5084-108">EXAMPLES</span></span>

### <span data-ttu-id="c5084-109">Esempio 1: Aggiungere un metastore SQL di database all'oggetto di configurazione del cluster</span><span class="sxs-lookup"><span data-stu-id="c5084-109">Example 1: Add a SQL database metastore to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Hive metastore info
PS C:\> $hiveSqlServer = "your-sqlserver-001"
PS C:\> $hiveDb = "your-sqldb-001"
PS C:\> $hiveCreds = Get-Credential

# Oozie metastore info
PS C:\> $oozieSqlServer = "your-sqlserver-001"
PS C:\> $oozieDb = "your-sqldb-002"
PS C:\> $oozieCreds = Get-Credential

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig  `
            | Add-AzHDInsightMetastore `
                -SqlAzureServerName "$oozieSqlServer.database.contoso.net" `
                -DatabaseName $oozieDb `
                -Credential $oozieCreds `
                -MetastoreType OozieMetastore `
            | Add-AzHDInsightMetastore `
                -SqlAzureServerName "$hiveSqlServer.database.contoso.net" `
                -DatabaseName $hiveDb `
                -Credential $hiveCreds `
                -MetastoreType HiveMetastore `
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

<span data-ttu-id="c5084-110">Questo comando aggiunge un metastore SQL di database al cluster denominato your-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="c5084-110">This command adds a SQL database metastore to the cluster named your-hadoop-001.</span></span>

### <span data-ttu-id="c5084-111">Esempio 2: Aggiungere un database Ambari personalizzato all'oggetto di configurazione del cluster</span><span class="sxs-lookup"><span data-stu-id="c5084-111">Example 2: Add a custom Ambari database to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Custom Amari database info
PS C:\> $ambariSqlServer = "your-sqlserver-001"
PS C:\> $ambariDb = "your-sqldb-003"
PS C:\> $ambariCreds = Get-Credential

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig  `
            | Add-AzHDInsightMetastore `
                -SqlAzureServerName "$ambariSqlServer.database.contoso.net" `
                -DatabaseName $ambariDb `
                -Credential $ambariCreds `
                -MetastoreType AmbariDatabase `
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

<span data-ttu-id="c5084-112">Questo comando aggiunge un database Ambari personalizzato al cluster denominato your-hadoop-002.</span><span class="sxs-lookup"><span data-stu-id="c5084-112">This command adds a custom Ambari database to the cluster named your-hadoop-002.</span></span>

## <span data-ttu-id="c5084-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5084-113">PARAMETERS</span></span>

### <span data-ttu-id="c5084-114">-Config</span><span class="sxs-lookup"><span data-stu-id="c5084-114">-Config</span></span>
<span data-ttu-id="c5084-115">Specifica l'oggetto di configurazione del cluster HDInsight modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5084-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="c5084-116">Questo oggetto viene creato dal cmdlet **New-AzHDInsightClusterConfig.**</span><span class="sxs-lookup"><span data-stu-id="c5084-116">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5084-117">-Credential</span><span class="sxs-lookup"><span data-stu-id="c5084-117">-Credential</span></span>
<span data-ttu-id="c5084-118">Specifica le credenziali da usare per il database del server AzureSQL.</span><span class="sxs-lookup"><span data-stu-id="c5084-118">Specifies the credentials to use for the AzureSQL Server database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5084-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c5084-119">-DatabaseName</span></span>
<span data-ttu-id="c5084-120">Specifica il database nell'istanza del server AzureSQL da usare per il metastore.</span><span class="sxs-lookup"><span data-stu-id="c5084-120">Specifies the database on the AzureSQL Server instance to use for this metastore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5084-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5084-121">-DefaultProfile</span></span>
<span data-ttu-id="c5084-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="c5084-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5084-123">-MetastoreType</span><span class="sxs-lookup"><span data-stu-id="c5084-123">-MetastoreType</span></span>
<span data-ttu-id="c5084-124">Specifica il tipo di metastore.</span><span class="sxs-lookup"><span data-stu-id="c5084-124">Specifies the type of metastore.</span></span>
<span data-ttu-id="c5084-125">I valori possibili sono HiveMetastore o OozieMetastore.</span><span class="sxs-lookup"><span data-stu-id="c5084-125">Possible values are HiveMetastore or OozieMetastore.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases:
Accepted values: HiveMetastore, OozieMetastore, AmbariDatabase

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5084-126">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="c5084-126">-SqlAzureServerName</span></span>
<span data-ttu-id="c5084-127">Specifica l'istanza del server AzureSQL da usare per il metastore.</span><span class="sxs-lookup"><span data-stu-id="c5084-127">Specifies the AzureSQL Server instance to use for this metastore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5084-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5084-128">CommonParameters</span></span>
<span data-ttu-id="c5084-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5084-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5084-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c5084-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5084-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="c5084-131">INPUTS</span></span>

### <span data-ttu-id="c5084-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="c5084-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="c5084-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5084-133">OUTPUTS</span></span>

### <span data-ttu-id="c5084-134">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="c5084-134">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="c5084-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="c5084-135">NOTES</span></span>

## <span data-ttu-id="c5084-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5084-136">RELATED LINKS</span></span>

[<span data-ttu-id="c5084-137">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="c5084-137">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


