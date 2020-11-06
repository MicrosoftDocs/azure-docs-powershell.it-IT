---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/remove-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 7e24fac68efa4392944179d4a0618c0ad487c03f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521009"
---
# <span data-ttu-id="6dc52-101">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="6dc52-101">Remove-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="6dc52-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6dc52-102">SYNOPSIS</span></span>
<span data-ttu-id="6dc52-103">Rimuove un'azione di script persistente da un cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="6dc52-103">Removes an persisted script action from an HDInsight cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6dc52-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6dc52-104">SYNTAX</span></span>

```
Remove-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6dc52-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6dc52-105">DESCRIPTION</span></span>
<span data-ttu-id="6dc52-106">Il cmdlet **Remove-AzureRmHDInsightPersistedScriptAction** rimuove un'azione di script persistente dall'elenco di azioni di script persistenti del cluster di Azure HDInsight specificato.</span><span class="sxs-lookup"><span data-stu-id="6dc52-106">The **Remove-AzureRmHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="6dc52-107">Lo script rimosso non verrà più eseguito quando il cluster viene ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="6dc52-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="6dc52-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6dc52-108">EXAMPLES</span></span>

### <span data-ttu-id="6dc52-109">Esempio 1: rimuovere un'azione di script dall'elenco delle azioni di script permanenti in un cluster</span><span class="sxs-lookup"><span data-stu-id="6dc52-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzureRmHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="6dc52-110">Questo comando rimuove l'azione di script denominata ScriptAction dall'elenco delle azioni di script permanenti nel cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="6dc52-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="6dc52-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6dc52-111">PARAMETERS</span></span>

### <span data-ttu-id="6dc52-112">-Clustername</span><span class="sxs-lookup"><span data-stu-id="6dc52-112">-ClusterName</span></span>
<span data-ttu-id="6dc52-113">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="6dc52-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="6dc52-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dc52-114">-DefaultProfile</span></span>
<span data-ttu-id="6dc52-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6dc52-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6dc52-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="6dc52-116">-Name</span></span>
<span data-ttu-id="6dc52-117">Specifica il nome dell'azione di script persistente da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6dc52-117">Specifies the name of the persisted script action to be removed.</span></span>

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

### <span data-ttu-id="6dc52-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dc52-118">-ResourceGroupName</span></span>
<span data-ttu-id="6dc52-119">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6dc52-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6dc52-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dc52-120">CommonParameters</span></span>
<span data-ttu-id="6dc52-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dc52-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dc52-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dc52-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dc52-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6dc52-123">INPUTS</span></span>

### <span data-ttu-id="6dc52-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6dc52-124">None</span></span>

## <span data-ttu-id="6dc52-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6dc52-125">OUTPUTS</span></span>

### <span data-ttu-id="6dc52-126">System. void</span><span class="sxs-lookup"><span data-stu-id="6dc52-126">System.Void</span></span>

## <span data-ttu-id="6dc52-127">Note</span><span class="sxs-lookup"><span data-stu-id="6dc52-127">NOTES</span></span>

## <span data-ttu-id="6dc52-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6dc52-128">RELATED LINKS</span></span>

[<span data-ttu-id="6dc52-129">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="6dc52-129">Get-AzureRmHDInsightPersistedScriptAction</span></span>](./Get-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="6dc52-130">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="6dc52-130">Set-AzureRmHDInsightPersistedScriptAction</span></span>](./Set-AzureRmHDInsightPersistedScriptAction.md)


