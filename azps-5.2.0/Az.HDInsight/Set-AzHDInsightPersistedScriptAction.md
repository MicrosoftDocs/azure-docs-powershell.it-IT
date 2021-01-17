---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: bff21d969a88282f3ba3c1d79d1f717c3c169265
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322851"
---
# <span data-ttu-id="73698-101">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="73698-101">Set-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="73698-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="73698-102">SYNOPSIS</span></span>
<span data-ttu-id="73698-103">Imposta un'azione di script eseguita in precedenza come azione di script persistente.</span><span class="sxs-lookup"><span data-stu-id="73698-103">Sets a previously executed script action to be a persisted script action.</span></span>

## <span data-ttu-id="73698-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="73698-104">SYNTAX</span></span>

```
Set-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73698-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73698-105">DESCRIPTION</span></span>
<span data-ttu-id="73698-106">Il cmdlet **set-AzHDInsightPersistedScriptAction** imposta un'azione di script eseguita in precedenza come azione di script persistente.</span><span class="sxs-lookup"><span data-stu-id="73698-106">The **Set-AzHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="73698-107">L'azione di script specificata deve essere stata completata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="73698-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="73698-108">L'azione script verrà eseguita ogni volta che viene ridimensionato il cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="73698-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="73698-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="73698-109">EXAMPLES</span></span>

### <span data-ttu-id="73698-110">Esempio 1: impostare un'azione di script in precedenza riuscita per essere mantenuta oppure eseguirla in scala cluster</span><span class="sxs-lookup"><span data-stu-id="73698-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="73698-111">Questo comando imposta un'azione di script in precedenza riuscita come azione di script persistente.</span><span class="sxs-lookup"><span data-stu-id="73698-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="73698-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="73698-112">PARAMETERS</span></span>

### <span data-ttu-id="73698-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="73698-113">-ClusterName</span></span>
<span data-ttu-id="73698-114">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="73698-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="73698-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73698-115">-DefaultProfile</span></span>
<span data-ttu-id="73698-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="73698-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73698-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73698-117">-ResourceGroupName</span></span>
<span data-ttu-id="73698-118">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="73698-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="73698-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="73698-119">-ScriptExecutionId</span></span>
<span data-ttu-id="73698-120">Specifica l'ID di esecuzione dell'azione script da promuovere per la persistenza.</span><span class="sxs-lookup"><span data-stu-id="73698-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="73698-121">Questa azione di script deve essere stata completata per essere alzata di posizione.</span><span class="sxs-lookup"><span data-stu-id="73698-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="73698-122">Puoi trovare l'ID esecuzione delle azioni script usando Get-AzHDInsightScriptActionHistory.</span><span class="sxs-lookup"><span data-stu-id="73698-122">You can find the script action execution ID using Get-AzHDInsightScriptActionHistory.</span></span>

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

### <span data-ttu-id="73698-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73698-123">CommonParameters</span></span>
<span data-ttu-id="73698-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73698-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73698-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73698-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73698-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="73698-126">INPUTS</span></span>

### <span data-ttu-id="73698-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="73698-127">None</span></span>

## <span data-ttu-id="73698-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="73698-128">OUTPUTS</span></span>

### <span data-ttu-id="73698-129">System. void</span><span class="sxs-lookup"><span data-stu-id="73698-129">System.Void</span></span>

## <span data-ttu-id="73698-130">Note</span><span class="sxs-lookup"><span data-stu-id="73698-130">NOTES</span></span>

## <span data-ttu-id="73698-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="73698-131">RELATED LINKS</span></span>

[<span data-ttu-id="73698-132">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="73698-132">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="73698-133">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="73698-133">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)


