---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdblocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
ms.openlocfilehash: 59fee5840ec279c7ed11b9b9d738561caf03ec66
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031839"
---
# <span data-ttu-id="b0bba-101">New-AzCosmosDBLocationObject</span><span class="sxs-lookup"><span data-stu-id="b0bba-101">New-AzCosmosDBLocationObject</span></span>

## <span data-ttu-id="b0bba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0bba-102">SYNOPSIS</span></span>
<span data-ttu-id="b0bba-103">Crea un nuovo oggetto location di CosmosDB (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="b0bba-103">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="b0bba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0bba-104">SYNTAX</span></span>

```
New-AzCosmosDBLocationObject -LocationName <String> [-FailoverPriority <Int32>] [-IsZoneRedundant <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0bba-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0bba-105">DESCRIPTION</span></span>
<span data-ttu-id="b0bba-106">Crea un nuovo oggetto location di CosmosDB (PSLocation).</span><span class="sxs-lookup"><span data-stu-id="b0bba-106">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="b0bba-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0bba-107">EXAMPLES</span></span>

### <span data-ttu-id="b0bba-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b0bba-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBLocationObject -LocationName {locationName} -FailoverPriority 2 -IsZoneRedundant 0

LocationName     FailoverPriority IsZoneRedundant
------------     ---------------- ---------------
{locationName}                 2           False
```

## <span data-ttu-id="b0bba-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0bba-109">PARAMETERS</span></span>

### <span data-ttu-id="b0bba-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0bba-110">-DefaultProfile</span></span>
<span data-ttu-id="b0bba-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0bba-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0bba-112">-FailoverPriority</span><span class="sxs-lookup"><span data-stu-id="b0bba-112">-FailoverPriority</span></span>
<span data-ttu-id="b0bba-113">Priorità di failover della posizione.</span><span class="sxs-lookup"><span data-stu-id="b0bba-113">Failover priority of the location.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0bba-114">-IsZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="b0bba-114">-IsZoneRedundant</span></span>
<span data-ttu-id="b0bba-115">Booleano per indicare se l'area geografica o meno è un AvailabilityZone.</span><span class="sxs-lookup"><span data-stu-id="b0bba-115">Boolean to indicate whether or not this region is an AvailabilityZone.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0bba-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="b0bba-116">-LocationName</span></span>
<span data-ttu-id="b0bba-117">Nome della posizione in String.</span><span class="sxs-lookup"><span data-stu-id="b0bba-117">Name of the Location in string.</span></span>

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

### <span data-ttu-id="b0bba-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0bba-118">CommonParameters</span></span>
<span data-ttu-id="b0bba-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0bba-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0bba-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0bba-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0bba-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0bba-121">INPUTS</span></span>

### <span data-ttu-id="b0bba-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b0bba-122">None</span></span>

## <span data-ttu-id="b0bba-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0bba-123">OUTPUTS</span></span>

### <span data-ttu-id="b0bba-124">Microsoft. Azure. Commands. CosmosDB. Models. PSLocation</span><span class="sxs-lookup"><span data-stu-id="b0bba-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span></span>

## <span data-ttu-id="b0bba-125">Note</span><span class="sxs-lookup"><span data-stu-id="b0bba-125">NOTES</span></span>

## <span data-ttu-id="b0bba-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0bba-126">RELATED LINKS</span></span>
