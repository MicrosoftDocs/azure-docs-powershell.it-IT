---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/New-azstorageobjectreplicationpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
ms.openlocfilehash: 8338f13829ebc3feff4c5a81fdfb3bd13934d90d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002445"
---
# <span data-ttu-id="58b18-101">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="58b18-101">New-AzStorageObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="58b18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58b18-102">SYNOPSIS</span></span>
<span data-ttu-id="58b18-103">Crea una regola dei criteri di replica degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="58b18-103">Creates an object replication policy rule.</span></span>

## <span data-ttu-id="58b18-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58b18-104">SYNTAX</span></span>

```
New-AzStorageObjectReplicationPolicyRule -SourceContainer <String> -DestinationContainer <String>
 [-PrefixMatch <String[]>] [-MinCreationTime <DateTime>] [-RuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58b18-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="58b18-105">DESCRIPTION</span></span>
<span data-ttu-id="58b18-106">Il cmdlet **Get-AzStorageObjectReplicationPolicy** crea una regola dei criteri di replica degli oggetti, che verrà usata Set-AzStorageObjectReplicationPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58b18-106">The **Get-AzStorageObjectReplicationPolicy** cmdlet creates an object replication policy rule, which will be used in Set-AzStorageObjectReplicationPolicy cmdlet.</span></span>

## <span data-ttu-id="58b18-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58b18-107">EXAMPLES</span></span>

### <span data-ttu-id="58b18-108">Esempio 1: Creare una regola dei criteri di replica degli oggetti con solo account di origine e di destinazione e visualizzarne le proprietà</span><span class="sxs-lookup"><span data-stu-id="58b18-108">Example 1: Create an object replication policy rule with only source and destination account, and show its properties</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule1

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src1            dest1                {}
```

<span data-ttu-id="58b18-109">Questo comando crea una regola dei criteri di replica degli oggetti con solo account di origine e di destinazione e ne mostra le proprietà.</span><span class="sxs-lookup"><span data-stu-id="58b18-109">This command creates an object replication policy rule with only source and destination account, and show its properties.</span></span>

### <span data-ttu-id="58b18-110">Esempio 2: Creare una regola dei criteri di replica degli oggetti con tutte le proprietà e visualizzarne le proprietà</span><span class="sxs-lookup"><span data-stu-id="58b18-110">Example 2: Create an object replication policy rule with all properties, and show its properties</span></span>
```
PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $rule2

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="58b18-111">Comando che consente di eseguire una regola dei criteri di replica degli oggetti con tutte le proprietà e di visualizzarne le proprietà.</span><span class="sxs-lookup"><span data-stu-id="58b18-111">This command an object replication policy rule with all properties, and show its properties.</span></span>

## <span data-ttu-id="58b18-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58b18-112">PARAMETERS</span></span>

### <span data-ttu-id="58b18-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58b18-113">-DefaultProfile</span></span>
<span data-ttu-id="58b18-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="58b18-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58b18-115">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="58b18-115">-DestinationContainer</span></span>
<span data-ttu-id="58b18-116">Nome del contenitore di destinazione in cui eseguire la replica.</span><span class="sxs-lookup"><span data-stu-id="58b18-116">The Destination Container name to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58b18-117">-MinCreationTime</span><span class="sxs-lookup"><span data-stu-id="58b18-117">-MinCreationTime</span></span>
<span data-ttu-id="58b18-118">I BLOB creati dopo il tempo verranno replicati nella destinazione.</span><span class="sxs-lookup"><span data-stu-id="58b18-118">Blobs created after the time will be replicated to the destination..</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58b18-119">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="58b18-119">-PrefixMatch</span></span>
<span data-ttu-id="58b18-120">Filtra i risultati per replicare solo i BLOB i cui nomi iniziano con il prefisso specificato.</span><span class="sxs-lookup"><span data-stu-id="58b18-120">Filters the results to replicate only blobs whose names begin with the specified prefix.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58b18-121">-RuleId</span><span class="sxs-lookup"><span data-stu-id="58b18-121">-RuleId</span></span>
<span data-ttu-id="58b18-122">ID regola di replica oggetti.</span><span class="sxs-lookup"><span data-stu-id="58b18-122">Object Replication Rule Id.</span></span>

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

### <span data-ttu-id="58b18-123">-SourceContainer</span><span class="sxs-lookup"><span data-stu-id="58b18-123">-SourceContainer</span></span>
<span data-ttu-id="58b18-124">Nome del contenitore di origine da cui eseguire la replica.</span><span class="sxs-lookup"><span data-stu-id="58b18-124">The Source Container name to replicate from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58b18-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58b18-125">CommonParameters</span></span>
<span data-ttu-id="58b18-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58b18-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58b18-127">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58b18-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58b18-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="58b18-128">INPUTS</span></span>

### <span data-ttu-id="58b18-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="58b18-129">None</span></span>

## <span data-ttu-id="58b18-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58b18-130">OUTPUTS</span></span>

### <span data-ttu-id="58b18-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="58b18-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="58b18-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="58b18-132">NOTES</span></span>

## <span data-ttu-id="58b18-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58b18-133">RELATED LINKS</span></span>
