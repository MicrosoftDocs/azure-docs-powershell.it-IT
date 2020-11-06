---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8BD3B8BD-DC87-4A94-9FCA-611D11D5E065
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightMetastore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightMetastore.md
ms.openlocfilehash: f21108e949ff1d6787488f9f4b6c062d5954a7e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521247"
---
# <span data-ttu-id="b5a3c-101">Add-AzureRmHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="b5a3c-101">Add-AzureRmHDInsightMetastore</span></span>

## <span data-ttu-id="b5a3c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b5a3c-102">SYNOPSIS</span></span>
<span data-ttu-id="b5a3c-103">Aggiunge un database SQL per fungere da Metastore hive o oozie a un oggetto di configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="b5a3c-103">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5a3c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5a3c-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightMetastore [-Config] <AzureHDInsightConfig> [-MetastoreType] <AzureHDInsightMetastoreType>
 [-SqlAzureServerName] <String> [-DatabaseName] <String> [-Credential] <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5a3c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5a3c-105">DESCRIPTION</span></span>
<span data-ttu-id="b5a3c-106">Il cmdlet **Add-AzureRmHDInsightMetastore** aggiunge un hive o oozie Metastore all'oggetto di configurazione HDInsight creato dal cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="b5a3c-106">The **Add-AzureRmHDInsightMetastore** cmdlet adds a Hive or Oozie metastore to the HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="b5a3c-107">Un Metastore è un database SQL che può essere usato per archiviare metadati per hive, oozie o entrambi.</span><span class="sxs-lookup"><span data-stu-id="b5a3c-107">A metastore is a SQL Database that can used to store metadata for Hive, Oozie, or both.</span></span>

## <span data-ttu-id="b5a3c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5a3c-108">EXAMPLES</span></span>

### <span data-ttu-id="b5a3c-109">Esempio 1: aggiungere un Metastore di database SQL all'oggetto di configurazione del cluster</span><span class="sxs-lookup"><span data-stu-id="b5a3c-109">Example 1: Add a SQL database metastore to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Hive metastore info
PS C:\> $hiveSqlServer = "your-sqlserver-001"
PS C:\> $hiveDb = "your-sqldb-001"
PS C:\> $hiveCreds = Get-Credential

# Oozie metastore info
PS C:\> $oozieSqlServer = "your-sqlserver-001"
PS C:\> $oozieDb = "your-sqldb-002"
PS C:\> $oozieCreds = Get-Credential

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig  `
            | Add-AzureRmHDInsightMetastore `
                -SqlAzureServerName "$oozieSqlServer.database.contoso.net" `
                -DatabaseName $oozieDb `
                -Credential $oozieCreds `
                -MetastoreType OozieMetastore `
            | Add-AzureRmHDInsightMetastore `
                -SqlAzureServerName "$hiveSqlServer.database.contoso.net" `
                -DatabaseName $hiveDb `
                -Credential $hiveCreds `
                -MetastoreType HiveMetastore `
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

<span data-ttu-id="b5a3c-110">Questo comando aggiunge un Metastore di database SQL al cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="b5a3c-110">This command adds a SQL database metastore to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="b5a3c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b5a3c-111">PARAMETERS</span></span>

### <span data-ttu-id="b5a3c-112">-Config</span><span class="sxs-lookup"><span data-stu-id="b5a3c-112">-Config</span></span>
<span data-ttu-id="b5a3c-113">Specifica l'oggetto di configurazione del cluster HDInsight modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5a3c-113">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="b5a3c-114">Questo oggetto viene creato dal cmdlet **New-AzureRmHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="b5a3c-114">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="b5a3c-115">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="b5a3c-115">-Credential</span></span>
<span data-ttu-id="b5a3c-116">Specifica le credenziali da usare per il database del server AzureSQL.</span><span class="sxs-lookup"><span data-stu-id="b5a3c-116">Specifies the credentials to use for the AzureSQL Server database.</span></span>

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

### <span data-ttu-id="b5a3c-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b5a3c-117">-DatabaseName</span></span>
<span data-ttu-id="b5a3c-118">Specifica il database nell'istanza del server AzureSQL da usare per questo Metastore.</span><span class="sxs-lookup"><span data-stu-id="b5a3c-118">Specifies the database on the AzureSQL Server instance to use for this metastore.</span></span>

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

### <span data-ttu-id="b5a3c-119">-MetastoreType</span><span class="sxs-lookup"><span data-stu-id="b5a3c-119">-MetastoreType</span></span>
<span data-ttu-id="b5a3c-120">Specifica il tipo di Metastore.</span><span class="sxs-lookup"><span data-stu-id="b5a3c-120">Specifies the type of metastore.</span></span>
<span data-ttu-id="b5a3c-121">I valori possibili sono HiveMetastore o OozieMetastore.</span><span class="sxs-lookup"><span data-stu-id="b5a3c-121">Possible values are HiveMetastore or OozieMetastore.</span></span>

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

### <span data-ttu-id="b5a3c-122">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="b5a3c-122">-SqlAzureServerName</span></span>
<span data-ttu-id="b5a3c-123">Specifica l'istanza del server AzureSQL da usare per questo Metastore.</span><span class="sxs-lookup"><span data-stu-id="b5a3c-123">Specifies the AzureSQL Server instance to use for this metastore.</span></span>

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

### <span data-ttu-id="b5a3c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5a3c-124">-DefaultProfile</span></span>
<span data-ttu-id="b5a3c-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b5a3c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5a3c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5a3c-126">CommonParameters</span></span>
<span data-ttu-id="b5a3c-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5a3c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5a3c-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5a3c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5a3c-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b5a3c-129">INPUTS</span></span>

### <span data-ttu-id="b5a3c-130">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="b5a3c-130">AzureHDInsightConfig</span></span>
<span data-ttu-id="b5a3c-131">Il parametro ' config ' accetta il valore di tipo ' AzureHDInsightConfig ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="b5a3c-131">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="b5a3c-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5a3c-132">OUTPUTS</span></span>

### <span data-ttu-id="b5a3c-133">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="b5a3c-133">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="b5a3c-134">Note</span><span class="sxs-lookup"><span data-stu-id="b5a3c-134">NOTES</span></span>

## <span data-ttu-id="b5a3c-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5a3c-135">RELATED LINKS</span></span>

[<span data-ttu-id="b5a3c-136">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="b5a3c-136">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


