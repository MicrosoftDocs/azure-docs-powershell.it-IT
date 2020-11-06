---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8F0634BD-D817-4365-B6D1-924DC36AE4C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightScriptAction.md
ms.openlocfilehash: 593eb41b66b581ac779b0eb1d5220551f27d8ff7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514319"
---
# <span data-ttu-id="095be-101">Add-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="095be-101">Add-AzureRmHDInsightScriptAction</span></span>

## <span data-ttu-id="095be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="095be-102">SYNOPSIS</span></span>
<span data-ttu-id="095be-103">Aggiunge un'azione di script a un oggetto di configurazione del cluster.</span><span class="sxs-lookup"><span data-stu-id="095be-103">Adds a script action to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="095be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="095be-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightScriptAction [-Config] <AzureHDInsightConfig> [-NodeType] <ClusterNodeType> [-Uri] <Uri>
 [-Name] <String> [[-Parameters] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="095be-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="095be-105">DESCRIPTION</span></span>
<span data-ttu-id="095be-106">Il cmdlet **Add-AzureRmHDInsightScriptAction** aggiunge le azioni di script all'oggetto di configurazione HDInsight creato dal cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="095be-106">The **Add-AzureRmHDInsightScriptAction** cmdlet adds script actions to the HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

<span data-ttu-id="095be-107">Le azioni di script includono funzionalità che vengono usate per installare software aggiuntivo o per modificare la configurazione delle applicazioni eseguite in un cluster Hadoop tramite Windows PowerShell o script bash (rispettivamente per i cluster Windows o Linux).</span><span class="sxs-lookup"><span data-stu-id="095be-107">Script actions provide functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell or Bash scripts (for Windows or Linux clusters, respectively).</span></span>

<span data-ttu-id="095be-108">Un'azione di script viene eseguita sui nodi del cluster quando vengono distribuiti i cluster di HDInsight e vengono eseguiti dopo i nodi della configurazione completa di HDInsight del cluster.</span><span class="sxs-lookup"><span data-stu-id="095be-108">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="095be-109">L'azione script viene eseguita in privilegi di amministratore di sistema e fornisce i diritti di accesso completo ai nodi del cluster.</span><span class="sxs-lookup"><span data-stu-id="095be-109">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="095be-110">Puoi specificare ogni cluster con un elenco di azioni di script da eseguire in una sequenza specificata.</span><span class="sxs-lookup"><span data-stu-id="095be-110">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="095be-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="095be-111">EXAMPLES</span></span>

### <span data-ttu-id="095be-112">Esempio 1: aggiungere un'azione di script all'oggetto di configurazione del cluster</span><span class="sxs-lookup"><span data-stu-id="095be-112">Example 1: Add a script action to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Script action info
PS C:\> $scriptActionName = "<script action name>"
PS C:\> $scriptActionURI = "<script action URI>"
PS C:\> $scriptActionParameters = "<script action parameters>" 

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig  `
            | Add-AzureRmHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Worker `
            | Add-AzureRmHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Head `
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

<span data-ttu-id="095be-113">Questo comando aggiunge un'azione di script per i nodi head e worker del cluster ur-Hadoop-001, da eseguire alla fine della creazione del cluster.</span><span class="sxs-lookup"><span data-stu-id="095be-113">This command adds a script action for the Head and Worker nodes of the your-hadoop-001 cluster, to be run at the end of cluster creation.</span></span>

## <span data-ttu-id="095be-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="095be-114">PARAMETERS</span></span>

### <span data-ttu-id="095be-115">-Config</span><span class="sxs-lookup"><span data-stu-id="095be-115">-Config</span></span>
<span data-ttu-id="095be-116">Specifica l'oggetto di configurazione del cluster HDInsight modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="095be-116">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="095be-117">Questo oggetto viene creato dal cmdlet **New-AzureRmHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="095be-117">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="095be-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="095be-118">-DefaultProfile</span></span>
<span data-ttu-id="095be-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="095be-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="095be-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="095be-120">-Name</span></span>
<span data-ttu-id="095be-121">Specifica il nome dell'azione di script.</span><span class="sxs-lookup"><span data-stu-id="095be-121">Specifies the name of the script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="095be-122">-NodeType</span><span class="sxs-lookup"><span data-stu-id="095be-122">-NodeType</span></span>
<span data-ttu-id="095be-123">Specifica il tipo di nodo su cui eseguire l'azione di script.</span><span class="sxs-lookup"><span data-stu-id="095be-123">Specifies the node type on which to run the script action.</span></span>
<span data-ttu-id="095be-124">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="095be-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="095be-125">HeadNode</span><span class="sxs-lookup"><span data-stu-id="095be-125">HeadNode</span></span>
- <span data-ttu-id="095be-126">WorkerNode</span><span class="sxs-lookup"><span data-stu-id="095be-126">WorkerNode</span></span>
- <span data-ttu-id="095be-127">ZookeeperNode</span><span class="sxs-lookup"><span data-stu-id="095be-127">ZookeeperNode</span></span>

```yaml
Type: ClusterNodeType
Parameter Sets: (All)
Aliases: 
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="095be-128">-Parameters</span><span class="sxs-lookup"><span data-stu-id="095be-128">-Parameters</span></span>
<span data-ttu-id="095be-129">Specifica i parametri per l'azione di script.</span><span class="sxs-lookup"><span data-stu-id="095be-129">Specifies the parameters for the script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="095be-130">-URI</span><span class="sxs-lookup"><span data-stu-id="095be-130">-Uri</span></span>
<span data-ttu-id="095be-131">Specifica l'URI pubblico per l'azione di script (uno script di PowerShell o bash).</span><span class="sxs-lookup"><span data-stu-id="095be-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="095be-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="095be-132">CommonParameters</span></span>
<span data-ttu-id="095be-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="095be-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="095be-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="095be-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="095be-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="095be-135">INPUTS</span></span>

### <span data-ttu-id="095be-136">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="095be-136">AzureHDInsightConfig</span></span>
<span data-ttu-id="095be-137">Il parametro ' config ' accetta il valore di tipo ' AzureHDInsightConfig ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="095be-137">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="095be-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="095be-138">OUTPUTS</span></span>

### <span data-ttu-id="095be-139">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="095be-139">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="095be-140">Note</span><span class="sxs-lookup"><span data-stu-id="095be-140">NOTES</span></span>

## <span data-ttu-id="095be-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="095be-141">RELATED LINKS</span></span>

[<span data-ttu-id="095be-142">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="095be-142">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


