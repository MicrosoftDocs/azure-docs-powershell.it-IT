---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: 9afcffc281c48e0235c814b352e65ae47e5f4337
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009742"
---
# <span data-ttu-id="92fd3-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="92fd3-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="92fd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92fd3-102">SYNOPSIS</span></span>
<span data-ttu-id="92fd3-103">Crea una nuova chiave cluster CassammasDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="92fd3-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="92fd3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92fd3-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92fd3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="92fd3-105">DESCRIPTION</span></span>
<span data-ttu-id="92fd3-106">La **nuova chiave cluster New-AzCosmosDBCassandraClusterKey** crea una nuova chiave cluster Diedb Cassandra.</span><span class="sxs-lookup"><span data-stu-id="92fd3-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="92fd3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92fd3-107">EXAMPLES</span></span>

### <span data-ttu-id="92fd3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="92fd3-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="92fd3-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92fd3-109">PARAMETERS</span></span>

### <span data-ttu-id="92fd3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92fd3-110">-DefaultProfile</span></span>
<span data-ttu-id="92fd3-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="92fd3-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92fd3-112">-Name</span><span class="sxs-lookup"><span data-stu-id="92fd3-112">-Name</span></span>
<span data-ttu-id="92fd3-113">Nome della chiave cluster Cassandra.</span><span class="sxs-lookup"><span data-stu-id="92fd3-113">Name of Cassandra Cluster Key.</span></span>

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

### <span data-ttu-id="92fd3-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="92fd3-114">-OrderBy</span></span>
<span data-ttu-id="92fd3-115">Ordinamento della chiave cluster Cassandra.</span><span class="sxs-lookup"><span data-stu-id="92fd3-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="92fd3-116">I valori possibili includono: 'Asc', 'Desc'</span><span class="sxs-lookup"><span data-stu-id="92fd3-116">Possible values include: 'Asc', 'Desc'</span></span>

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

### <span data-ttu-id="92fd3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92fd3-117">CommonParameters</span></span>
<span data-ttu-id="92fd3-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92fd3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92fd3-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="92fd3-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92fd3-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="92fd3-120">INPUTS</span></span>

### <span data-ttu-id="92fd3-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="92fd3-121">None</span></span>

## <span data-ttu-id="92fd3-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92fd3-122">OUTPUTS</span></span>

### <span data-ttu-id="92fd3-123">Microsoft.Azure.Commands.EnterpriseDb.Models.PSClusterKey</span><span class="sxs-lookup"><span data-stu-id="92fd3-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="92fd3-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="92fd3-124">NOTES</span></span>

## <span data-ttu-id="92fd3-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92fd3-125">RELATED LINKS</span></span>
