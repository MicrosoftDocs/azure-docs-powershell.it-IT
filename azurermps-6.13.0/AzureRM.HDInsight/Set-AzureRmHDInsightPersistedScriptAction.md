---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 07f501be4ac775a9d80c43173e13fccf3057cc26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510988"
---
# <span data-ttu-id="96b7c-101">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="96b7c-101">Set-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="96b7c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="96b7c-102">SYNOPSIS</span></span>
<span data-ttu-id="96b7c-103">Imposta un'azione di script eseguita in precedenza come azione di script persistente.</span><span class="sxs-lookup"><span data-stu-id="96b7c-103">Sets a previously executed script action to be a persisted script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96b7c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96b7c-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96b7c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96b7c-105">DESCRIPTION</span></span>
<span data-ttu-id="96b7c-106">Il cmdlet **set-AzureRmHDInsightPersistedScriptAction** imposta un'azione di script eseguita in precedenza come azione di script persistente.</span><span class="sxs-lookup"><span data-stu-id="96b7c-106">The **Set-AzureRmHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="96b7c-107">L'azione di script specificata deve essere stata completata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="96b7c-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="96b7c-108">L'azione script verrà eseguita ogni volta che viene ridimensionato il cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="96b7c-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="96b7c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96b7c-109">EXAMPLES</span></span>

### <span data-ttu-id="96b7c-110">Esempio 1: impostare un'azione di script in precedenza riuscita per essere mantenuta oppure eseguirla in scala cluster</span><span class="sxs-lookup"><span data-stu-id="96b7c-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzureRmHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="96b7c-111">Questo comando imposta un'azione di script in precedenza riuscita come azione di script persistente.</span><span class="sxs-lookup"><span data-stu-id="96b7c-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="96b7c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="96b7c-112">PARAMETERS</span></span>

### <span data-ttu-id="96b7c-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="96b7c-113">-ClusterName</span></span>
<span data-ttu-id="96b7c-114">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="96b7c-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="96b7c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96b7c-115">-DefaultProfile</span></span>
<span data-ttu-id="96b7c-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="96b7c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96b7c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96b7c-117">-ResourceGroupName</span></span>
<span data-ttu-id="96b7c-118">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="96b7c-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="96b7c-119">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="96b7c-119">-ScriptExecutionId</span></span>
<span data-ttu-id="96b7c-120">Specifica l'ID di esecuzione dell'azione script da promuovere per la persistenza.</span><span class="sxs-lookup"><span data-stu-id="96b7c-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="96b7c-121">Questa azione di script deve essere stata completata per essere alzata di posizione.</span><span class="sxs-lookup"><span data-stu-id="96b7c-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="96b7c-122">Puoi trovare l'ID esecuzione delle azioni script usando Get-AzureRmHDInsightScriptActionHistory.</span><span class="sxs-lookup"><span data-stu-id="96b7c-122">You can find the script action execution ID using Get-AzureRmHDInsightScriptActionHistory.</span></span>

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

### <span data-ttu-id="96b7c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96b7c-123">CommonParameters</span></span>
<span data-ttu-id="96b7c-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96b7c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96b7c-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96b7c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96b7c-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="96b7c-126">INPUTS</span></span>

### <span data-ttu-id="96b7c-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="96b7c-127">None</span></span>

## <span data-ttu-id="96b7c-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96b7c-128">OUTPUTS</span></span>

### <span data-ttu-id="96b7c-129">System. void</span><span class="sxs-lookup"><span data-stu-id="96b7c-129">System.Void</span></span>

## <span data-ttu-id="96b7c-130">Note</span><span class="sxs-lookup"><span data-stu-id="96b7c-130">NOTES</span></span>

## <span data-ttu-id="96b7c-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96b7c-131">RELATED LINKS</span></span>

[<span data-ttu-id="96b7c-132">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="96b7c-132">Get-AzureRmHDInsightPersistedScriptAction</span></span>](./Get-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="96b7c-133">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="96b7c-133">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](./Remove-AzureRmHDInsightPersistedScriptAction.md)


