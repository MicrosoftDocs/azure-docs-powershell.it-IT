---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: f58ba883cd724137d45632cabd293f0c7cdbefbd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033217"
---
# <span data-ttu-id="61337-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="61337-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="61337-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61337-102">SYNOPSIS</span></span>
<span data-ttu-id="61337-103">Crea una nuova chiave di cluster CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="61337-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="61337-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61337-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61337-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61337-105">DESCRIPTION</span></span>
<span data-ttu-id="61337-106">La **nuova AzCosmosDBCassandraClusterKey** crea una nuova chiave di cluster CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="61337-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="61337-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61337-107">EXAMPLES</span></span>

### <span data-ttu-id="61337-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="61337-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="61337-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61337-109">PARAMETERS</span></span>

### <span data-ttu-id="61337-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61337-110">-DefaultProfile</span></span>
<span data-ttu-id="61337-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61337-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61337-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="61337-112">-Name</span></span>
<span data-ttu-id="61337-113">Nome della chiave del cluster Cassandra.</span><span class="sxs-lookup"><span data-stu-id="61337-113">Name of Cassandra Cluster Key.</span></span>

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

### <span data-ttu-id="61337-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="61337-114">-OrderBy</span></span>
<span data-ttu-id="61337-115">Ordine della chiave del cluster Cassandra.</span><span class="sxs-lookup"><span data-stu-id="61337-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="61337-116">I valori possibili includono:' ASC ',' DESC '</span><span class="sxs-lookup"><span data-stu-id="61337-116">Possible values include: 'Asc', 'Desc'</span></span>

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

### <span data-ttu-id="61337-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61337-117">CommonParameters</span></span>
<span data-ttu-id="61337-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61337-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61337-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61337-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61337-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61337-120">INPUTS</span></span>

### <span data-ttu-id="61337-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="61337-121">None</span></span>

## <span data-ttu-id="61337-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61337-122">OUTPUTS</span></span>

### <span data-ttu-id="61337-123">Microsoft. Azure. Commands. CosmosDB. Models. PSClusterKey</span><span class="sxs-lookup"><span data-stu-id="61337-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="61337-124">Note</span><span class="sxs-lookup"><span data-stu-id="61337-124">NOTES</span></span>

## <span data-ttu-id="61337-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61337-125">RELATED LINKS</span></span>
