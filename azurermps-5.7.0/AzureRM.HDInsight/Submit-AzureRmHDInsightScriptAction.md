---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/submit-azurermhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
ms.openlocfilehash: 866bd8c8189ca727b3893f09370bcca1136e827b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521446"
---
# <span data-ttu-id="567a6-101">Submit-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="567a6-101">Submit-AzureRmHDInsightScriptAction</span></span>

## <span data-ttu-id="567a6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="567a6-102">SYNOPSIS</span></span>
<span data-ttu-id="567a6-103">Invia una nuova azione di script a un cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="567a6-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="567a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="567a6-104">SYNTAX</span></span>

```
Submit-AzureRmHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="567a6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="567a6-105">DESCRIPTION</span></span>
<span data-ttu-id="567a6-106">Il cmdlet **Submit-AzureRmHDInsightScriptAction** invia una nuova azione di script a un cluster HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="567a6-106">The **Submit-AzureRmHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="567a6-107">USA *PersistOnSuccess* per eseguire l'azione di script ogni volta che il cluster viene ridimensionato, purché l'azione di script abbia esito positivo.</span><span class="sxs-lookup"><span data-stu-id="567a6-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="567a6-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="567a6-108">EXAMPLES</span></span>

### <span data-ttu-id="567a6-109">Esempio 1: inviare una nuova azione di script a un cluster in esecuzione di HDInsight</span><span class="sxs-lookup"><span data-stu-id="567a6-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzureRmHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="567a6-110">Questo comando Invia un'azione di script a un cluster HDInsight in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="567a6-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="567a6-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="567a6-111">PARAMETERS</span></span>

### <span data-ttu-id="567a6-112">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="567a6-112">-ApplicationName</span></span>
<span data-ttu-id="567a6-113">Specifica il nome dell'applicazione per l'azione di script.</span><span class="sxs-lookup"><span data-stu-id="567a6-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="567a6-114">Quando si specifica *ApplicationName* , *PersistOnSuccess* deve essere impostato su false, i nodi devono contenere solo edgenode e il conteggio delle azioni script deve essere uguale a 1.</span><span class="sxs-lookup"><span data-stu-id="567a6-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="567a6-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="567a6-115">-ClusterName</span></span>
<span data-ttu-id="567a6-116">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="567a6-116">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="567a6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="567a6-117">-DefaultProfile</span></span>
<span data-ttu-id="567a6-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="567a6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="567a6-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="567a6-119">-Name</span></span>
<span data-ttu-id="567a6-120">Specifica il nome dell'azione di script.</span><span class="sxs-lookup"><span data-stu-id="567a6-120">Specifies the name of the script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="567a6-121">-NodeTypes</span><span class="sxs-lookup"><span data-stu-id="567a6-121">-NodeTypes</span></span>
<span data-ttu-id="567a6-122">Specifica i tipi di nodo su cui eseguire l'azione di script.</span><span class="sxs-lookup"><span data-stu-id="567a6-122">Specifies the node types on which to run the script action.</span></span>

```yaml
Type: RuntimeScriptActionClusterNodeType[]
Parameter Sets: (All)
Aliases: 
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="567a6-123">-Parameters</span><span class="sxs-lookup"><span data-stu-id="567a6-123">-Parameters</span></span>
<span data-ttu-id="567a6-124">Specifica i parametri per l'azione di script.</span><span class="sxs-lookup"><span data-stu-id="567a6-124">Specifies the parameters for the script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="567a6-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="567a6-125">-PersistOnSuccess</span></span>
<span data-ttu-id="567a6-126">Indica che l'azione di script deve essere eseguita ogni volta che il cluster viene ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="567a6-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="567a6-127">Questo parametro switch viene ignorato se l'azione di script non riesce inizialmente.</span><span class="sxs-lookup"><span data-stu-id="567a6-127">This switch parameter is ignored if the script action initially fails.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="567a6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="567a6-128">-ResourceGroupName</span></span>
<span data-ttu-id="567a6-129">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="567a6-129">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="567a6-130">-URI</span><span class="sxs-lookup"><span data-stu-id="567a6-130">-Uri</span></span>
<span data-ttu-id="567a6-131">Specifica l'URI pubblico per l'azione di script (uno script di PowerShell o bash).</span><span class="sxs-lookup"><span data-stu-id="567a6-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="567a6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="567a6-132">CommonParameters</span></span>
<span data-ttu-id="567a6-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="567a6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="567a6-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="567a6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="567a6-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="567a6-135">INPUTS</span></span>

### <span data-ttu-id="567a6-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="567a6-136">None</span></span>
<span data-ttu-id="567a6-137">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="567a6-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="567a6-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="567a6-138">OUTPUTS</span></span>

### <span data-ttu-id="567a6-139">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptActionOperationResource</span><span class="sxs-lookup"><span data-stu-id="567a6-139">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="567a6-140">Note</span><span class="sxs-lookup"><span data-stu-id="567a6-140">NOTES</span></span>

## <span data-ttu-id="567a6-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="567a6-141">RELATED LINKS</span></span>

[<span data-ttu-id="567a6-142">Add-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="567a6-142">Add-AzureRmHDInsightScriptAction</span></span>](./Add-AzureRmHDInsightScriptAction.md)


