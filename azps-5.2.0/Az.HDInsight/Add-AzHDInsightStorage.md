---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C2AF43D-18BF-4036-A355-FC27E406B18A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
ms.openlocfilehash: b3697b0f5e657a95d131c928f4393f8a4f1e854c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339988"
---
# <span data-ttu-id="07fc3-101">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="07fc3-101">Add-AzHDInsightStorage</span></span>

## <span data-ttu-id="07fc3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="07fc3-103">Aggiunge una chiave di archiviazione di Azure a un oggetto di configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="07fc3-103">Adds an Azure Storage key to a cluster configuration object.</span></span>

## <span data-ttu-id="07fc3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07fc3-104">SYNTAX</span></span>

```
Add-AzHDInsightStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07fc3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07fc3-105">DESCRIPTION</span></span>
<span data-ttu-id="07fc3-106">Il cmdlet **Add-AzHDInsightStorage** aggiunge una voce dell'account di archiviazione di Azure all'oggetto di configurazione di Azure HDInsight creato dal cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="07fc3-106">The **Add-AzHDInsightStorage** cmdlet adds an Azure Storage account entry to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="07fc3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07fc3-107">EXAMPLES</span></span>

### <span data-ttu-id="07fc3-108">Esempio 1: aggiungere una chiave di archiviazione di Azure all'oggetto di configurazione del cluster</span><span class="sxs-lookup"><span data-stu-id="07fc3-108">Example 1: Add an Azure storage key to the cluster configuration object</span></span>
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

# Second storage account info
PS C:\> $secondStorageAccountResourceGroupName = "Group"
PS C:\> $secondStorageAccountName = "yourstorageacct002"
PS C:\> $secondStorageAccountKey = Get-AzStorageAccountKey `
PS C:\> -ResourceGroupName $secondStorageAccountResourceGroupName `
            -Name $secondStorageAccountName | %{ $_.Key1 }

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

<span data-ttu-id="07fc3-109">Questo comando aggiunge una voce dell'account di archiviazione BLOB alla configurazione di HDInsight denominata your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="07fc3-109">This command adds an blob storage account entry to the HDInsight configuration named your-hadoop-001.</span></span>

## <span data-ttu-id="07fc3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07fc3-110">PARAMETERS</span></span>

### <span data-ttu-id="07fc3-111">-Config</span><span class="sxs-lookup"><span data-stu-id="07fc3-111">-Config</span></span>
<span data-ttu-id="07fc3-112">Specifica l'oggetto di configurazione del cluster HDInsight modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07fc3-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="07fc3-113">Questo oggetto viene creato dal cmdlet **New-AzHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="07fc3-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="07fc3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07fc3-114">-DefaultProfile</span></span>
<span data-ttu-id="07fc3-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="07fc3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07fc3-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="07fc3-116">-StorageAccountKey</span></span>
<span data-ttu-id="07fc3-117">Specifica la chiave dell'account di archiviazione per l'account di archiviazione da aggiungere al nuovo cluster.</span><span class="sxs-lookup"><span data-stu-id="07fc3-117">Specifies the storage account key for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="07fc3-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="07fc3-118">-StorageAccountName</span></span>
<span data-ttu-id="07fc3-119">Specifica il nome dell'account di archiviazione per l'account di archiviazione da aggiungere al cluster.</span><span class="sxs-lookup"><span data-stu-id="07fc3-119">Specifies the storage account name for the storage account to be added to the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07fc3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07fc3-120">CommonParameters</span></span>
<span data-ttu-id="07fc3-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07fc3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07fc3-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07fc3-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07fc3-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07fc3-123">INPUTS</span></span>

### <span data-ttu-id="07fc3-124">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="07fc3-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="07fc3-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07fc3-125">OUTPUTS</span></span>

### <span data-ttu-id="07fc3-126">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="07fc3-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="07fc3-127">Note</span><span class="sxs-lookup"><span data-stu-id="07fc3-127">NOTES</span></span>

## <span data-ttu-id="07fc3-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07fc3-128">RELATED LINKS</span></span>

[<span data-ttu-id="07fc3-129">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="07fc3-129">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


