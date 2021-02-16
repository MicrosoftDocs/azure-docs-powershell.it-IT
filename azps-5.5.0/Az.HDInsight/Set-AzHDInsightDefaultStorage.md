---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightdefaultstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
ms.openlocfilehash: 06a783d0faf32dc2a3a35b448b1316ef50ba3326
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200190"
---
# <span data-ttu-id="4dc7a-101">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="4dc7a-101">Set-AzHDInsightDefaultStorage</span></span>

## <span data-ttu-id="4dc7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dc7a-102">SYNOPSIS</span></span>
<span data-ttu-id="4dc7a-103">Imposta l'impostazione predefinita dell'account di archiviazione in un oggetto configurazione cluster.</span><span class="sxs-lookup"><span data-stu-id="4dc7a-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

## <span data-ttu-id="4dc7a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4dc7a-104">SYNTAX</span></span>

```
Set-AzHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountResourceId] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4dc7a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4dc7a-105">DESCRIPTION</span></span>
<span data-ttu-id="4dc7a-106">Il cmdlet **Set-AzHDInsightDefaultStorage** imposta l'impostazione predefinita dell'account di archiviazione nell'oggetto configurazione del cluster Azure HDInsight creato dal cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="4dc7a-106">The **Set-AzHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="4dc7a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4dc7a-107">EXAMPLES</span></span>

### <span data-ttu-id="4dc7a-108">Esempio 1: Impostare l'account di archiviazione predefinito per l'oggetto di configurazione del cluster</span><span class="sxs-lookup"><span data-stu-id="4dc7a-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageaccountname"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\>$storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Set-AzHDInsightDefaultStorage `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $key2 `
                -StorageContainer $storageContainer `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location
```

<span data-ttu-id="4dc7a-109">Questo comando imposta l'account di archiviazione predefinito per un oggetto di configurazione del cluster.</span><span class="sxs-lookup"><span data-stu-id="4dc7a-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="4dc7a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4dc7a-110">PARAMETERS</span></span>

### <span data-ttu-id="4dc7a-111">-Config</span><span class="sxs-lookup"><span data-stu-id="4dc7a-111">-Config</span></span>
<span data-ttu-id="4dc7a-112">Specifica l'oggetto di configurazione del cluster HDInsight modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dc7a-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="4dc7a-113">Questo oggetto viene creato dal cmdlet **New-AzHDInsightClusterConfig.**</span><span class="sxs-lookup"><span data-stu-id="4dc7a-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="4dc7a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dc7a-114">-DefaultProfile</span></span>
<span data-ttu-id="4dc7a-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="4dc7a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4dc7a-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4dc7a-116">-StorageAccountKey</span></span>
<span data-ttu-id="4dc7a-117">Specifica la chiave dell'account di archiviazione di Azure predefinito che verrà utilizzato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4dc7a-117">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="4dc7a-118">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="4dc7a-118">-StorageAccountResourceId</span></span>
<span data-ttu-id="4dc7a-119">Nome dell'account di archiviazione da aggiungere al nuovo cluster.</span><span class="sxs-lookup"><span data-stu-id="4dc7a-119">The storage account name for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="4dc7a-120">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="4dc7a-120">-StorageAccountType</span></span>
<span data-ttu-id="4dc7a-121">Ottiene o imposta il tipo di account di archiviazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="4dc7a-121">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="4dc7a-122">Impostazioni predefinite di AzureStorage</span><span class="sxs-lookup"><span data-stu-id="4dc7a-122">Defaults to AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dc7a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dc7a-123">CommonParameters</span></span>
<span data-ttu-id="4dc7a-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dc7a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dc7a-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4dc7a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dc7a-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="4dc7a-126">INPUTS</span></span>

### <span data-ttu-id="4dc7a-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="4dc7a-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="4dc7a-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4dc7a-128">OUTPUTS</span></span>

### <span data-ttu-id="4dc7a-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="4dc7a-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="4dc7a-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="4dc7a-130">NOTES</span></span>

## <span data-ttu-id="4dc7a-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4dc7a-131">RELATED LINKS</span></span>
