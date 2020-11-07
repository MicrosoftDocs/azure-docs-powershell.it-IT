---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightdefaultstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightDefaultStorage.md
ms.openlocfilehash: 1544b557382deb7ff3c005a184612f48c293521e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688426"
---
# <span data-ttu-id="097b6-101">Set-AzureRmHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="097b6-101">Set-AzureRmHDInsightDefaultStorage</span></span>

## <span data-ttu-id="097b6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="097b6-102">SYNOPSIS</span></span>
<span data-ttu-id="097b6-103">Imposta l'impostazione predefinita dell'account di archiviazione in un oggetto di configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="097b6-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="097b6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="097b6-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="097b6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="097b6-105">DESCRIPTION</span></span>
<span data-ttu-id="097b6-106">Il cmdlet **set-AzureRmHDInsightDefaultStorage** imposta l'impostazione predefinita dell'account di archiviazione nell'oggetto di configurazione del cluster di Azure HDInsight creato dal cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="097b6-106">The **Set-AzureRmHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="097b6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="097b6-107">EXAMPLES</span></span>

### <span data-ttu-id="097b6-108">Esempio 1: impostare l'account di archiviazione predefinito per l'oggetto di configurazione del cluster</span><span class="sxs-lookup"><span data-stu-id="097b6-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\>$storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRMResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Set-AzureRmHDInsightDefaultStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
                -StorageContainer $storageContainer `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location
```

<span data-ttu-id="097b6-109">Questo comando imposta l'account di archiviazione predefinito per un oggetto di configurazione del cluster.</span><span class="sxs-lookup"><span data-stu-id="097b6-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="097b6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="097b6-110">PARAMETERS</span></span>

### <span data-ttu-id="097b6-111">-Config</span><span class="sxs-lookup"><span data-stu-id="097b6-111">-Config</span></span>
<span data-ttu-id="097b6-112">Specifica l'oggetto di configurazione del cluster HDInsight modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="097b6-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="097b6-113">Questo oggetto viene creato dal cmdlet **New-AzureRmHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="097b6-113">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="097b6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="097b6-114">-DefaultProfile</span></span>
<span data-ttu-id="097b6-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="097b6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="097b6-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="097b6-116">-StorageAccountKey</span></span>
<span data-ttu-id="097b6-117">Specifica la chiave dell'account per l'account di archiviazione di Azure predefinito che verrà usato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="097b6-117">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="097b6-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="097b6-118">-StorageAccountName</span></span>
<span data-ttu-id="097b6-119">Specifica il nome dell'account di archiviazione predefinito che verrà usato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="097b6-119">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="097b6-120">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="097b6-120">-StorageAccountType</span></span>
<span data-ttu-id="097b6-121">Ottiene o imposta il tipo di account di archiviazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="097b6-121">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="097b6-122">Impostazione predefinita per AzureStorage</span><span class="sxs-lookup"><span data-stu-id="097b6-122">Defaults to AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="097b6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="097b6-123">CommonParameters</span></span>
<span data-ttu-id="097b6-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="097b6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="097b6-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="097b6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="097b6-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="097b6-126">INPUTS</span></span>

### <span data-ttu-id="097b6-127">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="097b6-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
<span data-ttu-id="097b6-128">Parametri: config (ByValue)</span><span class="sxs-lookup"><span data-stu-id="097b6-128">Parameters: Config (ByValue)</span></span>

## <span data-ttu-id="097b6-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="097b6-129">OUTPUTS</span></span>

### <span data-ttu-id="097b6-130">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="097b6-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="097b6-131">Note</span><span class="sxs-lookup"><span data-stu-id="097b6-131">NOTES</span></span>

## <span data-ttu-id="097b6-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="097b6-132">RELATED LINKS</span></span>
