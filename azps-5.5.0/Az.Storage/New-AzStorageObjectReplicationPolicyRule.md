---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/New-azstorageobjectreplicationpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
ms.openlocfilehash: c8d41300250e41548cf949248b02c819b7da497f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190839"
---
# <span data-ttu-id="b6450-101">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="b6450-101">New-AzStorageObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="b6450-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6450-102">SYNOPSIS</span></span>
<span data-ttu-id="b6450-103">Crea una regola dei criteri di replica degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="b6450-103">Creates an object replication policy rule.</span></span>

## <span data-ttu-id="b6450-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6450-104">SYNTAX</span></span>

```
New-AzStorageObjectReplicationPolicyRule -SourceContainer <String> -DestinationContainer <String>
 [-PrefixMatch <String[]>] [-MinCreationTime <DateTime>] [-RuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6450-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b6450-105">DESCRIPTION</span></span>
<span data-ttu-id="b6450-106">Il cmdlet **Get-AzStorageObjectReplicationPolicy** crea una regola dei criteri di replica degli oggetti, che verrà usata Set-AzStorageObjectReplicationPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6450-106">The **Get-AzStorageObjectReplicationPolicy** cmdlet creates an object replication policy rule, which will be used in Set-AzStorageObjectReplicationPolicy cmdlet.</span></span>

## <span data-ttu-id="b6450-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6450-107">EXAMPLES</span></span>

### <span data-ttu-id="b6450-108">Esempio 1: Creare una regola dei criteri di replica degli oggetti con solo account di origine e di destinazione e visualizzarne le proprietà</span><span class="sxs-lookup"><span data-stu-id="b6450-108">Example 1: Create an object replication policy rule with only source and destination account, and show its properties</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule1

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src1            dest1                {}
```

<span data-ttu-id="b6450-109">Questo comando crea una regola dei criteri di replica degli oggetti con solo account di origine e di destinazione e ne mostra le proprietà.</span><span class="sxs-lookup"><span data-stu-id="b6450-109">This command creates an object replication policy rule with only source and destination account, and show its properties.</span></span>

### <span data-ttu-id="b6450-110">Esempio 2: Creare una regola dei criteri di replica degli oggetti con tutte le proprietà e visualizzarne le proprietà</span><span class="sxs-lookup"><span data-stu-id="b6450-110">Example 2: Create an object replication policy rule with all properties, and show its properties</span></span>
```
PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $rule2

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="b6450-111">Comando che consente di eseguire una regola dei criteri di replica degli oggetti con tutte le proprietà e di visualizzarne le proprietà.</span><span class="sxs-lookup"><span data-stu-id="b6450-111">This command an object replication policy rule with all properties, and show its properties.</span></span>

## <span data-ttu-id="b6450-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6450-112">PARAMETERS</span></span>

### <span data-ttu-id="b6450-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6450-113">-DefaultProfile</span></span>
<span data-ttu-id="b6450-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6450-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6450-115">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="b6450-115">-DestinationContainer</span></span>
<span data-ttu-id="b6450-116">Nome del contenitore di destinazione in cui eseguire la replica.</span><span class="sxs-lookup"><span data-stu-id="b6450-116">The Destination Container name to replicate to.</span></span>

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

### <span data-ttu-id="b6450-117">-MinCreationTime</span><span class="sxs-lookup"><span data-stu-id="b6450-117">-MinCreationTime</span></span>
<span data-ttu-id="b6450-118">I BLOB creati dopo il tempo verranno replicati nella destinazione.</span><span class="sxs-lookup"><span data-stu-id="b6450-118">Blobs created after the time will be replicated to the destination..</span></span>

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

### <span data-ttu-id="b6450-119">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="b6450-119">-PrefixMatch</span></span>
<span data-ttu-id="b6450-120">Filtra i risultati per replicare solo i BLOB i cui nomi iniziano con il prefisso specificato.</span><span class="sxs-lookup"><span data-stu-id="b6450-120">Filters the results to replicate only blobs whose names begin with the specified prefix.</span></span>

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

### <span data-ttu-id="b6450-121">-RuleId</span><span class="sxs-lookup"><span data-stu-id="b6450-121">-RuleId</span></span>
<span data-ttu-id="b6450-122">ID regola di replica oggetti.</span><span class="sxs-lookup"><span data-stu-id="b6450-122">Object Replication Rule Id.</span></span>

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

### <span data-ttu-id="b6450-123">-SourceContainer</span><span class="sxs-lookup"><span data-stu-id="b6450-123">-SourceContainer</span></span>
<span data-ttu-id="b6450-124">Nome del contenitore di origine da cui eseguire la replica.</span><span class="sxs-lookup"><span data-stu-id="b6450-124">The Source Container name to replicate from.</span></span>

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

### <span data-ttu-id="b6450-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6450-125">CommonParameters</span></span>
<span data-ttu-id="b6450-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6450-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6450-127">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6450-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6450-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="b6450-128">INPUTS</span></span>

### <span data-ttu-id="b6450-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b6450-129">None</span></span>

## <span data-ttu-id="b6450-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6450-130">OUTPUTS</span></span>

### <span data-ttu-id="b6450-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="b6450-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="b6450-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="b6450-132">NOTES</span></span>

## <span data-ttu-id="b6450-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6450-133">RELATED LINKS</span></span>
