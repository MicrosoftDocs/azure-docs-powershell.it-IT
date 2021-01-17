---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/New-azstorageobjectreplicationpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
ms.openlocfilehash: c8d41300250e41548cf949248b02c819b7da497f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324755"
---
# <span data-ttu-id="0947a-101">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="0947a-101">New-AzStorageObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="0947a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0947a-102">SYNOPSIS</span></span>
<span data-ttu-id="0947a-103">Crea una regola di criteri di replica degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="0947a-103">Creates an object replication policy rule.</span></span>

## <span data-ttu-id="0947a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0947a-104">SYNTAX</span></span>

```
New-AzStorageObjectReplicationPolicyRule -SourceContainer <String> -DestinationContainer <String>
 [-PrefixMatch <String[]>] [-MinCreationTime <DateTime>] [-RuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0947a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0947a-105">DESCRIPTION</span></span>
<span data-ttu-id="0947a-106">Il cmdlet **Get-AzStorageObjectReplicationPolicy** crea una regola di criteri di replica degli oggetti, che verrà usata nel cmdlet Set-AzStorageObjectReplicationPolicy.</span><span class="sxs-lookup"><span data-stu-id="0947a-106">The **Get-AzStorageObjectReplicationPolicy** cmdlet creates an object replication policy rule, which will be used in Set-AzStorageObjectReplicationPolicy cmdlet.</span></span>

## <span data-ttu-id="0947a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0947a-107">EXAMPLES</span></span>

### <span data-ttu-id="0947a-108">Esempio 1: creare una regola di criteri di replica degli oggetti con solo l'account di origine e di destinazione e visualizzare le relative proprietà</span><span class="sxs-lookup"><span data-stu-id="0947a-108">Example 1: Create an object replication policy rule with only source and destination account, and show its properties</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule1

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src1            dest1                {}
```

<span data-ttu-id="0947a-109">Questo comando crea una regola di criteri di replica degli oggetti con solo l'account di origine e di destinazione e ne mostra le proprietà.</span><span class="sxs-lookup"><span data-stu-id="0947a-109">This command creates an object replication policy rule with only source and destination account, and show its properties.</span></span>

### <span data-ttu-id="0947a-110">Esempio 2: creare una regola di criteri di replica degli oggetti con tutte le proprietà e mostrarne le proprietà</span><span class="sxs-lookup"><span data-stu-id="0947a-110">Example 2: Create an object replication policy rule with all properties, and show its properties</span></span>
```
PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $rule2

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="0947a-111">Questo comando regola un criterio di replica degli oggetti con tutte le proprietà e ne mostra le proprietà.</span><span class="sxs-lookup"><span data-stu-id="0947a-111">This command an object replication policy rule with all properties, and show its properties.</span></span>

## <span data-ttu-id="0947a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0947a-112">PARAMETERS</span></span>

### <span data-ttu-id="0947a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0947a-113">-DefaultProfile</span></span>
<span data-ttu-id="0947a-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0947a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0947a-115">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="0947a-115">-DestinationContainer</span></span>
<span data-ttu-id="0947a-116">Il nome del contenitore di destinazione in cui eseguire la replica.</span><span class="sxs-lookup"><span data-stu-id="0947a-116">The Destination Container name to replicate to.</span></span>

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

### <span data-ttu-id="0947a-117">-MinCreationTime</span><span class="sxs-lookup"><span data-stu-id="0947a-117">-MinCreationTime</span></span>
<span data-ttu-id="0947a-118">I BLOB creati dopo l'ora verranno replicati nella destinazione.</span><span class="sxs-lookup"><span data-stu-id="0947a-118">Blobs created after the time will be replicated to the destination..</span></span>

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

### <span data-ttu-id="0947a-119">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="0947a-119">-PrefixMatch</span></span>
<span data-ttu-id="0947a-120">Filtra i risultati per replicare solo i BLOB i cui nomi iniziano con il prefisso specificato.</span><span class="sxs-lookup"><span data-stu-id="0947a-120">Filters the results to replicate only blobs whose names begin with the specified prefix.</span></span>

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

### <span data-ttu-id="0947a-121">-RuleId</span><span class="sxs-lookup"><span data-stu-id="0947a-121">-RuleId</span></span>
<span data-ttu-id="0947a-122">ID regola di replica degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="0947a-122">Object Replication Rule Id.</span></span>

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

### <span data-ttu-id="0947a-123">-SourceContainer</span><span class="sxs-lookup"><span data-stu-id="0947a-123">-SourceContainer</span></span>
<span data-ttu-id="0947a-124">Il nome del contenitore di origine da cui eseguire la replica.</span><span class="sxs-lookup"><span data-stu-id="0947a-124">The Source Container name to replicate from.</span></span>

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

### <span data-ttu-id="0947a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0947a-125">CommonParameters</span></span>
<span data-ttu-id="0947a-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0947a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0947a-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0947a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0947a-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0947a-128">INPUTS</span></span>

### <span data-ttu-id="0947a-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0947a-129">None</span></span>

## <span data-ttu-id="0947a-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0947a-130">OUTPUTS</span></span>

### <span data-ttu-id="0947a-131">Microsoft. Azure. Commands. Management. storage. Models. PSObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="0947a-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="0947a-132">Note</span><span class="sxs-lookup"><span data-stu-id="0947a-132">NOTES</span></span>

## <span data-ttu-id="0947a-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0947a-133">RELATED LINKS</span></span>
