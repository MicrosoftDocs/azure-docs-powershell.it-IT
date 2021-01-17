---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 997f9e0751eb616fdc9e64f73d66b3f15b7ed756
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368462"
---
# <span data-ttu-id="bd0cf-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="bd0cf-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="bd0cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bd0cf-102">SYNOPSIS</span></span>
<span data-ttu-id="bd0cf-103">Crea un nuovo schema di CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="bd0cf-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="bd0cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd0cf-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd0cf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd0cf-105">DESCRIPTION</span></span>
<span data-ttu-id="bd0cf-106">Il **nuovo-AzCosmosDBCassandraSchema** crea un nuovo schema di CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="bd0cf-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="bd0cf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd0cf-107">EXAMPLES</span></span>

### <span data-ttu-id="bd0cf-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bd0cf-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="bd0cf-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bd0cf-109">PARAMETERS</span></span>

### <span data-ttu-id="bd0cf-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="bd0cf-110">-ClusterKey</span></span>
<span data-ttu-id="bd0cf-111">Matrice di oggetti PSClusterKey.</span><span class="sxs-lookup"><span data-stu-id="bd0cf-111">Array of PSClusterKey objects.</span></span>

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

### <span data-ttu-id="bd0cf-112">-Colonna</span><span class="sxs-lookup"><span data-stu-id="bd0cf-112">-Column</span></span>
<span data-ttu-id="bd0cf-113">Oggetto PSColumn.</span><span class="sxs-lookup"><span data-stu-id="bd0cf-113">PSColumn object.</span></span>

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

### <span data-ttu-id="bd0cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd0cf-114">-DefaultProfile</span></span>
<span data-ttu-id="bd0cf-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bd0cf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd0cf-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="bd0cf-116">-PartitionKey</span></span>
<span data-ttu-id="bd0cf-117">Matrice di stringhe che contengono le chiavi di partizione.</span><span class="sxs-lookup"><span data-stu-id="bd0cf-117">Array of strings containing Partition Keys.</span></span>

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

### <span data-ttu-id="bd0cf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd0cf-118">CommonParameters</span></span>
<span data-ttu-id="bd0cf-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd0cf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd0cf-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd0cf-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd0cf-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bd0cf-121">INPUTS</span></span>

### <span data-ttu-id="bd0cf-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bd0cf-122">None</span></span>

## <span data-ttu-id="bd0cf-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd0cf-123">OUTPUTS</span></span>

### <span data-ttu-id="bd0cf-124">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="bd0cf-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="bd0cf-125">Note</span><span class="sxs-lookup"><span data-stu-id="bd0cf-125">NOTES</span></span>

## <span data-ttu-id="bd0cf-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd0cf-126">RELATED LINKS</span></span>
