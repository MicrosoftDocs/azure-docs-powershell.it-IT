---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/set-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 573bb9534107a4df020e21269b5bdb2ec12db125
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984604"
---
# <span data-ttu-id="caea4-101">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="caea4-101">Set-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="caea4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="caea4-102">SYNOPSIS</span></span>
<span data-ttu-id="caea4-103">Imposta un'azione script eseguita in precedenza come azione di script persistente.</span><span class="sxs-lookup"><span data-stu-id="caea4-103">Sets a previously executed script action to be a persisted script action.</span></span>

## <span data-ttu-id="caea4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="caea4-104">SYNTAX</span></span>

```
Set-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="caea4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="caea4-105">DESCRIPTION</span></span>
<span data-ttu-id="caea4-106">Il cmdlet **Set-AzHDInsightPersistedScriptAction** imposta un'azione script eseguita in precedenza come azione di script persistente.</span><span class="sxs-lookup"><span data-stu-id="caea4-106">The **Set-AzHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="caea4-107">L'azione di script specificata deve avere avuto esito positivo in precedenza.</span><span class="sxs-lookup"><span data-stu-id="caea4-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="caea4-108">L'azione di script verrà eseguita ogni volta che il cluster Azure HDInsight viene ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="caea4-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="caea4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="caea4-109">EXAMPLES</span></span>

### <span data-ttu-id="caea4-110">Esempio 1: Impostare il persistere di un'azione di script riuscita in precedenza o eseguirlo sul cluster di ridimensionamento</span><span class="sxs-lookup"><span data-stu-id="caea4-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="caea4-111">Questo comando imposta un'azione di script eseguita in precedenza come azione di script persistente.</span><span class="sxs-lookup"><span data-stu-id="caea4-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="caea4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="caea4-112">PARAMETERS</span></span>

### <span data-ttu-id="caea4-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="caea4-113">-ClusterName</span></span>
<span data-ttu-id="caea4-114">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="caea4-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="caea4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caea4-115">-DefaultProfile</span></span>
<span data-ttu-id="caea4-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="caea4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="caea4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caea4-117">-ResourceGroupName</span></span>
<span data-ttu-id="caea4-118">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="caea4-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="caea4-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="caea4-119">-ScriptExecutionId</span></span>
<span data-ttu-id="caea4-120">Specifica l'ID di esecuzione dell'azione di script da alzare di livello a persistente.</span><span class="sxs-lookup"><span data-stu-id="caea4-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="caea4-121">Per alzare di livello l'azione di script deve essere stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="caea4-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="caea4-122">L'ID di esecuzione dell'azione script è possibile usare Get-AzHDInsightScriptActionHistory.</span><span class="sxs-lookup"><span data-stu-id="caea4-122">You can find the script action execution ID using Get-AzHDInsightScriptActionHistory.</span></span>

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

### <span data-ttu-id="caea4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caea4-123">CommonParameters</span></span>
<span data-ttu-id="caea4-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caea4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caea4-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="caea4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caea4-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="caea4-126">INPUTS</span></span>

### <span data-ttu-id="caea4-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="caea4-127">None</span></span>

## <span data-ttu-id="caea4-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="caea4-128">OUTPUTS</span></span>

### <span data-ttu-id="caea4-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="caea4-129">System.Void</span></span>

## <span data-ttu-id="caea4-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="caea4-130">NOTES</span></span>

## <span data-ttu-id="caea4-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="caea4-131">RELATED LINKS</span></span>

[<span data-ttu-id="caea4-132">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="caea4-132">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="caea4-133">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="caea4-133">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)


