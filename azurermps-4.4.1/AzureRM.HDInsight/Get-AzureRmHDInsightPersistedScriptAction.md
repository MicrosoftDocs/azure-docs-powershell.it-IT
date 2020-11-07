---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: d0ca241cc29bedcd3a34f866fa2b7a19fceb0745
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688310"
---
# <span data-ttu-id="a9033-101">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a9033-101">Get-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="a9033-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a9033-102">SYNOPSIS</span></span>
<span data-ttu-id="a9033-103">Ottiene le azioni di script permanenti per un cluster e le elenca in ordine cronologico oppure restituisce i dettagli per un'azione di script persistente specificata.</span><span class="sxs-lookup"><span data-stu-id="a9033-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9033-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9033-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9033-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9033-105">DESCRIPTION</span></span>
<span data-ttu-id="a9033-106">Il cmdlet **Get-AzureRmHDInsightPersistedScriptAction** ottiene le azioni di script permanenti per un cluster HDInsight di Azure e le elenca in ordine cronologico oppure restituisce i dettagli per un'azione di script persistente specificata.</span><span class="sxs-lookup"><span data-stu-id="a9033-106">The **Get-AzureRmHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="a9033-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9033-107">EXAMPLES</span></span>

### <span data-ttu-id="a9033-108">Esempio 1: ottenere le azioni di script permanenti in un cluster</span><span class="sxs-lookup"><span data-stu-id="a9033-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="a9033-109">Questo comando ottiene le azioni di script permanenti nel cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="a9033-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="a9033-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a9033-110">PARAMETERS</span></span>

### <span data-ttu-id="a9033-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="a9033-111">-ClusterName</span></span>
<span data-ttu-id="a9033-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="a9033-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="a9033-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a9033-113">-Name</span></span>
<span data-ttu-id="a9033-114">Specifica il nome dell'azione di script persistente.</span><span class="sxs-lookup"><span data-stu-id="a9033-114">Specifies the name of the persisted script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9033-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9033-115">-ResourceGroupName</span></span>
<span data-ttu-id="a9033-116">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a9033-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a9033-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9033-117">-DefaultProfile</span></span>
<span data-ttu-id="a9033-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a9033-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9033-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9033-119">CommonParameters</span></span>
<span data-ttu-id="a9033-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9033-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9033-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9033-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9033-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a9033-122">INPUTS</span></span>

## <span data-ttu-id="a9033-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9033-123">OUTPUTS</span></span>

### <span data-ttu-id="a9033-124">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptAction]</span><span class="sxs-lookup"><span data-stu-id="a9033-124">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction]</span></span>

## <span data-ttu-id="a9033-125">Note</span><span class="sxs-lookup"><span data-stu-id="a9033-125">NOTES</span></span>

## <span data-ttu-id="a9033-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9033-126">RELATED LINKS</span></span>

[<span data-ttu-id="a9033-127">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a9033-127">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](./Remove-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="a9033-128">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="a9033-128">Set-AzureRmHDInsightPersistedScriptAction</span></span>](./Set-AzureRmHDInsightPersistedScriptAction.md)


