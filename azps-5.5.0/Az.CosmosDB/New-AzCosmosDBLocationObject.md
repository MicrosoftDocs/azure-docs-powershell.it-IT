---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdblocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBLocationObject.md
ms.openlocfilehash: 59fee5840ec279c7ed11b9b9d738561caf03ec66
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204634"
---
# <span data-ttu-id="067a7-101">New-AzCosmosDBLocationObject</span><span class="sxs-lookup"><span data-stu-id="067a7-101">New-AzCosmosDBLocationObject</span></span>

## <span data-ttu-id="067a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="067a7-102">SYNOPSIS</span></span>
<span data-ttu-id="067a7-103">Creare un nuovo oggetto posizioneDbDb(PSLocation).</span><span class="sxs-lookup"><span data-stu-id="067a7-103">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="067a7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="067a7-104">SYNTAX</span></span>

```
New-AzCosmosDBLocationObject -LocationName <String> [-FailoverPriority <Int32>] [-IsZoneRedundant <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="067a7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="067a7-105">DESCRIPTION</span></span>
<span data-ttu-id="067a7-106">Creare un nuovo oggetto posizioneDbDb(PSLocation).</span><span class="sxs-lookup"><span data-stu-id="067a7-106">Create a new CosmosDB Location Object(PSLocation).</span></span>

## <span data-ttu-id="067a7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="067a7-107">EXAMPLES</span></span>

### <span data-ttu-id="067a7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="067a7-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBLocationObject -LocationName {locationName} -FailoverPriority 2 -IsZoneRedundant 0

LocationName     FailoverPriority IsZoneRedundant
------------     ---------------- ---------------
{locationName}                 2           False
```

## <span data-ttu-id="067a7-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="067a7-109">PARAMETERS</span></span>

### <span data-ttu-id="067a7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="067a7-110">-DefaultProfile</span></span>
<span data-ttu-id="067a7-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="067a7-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="067a7-112">-FailoverPriority</span><span class="sxs-lookup"><span data-stu-id="067a7-112">-FailoverPriority</span></span>
<span data-ttu-id="067a7-113">Priorità di failover della posizione.</span><span class="sxs-lookup"><span data-stu-id="067a7-113">Failover priority of the location.</span></span>

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

### <span data-ttu-id="067a7-114">-IsZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="067a7-114">-IsZoneRedundant</span></span>
<span data-ttu-id="067a7-115">Booleano per indicare se l'area geografica è o meno un valore AvailabilityZone.</span><span class="sxs-lookup"><span data-stu-id="067a7-115">Boolean to indicate whether or not this region is an AvailabilityZone.</span></span>

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

### <span data-ttu-id="067a7-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="067a7-116">-LocationName</span></span>
<span data-ttu-id="067a7-117">Nome della posizione nella stringa.</span><span class="sxs-lookup"><span data-stu-id="067a7-117">Name of the Location in string.</span></span>

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

### <span data-ttu-id="067a7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="067a7-118">CommonParameters</span></span>
<span data-ttu-id="067a7-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="067a7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="067a7-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="067a7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="067a7-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="067a7-121">INPUTS</span></span>

### <span data-ttu-id="067a7-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="067a7-122">None</span></span>

## <span data-ttu-id="067a7-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="067a7-123">OUTPUTS</span></span>

### <span data-ttu-id="067a7-124">Microsoft.Azure.Commands.EnterpriseDb.Models.PSLocation</span><span class="sxs-lookup"><span data-stu-id="067a7-124">Microsoft.Azure.Commands.CosmosDB.Models.PSLocation</span></span>

## <span data-ttu-id="067a7-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="067a7-125">NOTES</span></span>

## <span data-ttu-id="067a7-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="067a7-126">RELATED LINKS</span></span>
