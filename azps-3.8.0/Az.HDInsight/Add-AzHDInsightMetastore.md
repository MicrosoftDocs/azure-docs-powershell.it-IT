---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8BD3B8BD-DC87-4A94-9FCA-611D11D5E065
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightmetastore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightMetastore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightMetastore.md
ms.openlocfilehash: f8971070851da36fb1bf72aef33085e974ef1fb7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865491"
---
# <span data-ttu-id="6ac40-101">Add-AzHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="6ac40-101">Add-AzHDInsightMetastore</span></span>

## <span data-ttu-id="6ac40-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ac40-102">SYNOPSIS</span></span>
<span data-ttu-id="6ac40-103">Aggiunge un database SQL per fungere da Metastore hive o oozie a un oggetto di configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="6ac40-103">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

## <span data-ttu-id="6ac40-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ac40-104">SYNTAX</span></span>

```
Add-AzHDInsightMetastore [-Config] <AzureHDInsightConfig> [-MetastoreType] <AzureHDInsightMetastoreType>
 [-SqlAzureServerName] <String> [-DatabaseName] <String> [-Credential] <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ac40-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ac40-105">DESCRIPTION</span></span>
<span data-ttu-id="6ac40-106">Il cmdlet **Add-AzHDInsightMetastore** aggiunge un hive o oozie Metastore all'oggetto di configurazione HDInsight creato dal cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="6ac40-106">The **Add-AzHDInsightMetastore** cmdlet adds a Hive or Oozie metastore to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="6ac40-107">Un Metastore è un database SQL che può essere usato per archiviare metadati per hive, oozie o entrambi.</span><span class="sxs-lookup"><span data-stu-id="6ac40-107">A metastore is a SQL Database that can used to store metadata for Hive, Oozie, or both.</span></span>

## <span data-ttu-id="6ac40-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ac40-108">EXAMPLES</span></span>

### <span data-ttu-id="6ac40-109">Esempio 1: aggiungere un Metastore di database SQL all'oggetto di configurazione del cluster</span><span class="sxs-lookup"><span data-stu-id="6ac40-109">Example 1: Add a SQL database metastore to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
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
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="6ac40-110">Questo comando aggiunge un Metastore di database SQL al cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="6ac40-110">This command adds a SQL database metastore to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="6ac40-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ac40-111">PARAMETERS</span></span>

### <span data-ttu-id="6ac40-112">-Config</span><span class="sxs-lookup"><span data-stu-id="6ac40-112">-Config</span></span>
<span data-ttu-id="6ac40-113">Specifica l'oggetto di configurazione del cluster HDInsight modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ac40-113">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="6ac40-114">Questo oggetto viene creato dal cmdlet **New-AzHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="6ac40-114">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="6ac40-115">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="6ac40-115">-Credential</span></span>
<span data-ttu-id="6ac40-116">Specifica le credenziali da usare per il database del server AzureSQL.</span><span class="sxs-lookup"><span data-stu-id="6ac40-116">Specifies the credentials to use for the AzureSQL Server database.</span></span>

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

### <span data-ttu-id="6ac40-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6ac40-117">-DatabaseName</span></span>
<span data-ttu-id="6ac40-118">Specifica il database nell'istanza del server AzureSQL da usare per questo Metastore.</span><span class="sxs-lookup"><span data-stu-id="6ac40-118">Specifies the database on the AzureSQL Server instance to use for this metastore.</span></span>

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

### <span data-ttu-id="6ac40-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ac40-119">-DefaultProfile</span></span>
<span data-ttu-id="6ac40-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6ac40-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ac40-121">-MetastoreType</span><span class="sxs-lookup"><span data-stu-id="6ac40-121">-MetastoreType</span></span>
<span data-ttu-id="6ac40-122">Specifica il tipo di Metastore.</span><span class="sxs-lookup"><span data-stu-id="6ac40-122">Specifies the type of metastore.</span></span>
<span data-ttu-id="6ac40-123">I valori possibili sono HiveMetastore o OozieMetastore.</span><span class="sxs-lookup"><span data-stu-id="6ac40-123">Possible values are HiveMetastore or OozieMetastore.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases:
Accepted values: HiveMetastore, OozieMetastore

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ac40-124">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="6ac40-124">-SqlAzureServerName</span></span>
<span data-ttu-id="6ac40-125">Specifica l'istanza del server AzureSQL da usare per questo Metastore.</span><span class="sxs-lookup"><span data-stu-id="6ac40-125">Specifies the AzureSQL Server instance to use for this metastore.</span></span>

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

### <span data-ttu-id="6ac40-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ac40-126">CommonParameters</span></span>
<span data-ttu-id="6ac40-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ac40-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ac40-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ac40-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ac40-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ac40-129">INPUTS</span></span>

### <span data-ttu-id="6ac40-130">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="6ac40-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="6ac40-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ac40-131">OUTPUTS</span></span>

### <span data-ttu-id="6ac40-132">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="6ac40-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="6ac40-133">Note</span><span class="sxs-lookup"><span data-stu-id="6ac40-133">NOTES</span></span>

## <span data-ttu-id="6ac40-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ac40-134">RELATED LINKS</span></span>

[<span data-ttu-id="6ac40-135">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="6ac40-135">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


