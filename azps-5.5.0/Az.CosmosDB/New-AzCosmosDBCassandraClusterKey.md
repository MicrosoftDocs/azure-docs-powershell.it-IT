---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: f58ba883cd724137d45632cabd293f0c7cdbefbd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177302"
---
# <span data-ttu-id="cf825-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="cf825-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="cf825-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf825-102">SYNOPSIS</span></span>
<span data-ttu-id="cf825-103">Crea una nuova chiave cluster CassammasDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="cf825-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="cf825-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf825-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf825-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cf825-105">DESCRIPTION</span></span>
<span data-ttu-id="cf825-106">La **nuova chiave cluster New-AzCosmosDBCassandraClusterKey** crea una nuova chiave cluster Diedb Cassandra.</span><span class="sxs-lookup"><span data-stu-id="cf825-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="cf825-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf825-107">EXAMPLES</span></span>

### <span data-ttu-id="cf825-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cf825-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="cf825-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf825-109">PARAMETERS</span></span>

### <span data-ttu-id="cf825-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf825-110">-DefaultProfile</span></span>
<span data-ttu-id="cf825-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cf825-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf825-112">-Name</span><span class="sxs-lookup"><span data-stu-id="cf825-112">-Name</span></span>
<span data-ttu-id="cf825-113">Nome della chiave cluster Cassandra.</span><span class="sxs-lookup"><span data-stu-id="cf825-113">Name of Cassandra Cluster Key.</span></span>

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

### <span data-ttu-id="cf825-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="cf825-114">-OrderBy</span></span>
<span data-ttu-id="cf825-115">Ordinamento della chiave cluster Cassandra.</span><span class="sxs-lookup"><span data-stu-id="cf825-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="cf825-116">I valori possibili includono: 'Asc', 'Desc'</span><span class="sxs-lookup"><span data-stu-id="cf825-116">Possible values include: 'Asc', 'Desc'</span></span>

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

### <span data-ttu-id="cf825-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf825-117">CommonParameters</span></span>
<span data-ttu-id="cf825-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf825-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf825-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cf825-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf825-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="cf825-120">INPUTS</span></span>

### <span data-ttu-id="cf825-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="cf825-121">None</span></span>

## <span data-ttu-id="cf825-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf825-122">OUTPUTS</span></span>

### <span data-ttu-id="cf825-123">Microsoft.Azure.Commands.EnterpriseDb.Models.PSClusterKey</span><span class="sxs-lookup"><span data-stu-id="cf825-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="cf825-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="cf825-124">NOTES</span></span>

## <span data-ttu-id="cf825-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf825-125">RELATED LINKS</span></span>
