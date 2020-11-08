---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 997f9e0751eb616fdc9e64f73d66b3f15b7ed756
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033214"
---
# <span data-ttu-id="fb011-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="fb011-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="fb011-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fb011-102">SYNOPSIS</span></span>
<span data-ttu-id="fb011-103">Crea un nuovo schema di CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="fb011-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="fb011-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb011-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb011-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb011-105">DESCRIPTION</span></span>
<span data-ttu-id="fb011-106">Il **nuovo-AzCosmosDBCassandraSchema** crea un nuovo schema di CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="fb011-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="fb011-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb011-107">EXAMPLES</span></span>

### <span data-ttu-id="fb011-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fb011-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="fb011-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fb011-109">PARAMETERS</span></span>

### <span data-ttu-id="fb011-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="fb011-110">-ClusterKey</span></span>
<span data-ttu-id="fb011-111">Matrice di oggetti PSClusterKey.</span><span class="sxs-lookup"><span data-stu-id="fb011-111">Array of PSClusterKey objects.</span></span>

```yaml
Type: PSClusterKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb011-112">-Colonna</span><span class="sxs-lookup"><span data-stu-id="fb011-112">-Column</span></span>
<span data-ttu-id="fb011-113">Oggetto PSColumn.</span><span class="sxs-lookup"><span data-stu-id="fb011-113">PSColumn object.</span></span>

```yaml
Type: PSColumn[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb011-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb011-114">-DefaultProfile</span></span>
<span data-ttu-id="fb011-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fb011-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb011-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="fb011-116">-PartitionKey</span></span>
<span data-ttu-id="fb011-117">Matrice di stringhe che contengono le chiavi di partizione.</span><span class="sxs-lookup"><span data-stu-id="fb011-117">Array of strings containing Partition Keys.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb011-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb011-118">CommonParameters</span></span>
<span data-ttu-id="fb011-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb011-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb011-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb011-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb011-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fb011-121">INPUTS</span></span>

### <span data-ttu-id="fb011-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fb011-122">None</span></span>

## <span data-ttu-id="fb011-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb011-123">OUTPUTS</span></span>

### <span data-ttu-id="fb011-124">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="fb011-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="fb011-125">Note</span><span class="sxs-lookup"><span data-stu-id="fb011-125">NOTES</span></span>

## <span data-ttu-id="fb011-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb011-126">RELATED LINKS</span></span>
