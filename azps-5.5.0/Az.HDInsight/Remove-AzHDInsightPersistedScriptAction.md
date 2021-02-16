---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 344c6fccd0f6c7db26110a94e2cacc53625df3d9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200199"
---
# <span data-ttu-id="83b11-101">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="83b11-101">Remove-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="83b11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83b11-102">SYNOPSIS</span></span>
<span data-ttu-id="83b11-103">Rimuove un'azione di script persistente da un cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="83b11-103">Removes an persisted script action from an HDInsight cluster.</span></span>

## <span data-ttu-id="83b11-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83b11-104">SYNTAX</span></span>

```
Remove-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83b11-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="83b11-105">DESCRIPTION</span></span>
<span data-ttu-id="83b11-106">Il cmdlet **Remove-AzHDInsightPersistedScriptAction** rimuove un'azione script persistente dall'elenco di azioni degli script persistenti del cluster Azure HDInsight specificato.</span><span class="sxs-lookup"><span data-stu-id="83b11-106">The **Remove-AzHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="83b11-107">Lo script rimosso non verrà più eseguito quando il cluster viene ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="83b11-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="83b11-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83b11-108">EXAMPLES</span></span>

### <span data-ttu-id="83b11-109">Esempio 1: Rimuovere un'azione script dall'elenco di azioni di script persistenti in un cluster</span><span class="sxs-lookup"><span data-stu-id="83b11-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="83b11-110">Questo comando rimuove l'azione script denominata Scriptaction dall'elenco di azioni di script persistenti nel cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="83b11-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="83b11-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83b11-111">PARAMETERS</span></span>

### <span data-ttu-id="83b11-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="83b11-112">-ClusterName</span></span>
<span data-ttu-id="83b11-113">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="83b11-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="83b11-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83b11-114">-DefaultProfile</span></span>
<span data-ttu-id="83b11-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="83b11-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83b11-116">-Name</span><span class="sxs-lookup"><span data-stu-id="83b11-116">-Name</span></span>
<span data-ttu-id="83b11-117">Specifica il nome dell'azione script persistente da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="83b11-117">Specifies the name of the persisted script action to be removed.</span></span>

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

### <span data-ttu-id="83b11-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83b11-118">-ResourceGroupName</span></span>
<span data-ttu-id="83b11-119">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="83b11-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="83b11-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83b11-120">CommonParameters</span></span>
<span data-ttu-id="83b11-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83b11-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83b11-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="83b11-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83b11-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="83b11-123">INPUTS</span></span>

### <span data-ttu-id="83b11-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="83b11-124">None</span></span>

## <span data-ttu-id="83b11-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83b11-125">OUTPUTS</span></span>

### <span data-ttu-id="83b11-126">System.Void</span><span class="sxs-lookup"><span data-stu-id="83b11-126">System.Void</span></span>

## <span data-ttu-id="83b11-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="83b11-127">NOTES</span></span>

## <span data-ttu-id="83b11-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83b11-128">RELATED LINKS</span></span>

[<span data-ttu-id="83b11-129">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="83b11-129">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="83b11-130">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="83b11-130">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


