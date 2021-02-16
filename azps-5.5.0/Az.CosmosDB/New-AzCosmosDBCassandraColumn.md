---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandracolumn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
ms.openlocfilehash: 31563c11a1df418d0f53c1eeb80e8bc02691188c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198983"
---
# <span data-ttu-id="40b61-101">New-AzCosmosDBCassandraColumn</span><span class="sxs-lookup"><span data-stu-id="40b61-101">New-AzCosmosDBCassandraColumn</span></span>

## <span data-ttu-id="40b61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40b61-102">SYNOPSIS</span></span>
<span data-ttu-id="40b61-103">Crea una nuova colonna CassandraDB.</span><span class="sxs-lookup"><span data-stu-id="40b61-103">Creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="40b61-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="40b61-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraColumn -Name <String> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40b61-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="40b61-105">DESCRIPTION</span></span>
<span data-ttu-id="40b61-106">La **nuova colonna New-AzCosmosDBCassandraColumn** crea una nuova colonnaDb Cassandra.</span><span class="sxs-lookup"><span data-stu-id="40b61-106">The **New-AzCosmosDBCassandraColumn** creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="40b61-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="40b61-107">EXAMPLES</span></span>

### <span data-ttu-id="40b61-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="40b61-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraColumn -Name "name" -Type int

Name Type
---- ----
name int
```

## <span data-ttu-id="40b61-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40b61-109">PARAMETERS</span></span>

### <span data-ttu-id="40b61-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40b61-110">-DefaultProfile</span></span>
<span data-ttu-id="40b61-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="40b61-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40b61-112">-Name</span><span class="sxs-lookup"><span data-stu-id="40b61-112">-Name</span></span>
<span data-ttu-id="40b61-113">Nome della colonna Cassandra.</span><span class="sxs-lookup"><span data-stu-id="40b61-113">Name of Cassandra Column.</span></span>

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

### <span data-ttu-id="40b61-114">-Type</span><span class="sxs-lookup"><span data-stu-id="40b61-114">-Type</span></span>
<span data-ttu-id="40b61-115">Tipo di colonna Cassandra.</span><span class="sxs-lookup"><span data-stu-id="40b61-115">Type of Cassandra Column.</span></span>

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

### <span data-ttu-id="40b61-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40b61-116">CommonParameters</span></span>
<span data-ttu-id="40b61-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40b61-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40b61-118">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="40b61-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40b61-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="40b61-119">INPUTS</span></span>

### <span data-ttu-id="40b61-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="40b61-120">None</span></span>

## <span data-ttu-id="40b61-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40b61-121">OUTPUTS</span></span>

### <span data-ttu-id="40b61-122">Microsoft.Azure.Commands.EnterpriseDb.Models.PSColumn</span><span class="sxs-lookup"><span data-stu-id="40b61-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span></span>

## <span data-ttu-id="40b61-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="40b61-123">NOTES</span></span>

## <span data-ttu-id="40b61-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="40b61-124">RELATED LINKS</span></span>
