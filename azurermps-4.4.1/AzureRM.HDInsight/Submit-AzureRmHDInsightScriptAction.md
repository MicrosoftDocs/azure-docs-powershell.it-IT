---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
ms.openlocfilehash: 4739d5d6780caa85820c37974d9a8b69d2816e38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688298"
---
# <span data-ttu-id="0268f-101">Submit-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="0268f-101">Submit-AzureRmHDInsightScriptAction</span></span>

## <span data-ttu-id="0268f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0268f-102">SYNOPSIS</span></span>
<span data-ttu-id="0268f-103">Invia una nuova azione di script a un cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0268f-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0268f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0268f-104">SYNTAX</span></span>

```
Submit-AzureRmHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0268f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0268f-105">DESCRIPTION</span></span>
<span data-ttu-id="0268f-106">Il cmdlet **Submit-AzureRmHDInsightScriptAction** invia una nuova azione di script a un cluster HDInsight di Azure.</span><span class="sxs-lookup"><span data-stu-id="0268f-106">The **Submit-AzureRmHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="0268f-107">USA *PersistOnSuccess* per eseguire l'azione di script ogni volta che il cluster viene ridimensionato, purché l'azione di script abbia esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0268f-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="0268f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0268f-108">EXAMPLES</span></span>

### <span data-ttu-id="0268f-109">Esempio 1: inviare una nuova azione di script a un cluster in esecuzione di HDInsight</span><span class="sxs-lookup"><span data-stu-id="0268f-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzureRmHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="0268f-110">Questo comando Invia un'azione di script a un cluster HDInsight in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="0268f-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="0268f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0268f-111">PARAMETERS</span></span>

### <span data-ttu-id="0268f-112">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="0268f-112">-ApplicationName</span></span>
<span data-ttu-id="0268f-113">Specifica il nome dell'applicazione per l'azione di script.</span><span class="sxs-lookup"><span data-stu-id="0268f-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="0268f-114">Quando si specifica *ApplicationName* , *PersistOnSuccess* deve essere impostato su false, i nodi devono contenere solo edgenode e il conteggio delle azioni script deve essere uguale a 1.</span><span class="sxs-lookup"><span data-stu-id="0268f-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0268f-115">-Clustername</span><span class="sxs-lookup"><span data-stu-id="0268f-115">-ClusterName</span></span>
<span data-ttu-id="0268f-116">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="0268f-116">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0268f-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="0268f-117">-Name</span></span>
<span data-ttu-id="0268f-118">Specifica il nome dell'azione di script.</span><span class="sxs-lookup"><span data-stu-id="0268f-118">Specifies the name of the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0268f-119">-NodeTypes</span><span class="sxs-lookup"><span data-stu-id="0268f-119">-NodeTypes</span></span>
<span data-ttu-id="0268f-120">Specifica i tipi di nodo su cui eseguire l'azione di script.</span><span class="sxs-lookup"><span data-stu-id="0268f-120">Specifies the node types on which to run the script action.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]
Parameter Sets: (All)
Aliases: 
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0268f-121">-Parameters</span><span class="sxs-lookup"><span data-stu-id="0268f-121">-Parameters</span></span>
<span data-ttu-id="0268f-122">Specifica i parametri per l'azione di script.</span><span class="sxs-lookup"><span data-stu-id="0268f-122">Specifies the parameters for the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0268f-123">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="0268f-123">-PersistOnSuccess</span></span>
<span data-ttu-id="0268f-124">Indica che l'azione di script deve essere eseguita ogni volta che il cluster viene ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="0268f-124">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="0268f-125">Questo parametro switch viene ignorato se l'azione di script non riesce inizialmente.</span><span class="sxs-lookup"><span data-stu-id="0268f-125">This switch parameter is ignored if the script action initially fails.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0268f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0268f-126">-ResourceGroupName</span></span>
<span data-ttu-id="0268f-127">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0268f-127">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0268f-128">-URI</span><span class="sxs-lookup"><span data-stu-id="0268f-128">-Uri</span></span>
<span data-ttu-id="0268f-129">Specifica l'URI pubblico per l'azione di script (uno script di PowerShell o bash).</span><span class="sxs-lookup"><span data-stu-id="0268f-129">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0268f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0268f-130">-DefaultProfile</span></span>
<span data-ttu-id="0268f-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0268f-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0268f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0268f-132">CommonParameters</span></span>
<span data-ttu-id="0268f-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0268f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0268f-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0268f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0268f-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0268f-135">INPUTS</span></span>

## <span data-ttu-id="0268f-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0268f-136">OUTPUTS</span></span>

### <span data-ttu-id="0268f-137">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptActionOperationResource</span><span class="sxs-lookup"><span data-stu-id="0268f-137">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="0268f-138">Note</span><span class="sxs-lookup"><span data-stu-id="0268f-138">NOTES</span></span>

## <span data-ttu-id="0268f-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0268f-139">RELATED LINKS</span></span>

[<span data-ttu-id="0268f-140">Add-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="0268f-140">Add-AzureRmHDInsightScriptAction</span></span>](./Add-AzureRmHDInsightScriptAction.md)


