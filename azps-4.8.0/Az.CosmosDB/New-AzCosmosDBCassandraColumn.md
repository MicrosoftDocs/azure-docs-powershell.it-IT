---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandracolumn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
ms.openlocfilehash: 31563c11a1df418d0f53c1eeb80e8bc02691188c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033216"
---
# <span data-ttu-id="24116-101">New-AzCosmosDBCassandraColumn</span><span class="sxs-lookup"><span data-stu-id="24116-101">New-AzCosmosDBCassandraColumn</span></span>

## <span data-ttu-id="24116-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24116-102">SYNOPSIS</span></span>
<span data-ttu-id="24116-103">Crea una nuova colonna di CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="24116-103">Creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="24116-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24116-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraColumn -Name <String> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24116-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24116-105">DESCRIPTION</span></span>
<span data-ttu-id="24116-106">Il **nuovo AzCosmosDBCassandraColumn** crea una nuova colonna di CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="24116-106">The **New-AzCosmosDBCassandraColumn** creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="24116-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24116-107">EXAMPLES</span></span>

### <span data-ttu-id="24116-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="24116-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraColumn -Name "name" -Type int

Name Type
---- ----
name int
```

## <span data-ttu-id="24116-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24116-109">PARAMETERS</span></span>

### <span data-ttu-id="24116-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24116-110">-DefaultProfile</span></span>
<span data-ttu-id="24116-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24116-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24116-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="24116-112">-Name</span></span>
<span data-ttu-id="24116-113">Nome della colonna Cassandra.</span><span class="sxs-lookup"><span data-stu-id="24116-113">Name of Cassandra Column.</span></span>

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

### <span data-ttu-id="24116-114">-Digitare</span><span class="sxs-lookup"><span data-stu-id="24116-114">-Type</span></span>
<span data-ttu-id="24116-115">Tipo di colonna Cassandra.</span><span class="sxs-lookup"><span data-stu-id="24116-115">Type of Cassandra Column.</span></span>

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

### <span data-ttu-id="24116-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24116-116">CommonParameters</span></span>
<span data-ttu-id="24116-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24116-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24116-118">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24116-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24116-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24116-119">INPUTS</span></span>

### <span data-ttu-id="24116-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="24116-120">None</span></span>

## <span data-ttu-id="24116-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24116-121">OUTPUTS</span></span>

### <span data-ttu-id="24116-122">Microsoft. Azure. Commands. CosmosDB. Models. PSColumn</span><span class="sxs-lookup"><span data-stu-id="24116-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span></span>

## <span data-ttu-id="24116-123">Note</span><span class="sxs-lookup"><span data-stu-id="24116-123">NOTES</span></span>

## <span data-ttu-id="24116-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24116-124">RELATED LINKS</span></span>
