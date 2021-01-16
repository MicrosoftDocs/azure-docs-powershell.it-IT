---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: f593989125642d03a9dff1b48bbc7430498b2a36
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475282"
---
# <span data-ttu-id="c2b4a-101">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="c2b4a-101">Set-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="c2b4a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2b4a-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b4a-103">Imposta un'azione di script eseguita in precedenza come azione di script persistente.</span><span class="sxs-lookup"><span data-stu-id="c2b4a-103">Sets a previously executed script action to be a persisted script action.</span></span>

## <span data-ttu-id="c2b4a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2b4a-104">SYNTAX</span></span>

```
Set-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2b4a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2b4a-105">DESCRIPTION</span></span>
<span data-ttu-id="c2b4a-106">Il cmdlet **set-AzHDInsightPersistedScriptAction** imposta un'azione di script eseguita in precedenza come azione di script persistente.</span><span class="sxs-lookup"><span data-stu-id="c2b4a-106">The **Set-AzHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="c2b4a-107">L'azione di script specificata deve essere stata completata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="c2b4a-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="c2b4a-108">L'azione script verrà eseguita ogni volta che viene ridimensionato il cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c2b4a-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="c2b4a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2b4a-109">EXAMPLES</span></span>

### <span data-ttu-id="c2b4a-110">Esempio 1: impostare un'azione di script in precedenza riuscita per essere mantenuta oppure eseguirla in scala cluster</span><span class="sxs-lookup"><span data-stu-id="c2b4a-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="c2b4a-111">Questo comando imposta un'azione di script in precedenza riuscita come azione di script persistente.</span><span class="sxs-lookup"><span data-stu-id="c2b4a-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="c2b4a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2b4a-112">PARAMETERS</span></span>

### <span data-ttu-id="c2b4a-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="c2b4a-113">-ClusterName</span></span>
<span data-ttu-id="c2b4a-114">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="c2b4a-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="c2b4a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b4a-115">-DefaultProfile</span></span>
<span data-ttu-id="c2b4a-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c2b4a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2b4a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2b4a-117">-ResourceGroupName</span></span>
<span data-ttu-id="c2b4a-118">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c2b4a-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c2b4a-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="c2b4a-119">-ScriptExecutionId</span></span>
<span data-ttu-id="c2b4a-120">Specifica l'ID di esecuzione dell'azione script da promuovere per la persistenza.</span><span class="sxs-lookup"><span data-stu-id="c2b4a-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="c2b4a-121">Questa azione di script deve essere stata completata per essere alzata di posizione.</span><span class="sxs-lookup"><span data-stu-id="c2b4a-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="c2b4a-122">Puoi trovare l'ID esecuzione delle azioni script usando Get-AzHDInsightScriptActionHistory.</span><span class="sxs-lookup"><span data-stu-id="c2b4a-122">You can find the script action execution ID using Get-AzHDInsightScriptActionHistory.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2b4a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b4a-123">CommonParameters</span></span>
<span data-ttu-id="c2b4a-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2b4a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b4a-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2b4a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b4a-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2b4a-126">INPUTS</span></span>

### <span data-ttu-id="c2b4a-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c2b4a-127">None</span></span>

## <span data-ttu-id="c2b4a-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2b4a-128">OUTPUTS</span></span>

### <span data-ttu-id="c2b4a-129">System. void</span><span class="sxs-lookup"><span data-stu-id="c2b4a-129">System.Void</span></span>

## <span data-ttu-id="c2b4a-130">Note</span><span class="sxs-lookup"><span data-stu-id="c2b4a-130">NOTES</span></span>

## <span data-ttu-id="c2b4a-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2b4a-131">RELATED LINKS</span></span>

[<span data-ttu-id="c2b4a-132">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="c2b4a-132">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="c2b4a-133">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="c2b4a-133">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)


