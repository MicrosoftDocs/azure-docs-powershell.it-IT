---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: f58ba883cd724137d45632cabd293f0c7cdbefbd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347140"
---
# <span data-ttu-id="16089-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="16089-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="16089-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="16089-102">SYNOPSIS</span></span>
<span data-ttu-id="16089-103">Crea una nuova chiave di cluster CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="16089-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="16089-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16089-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16089-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16089-105">DESCRIPTION</span></span>
<span data-ttu-id="16089-106">La **nuova AzCosmosDBCassandraClusterKey** crea una nuova chiave di cluster CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="16089-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="16089-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16089-107">EXAMPLES</span></span>

### <span data-ttu-id="16089-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="16089-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="16089-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="16089-109">PARAMETERS</span></span>

### <span data-ttu-id="16089-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16089-110">-DefaultProfile</span></span>
<span data-ttu-id="16089-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16089-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16089-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="16089-112">-Name</span></span>
<span data-ttu-id="16089-113">Nome della chiave del cluster Cassandra.</span><span class="sxs-lookup"><span data-stu-id="16089-113">Name of Cassandra Cluster Key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16089-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="16089-114">-OrderBy</span></span>
<span data-ttu-id="16089-115">Ordine della chiave del cluster Cassandra.</span><span class="sxs-lookup"><span data-stu-id="16089-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="16089-116">I valori possibili includono:' ASC ',' DESC '</span><span class="sxs-lookup"><span data-stu-id="16089-116">Possible values include: 'Asc', 'Desc'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16089-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16089-117">CommonParameters</span></span>
<span data-ttu-id="16089-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16089-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16089-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16089-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16089-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="16089-120">INPUTS</span></span>

### <span data-ttu-id="16089-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="16089-121">None</span></span>

## <span data-ttu-id="16089-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16089-122">OUTPUTS</span></span>

### <span data-ttu-id="16089-123">Microsoft. Azure. Commands. CosmosDB. Models. PSClusterKey</span><span class="sxs-lookup"><span data-stu-id="16089-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="16089-124">Note</span><span class="sxs-lookup"><span data-stu-id="16089-124">NOTES</span></span>

## <span data-ttu-id="16089-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16089-125">RELATED LINKS</span></span>
