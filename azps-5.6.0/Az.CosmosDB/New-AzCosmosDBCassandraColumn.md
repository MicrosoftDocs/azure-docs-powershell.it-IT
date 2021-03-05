---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbcassandracolumn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
ms.openlocfilehash: 634a6a8e1e6b921703603ee7f2bfd345aa64608c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010766"
---
# <span data-ttu-id="faf37-101">New-AzCosmosDBCassandraColumn</span><span class="sxs-lookup"><span data-stu-id="faf37-101">New-AzCosmosDBCassandraColumn</span></span>

## <span data-ttu-id="faf37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faf37-102">SYNOPSIS</span></span>
<span data-ttu-id="faf37-103">Crea una nuova colonna CassandraDB.</span><span class="sxs-lookup"><span data-stu-id="faf37-103">Creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="faf37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="faf37-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraColumn -Name <String> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="faf37-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="faf37-105">DESCRIPTION</span></span>
<span data-ttu-id="faf37-106">La **colonna New-AzCosmosDBCassandraColumn** crea una nuova colonnaDb Cassandra.</span><span class="sxs-lookup"><span data-stu-id="faf37-106">The **New-AzCosmosDBCassandraColumn** creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="faf37-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="faf37-107">EXAMPLES</span></span>

### <span data-ttu-id="faf37-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="faf37-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraColumn -Name "name" -Type int

Name Type
---- ----
name int
```

## <span data-ttu-id="faf37-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="faf37-109">PARAMETERS</span></span>

### <span data-ttu-id="faf37-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faf37-110">-DefaultProfile</span></span>
<span data-ttu-id="faf37-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="faf37-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="faf37-112">-Name</span><span class="sxs-lookup"><span data-stu-id="faf37-112">-Name</span></span>
<span data-ttu-id="faf37-113">Nome della colonna Cassandra.</span><span class="sxs-lookup"><span data-stu-id="faf37-113">Name of Cassandra Column.</span></span>

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

### <span data-ttu-id="faf37-114">-Type</span><span class="sxs-lookup"><span data-stu-id="faf37-114">-Type</span></span>
<span data-ttu-id="faf37-115">Tipo di Colonna Cassandra.</span><span class="sxs-lookup"><span data-stu-id="faf37-115">Type of Cassandra Column.</span></span>

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

### <span data-ttu-id="faf37-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faf37-116">CommonParameters</span></span>
<span data-ttu-id="faf37-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faf37-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faf37-118">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="faf37-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faf37-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="faf37-119">INPUTS</span></span>

### <span data-ttu-id="faf37-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="faf37-120">None</span></span>

## <span data-ttu-id="faf37-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="faf37-121">OUTPUTS</span></span>

### <span data-ttu-id="faf37-122">Microsoft.Azure.Commands.EnterpriseDb.Models.PSColumn</span><span class="sxs-lookup"><span data-stu-id="faf37-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span></span>

## <span data-ttu-id="faf37-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="faf37-123">NOTES</span></span>

## <span data-ttu-id="faf37-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="faf37-124">RELATED LINKS</span></span>
