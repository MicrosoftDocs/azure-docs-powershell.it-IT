---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
ms.openlocfilehash: e3c96cfd4051a186e0584d810088bc06a57ad862
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477412"
---
# <span data-ttu-id="40efd-101">New-AzCosmosDBSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="40efd-101">New-AzCosmosDBSqlUniqueKey</span></span>

## <span data-ttu-id="40efd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="40efd-102">SYNOPSIS</span></span>
<span data-ttu-id="40efd-103">Crea un nuovo oggetto CosmosDB SQL UniqueKey.</span><span class="sxs-lookup"><span data-stu-id="40efd-103">Creates a new CosmosDB Sql UniqueKey object.</span></span>

## <span data-ttu-id="40efd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="40efd-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40efd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40efd-105">DESCRIPTION</span></span>
<span data-ttu-id="40efd-106">Il cmdlet **New-AzCosmosDBSqlUniqueKey** crea un nuovo oggetto di tipo PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="40efd-106">The **New-AzCosmosDBSqlUniqueKey** cmdlet creates a new object of type PSUniqueKey.</span></span>

## <span data-ttu-id="40efd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="40efd-107">EXAMPLES</span></span>

### <span data-ttu-id="40efd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="40efd-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUniqueKey -Path {path}

Path
----
{path}
```

## <span data-ttu-id="40efd-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="40efd-109">PARAMETERS</span></span>

### <span data-ttu-id="40efd-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40efd-110">-DefaultProfile</span></span>
<span data-ttu-id="40efd-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="40efd-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40efd-112">-Path</span><span class="sxs-lookup"><span data-stu-id="40efd-112">-Path</span></span>
<span data-ttu-id="40efd-113">Matrice di stringa di valori di percorso</span><span class="sxs-lookup"><span data-stu-id="40efd-113">Array of string of path values</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40efd-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40efd-114">CommonParameters</span></span>
<span data-ttu-id="40efd-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40efd-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40efd-116">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40efd-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40efd-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="40efd-117">INPUTS</span></span>

### <span data-ttu-id="40efd-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="40efd-118">None</span></span>

## <span data-ttu-id="40efd-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40efd-119">OUTPUTS</span></span>

### <span data-ttu-id="40efd-120">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="40efd-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span></span>

## <span data-ttu-id="40efd-121">Note</span><span class="sxs-lookup"><span data-stu-id="40efd-121">NOTES</span></span>

## <span data-ttu-id="40efd-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="40efd-122">RELATED LINKS</span></span>
