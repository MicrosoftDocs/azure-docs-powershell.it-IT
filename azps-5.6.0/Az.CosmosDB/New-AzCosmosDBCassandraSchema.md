---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 3a19e0c60b5a32e1d1083b1afba55a8bf3045fe9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983613"
---
# <span data-ttu-id="7553f-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="7553f-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="7553f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7553f-102">SYNOPSIS</span></span>
<span data-ttu-id="7553f-103">Crea un nuovo schema Diedb Cassandra.</span><span class="sxs-lookup"><span data-stu-id="7553f-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="7553f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7553f-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7553f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7553f-105">DESCRIPTION</span></span>
<span data-ttu-id="7553f-106">**New-AzCosmosDBCassandraSchema** crea un nuovo SchemaDb Cassandra.</span><span class="sxs-lookup"><span data-stu-id="7553f-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="7553f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7553f-107">EXAMPLES</span></span>

### <span data-ttu-id="7553f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7553f-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="7553f-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7553f-109">PARAMETERS</span></span>

### <span data-ttu-id="7553f-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="7553f-110">-ClusterKey</span></span>
<span data-ttu-id="7553f-111">Matrice di oggetti PSClusterKey.</span><span class="sxs-lookup"><span data-stu-id="7553f-111">Array of PSClusterKey objects.</span></span>

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

### <span data-ttu-id="7553f-112">-Column</span><span class="sxs-lookup"><span data-stu-id="7553f-112">-Column</span></span>
<span data-ttu-id="7553f-113">Oggetto PSColumn.</span><span class="sxs-lookup"><span data-stu-id="7553f-113">PSColumn object.</span></span>

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

### <span data-ttu-id="7553f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7553f-114">-DefaultProfile</span></span>
<span data-ttu-id="7553f-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7553f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7553f-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="7553f-116">-PartitionKey</span></span>
<span data-ttu-id="7553f-117">Matrice di stringhe contenenti chiavi partition.</span><span class="sxs-lookup"><span data-stu-id="7553f-117">Array of strings containing Partition Keys.</span></span>

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

### <span data-ttu-id="7553f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7553f-118">CommonParameters</span></span>
<span data-ttu-id="7553f-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7553f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7553f-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7553f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7553f-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="7553f-121">INPUTS</span></span>

### <span data-ttu-id="7553f-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7553f-122">None</span></span>

## <span data-ttu-id="7553f-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7553f-123">OUTPUTS</span></span>

### <span data-ttu-id="7553f-124">Microsoft.Azure.Commands.ColumnsDB.Models.PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="7553f-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="7553f-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="7553f-125">NOTES</span></span>

## <span data-ttu-id="7553f-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7553f-126">RELATED LINKS</span></span>
