---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2C2AF43D-18BF-4036-A355-FC27E406B18A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightStorage.md
ms.openlocfilehash: 2452ef9784b18550569125c47fd5859c260e754e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685989"
---
# <span data-ttu-id="bbfab-101">Add-AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="bbfab-101">Add-AzureRmHDInsightStorage</span></span>

## <span data-ttu-id="bbfab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bbfab-102">SYNOPSIS</span></span>
<span data-ttu-id="bbfab-103">Aggiunge una chiave di archiviazione di Azure a un oggetto di configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="bbfab-103">Adds an Azure Storage key to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbfab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bbfab-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbfab-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bbfab-105">DESCRIPTION</span></span>
<span data-ttu-id="bbfab-106">Il cmdlet **Add-AzureRmHDInsightStorage** aggiunge una voce dell'account di archiviazione di Azure all'oggetto di configurazione di Azure HDInsight creato dal cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="bbfab-106">The **Add-AzureRmHDInsightStorage** cmdlet adds an Azure Storage account entry to the Azure HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="bbfab-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bbfab-107">EXAMPLES</span></span>

### <span data-ttu-id="bbfab-108">Esempio 1: aggiungere una chiave di archiviazione di Azure all'oggetto di configurazione del cluster</span><span class="sxs-lookup"><span data-stu-id="bbfab-108">Example 1: Add an Azure storage key to the cluster configuration object</span></span>
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

# Second storage account info
PS C:\> $secondStorageAccountResourceGroupName = "Group"
PS C:\> $secondStorageAccountName = "yourstorageacct002"
PS C:\> $secondStorageAccountKey = Get-AzureRmStorageAccountKey `
PS C:\> -ResourceGroupName $secondStorageAccountResourceGroupName `
            -Name $secondStorageAccountName | %{ $_.Key1 }

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

<span data-ttu-id="bbfab-109">Questo comando aggiunge una voce dell'account di archiviazione BLOB alla configurazione di HDInsight denominata your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="bbfab-109">This command adds an blob storage account entry to the HDInsight configuration named your-hadoop-001.</span></span>

## <span data-ttu-id="bbfab-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bbfab-110">PARAMETERS</span></span>

### <span data-ttu-id="bbfab-111">-Config</span><span class="sxs-lookup"><span data-stu-id="bbfab-111">-Config</span></span>
<span data-ttu-id="bbfab-112">Specifica l'oggetto di configurazione del cluster HDInsight modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbfab-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="bbfab-113">Questo oggetto viene creato dal cmdlet **New-AzureRmHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="bbfab-113">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbfab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbfab-114">-DefaultProfile</span></span>
<span data-ttu-id="bbfab-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="bbfab-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bbfab-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="bbfab-116">-StorageAccountKey</span></span>
<span data-ttu-id="bbfab-117">Specifica la chiave dell'account di archiviazione per l'account di archiviazione da aggiungere al nuovo cluster.</span><span class="sxs-lookup"><span data-stu-id="bbfab-117">Specifies the storage account key for the storage account to be added to the new cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbfab-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bbfab-118">-StorageAccountName</span></span>
<span data-ttu-id="bbfab-119">Specifica il nome dell'account di archiviazione per l'account di archiviazione da aggiungere al cluster.</span><span class="sxs-lookup"><span data-stu-id="bbfab-119">Specifies the storage account name for the storage account to be added to the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbfab-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbfab-120">CommonParameters</span></span>
<span data-ttu-id="bbfab-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbfab-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbfab-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbfab-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbfab-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bbfab-123">INPUTS</span></span>

### <span data-ttu-id="bbfab-124">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="bbfab-124">AzureHDInsightConfig</span></span>
<span data-ttu-id="bbfab-125">Il parametro ' config ' accetta il valore di tipo ' AzureHDInsightConfig ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="bbfab-125">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="bbfab-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bbfab-126">OUTPUTS</span></span>

### <span data-ttu-id="bbfab-127">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="bbfab-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="bbfab-128">Note</span><span class="sxs-lookup"><span data-stu-id="bbfab-128">NOTES</span></span>

## <span data-ttu-id="bbfab-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bbfab-129">RELATED LINKS</span></span>

[<span data-ttu-id="bbfab-130">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="bbfab-130">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


