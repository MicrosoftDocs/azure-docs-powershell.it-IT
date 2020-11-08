---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 4d3d88fb5a8cca2343403870233e89b0f2073e8e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189863"
---
# <span data-ttu-id="d8c9a-101">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="d8c9a-101">Remove-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="d8c9a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d8c9a-102">SYNOPSIS</span></span>
<span data-ttu-id="d8c9a-103">Rimuove un'azione di script persistente da un cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-103">Removes an persisted script action from an HDInsight cluster.</span></span>

## <span data-ttu-id="d8c9a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8c9a-104">SYNTAX</span></span>

```
Remove-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8c9a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8c9a-105">DESCRIPTION</span></span>
<span data-ttu-id="d8c9a-106">Il cmdlet **Remove-AzHDInsightPersistedScriptAction** rimuove un'azione di script persistente dall'elenco di azioni di script persistenti del cluster di Azure HDInsight specificato.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-106">The **Remove-AzHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="d8c9a-107">Lo script rimosso non verrà più eseguito quando il cluster viene ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="d8c9a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8c9a-108">EXAMPLES</span></span>

### <span data-ttu-id="d8c9a-109">Esempio 1: rimuovere un'azione di script dall'elenco delle azioni di script permanenti in un cluster</span><span class="sxs-lookup"><span data-stu-id="d8c9a-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="d8c9a-110">Questo comando rimuove l'azione di script denominata ScriptAction dall'elenco delle azioni di script permanenti nel cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="d8c9a-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d8c9a-111">PARAMETERS</span></span>

### <span data-ttu-id="d8c9a-112">-Clustername</span><span class="sxs-lookup"><span data-stu-id="d8c9a-112">-ClusterName</span></span>
<span data-ttu-id="d8c9a-113">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="d8c9a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8c9a-114">-DefaultProfile</span></span>
<span data-ttu-id="d8c9a-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d8c9a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8c9a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="d8c9a-116">-Name</span></span>
<span data-ttu-id="d8c9a-117">Specifica il nome dell'azione di script persistente da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-117">Specifies the name of the persisted script action to be removed.</span></span>

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

### <span data-ttu-id="d8c9a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8c9a-118">-ResourceGroupName</span></span>
<span data-ttu-id="d8c9a-119">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d8c9a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8c9a-120">CommonParameters</span></span>
<span data-ttu-id="d8c9a-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8c9a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8c9a-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8c9a-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8c9a-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d8c9a-123">INPUTS</span></span>

### <span data-ttu-id="d8c9a-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d8c9a-124">None</span></span>

## <span data-ttu-id="d8c9a-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8c9a-125">OUTPUTS</span></span>

### <span data-ttu-id="d8c9a-126">System. void</span><span class="sxs-lookup"><span data-stu-id="d8c9a-126">System.Void</span></span>

## <span data-ttu-id="d8c9a-127">Note</span><span class="sxs-lookup"><span data-stu-id="d8c9a-127">NOTES</span></span>

## <span data-ttu-id="d8c9a-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8c9a-128">RELATED LINKS</span></span>

[<span data-ttu-id="d8c9a-129">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="d8c9a-129">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="d8c9a-130">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="d8c9a-130">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)

