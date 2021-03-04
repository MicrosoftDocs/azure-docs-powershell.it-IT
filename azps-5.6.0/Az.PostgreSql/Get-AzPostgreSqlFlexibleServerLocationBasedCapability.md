---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlflexibleserverlocationbasedcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerLocationBasedCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerLocationBasedCapability.md
ms.openlocfilehash: efe45da6cd5426fda3b301efd4daf2ef532e4c02
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953741"
---
# <span data-ttu-id="73cc2-101">Get-AzPostgreSqlFlexibleServerLocationBasedCapability</span><span class="sxs-lookup"><span data-stu-id="73cc2-101">Get-AzPostgreSqlFlexibleServerLocationBasedCapability</span></span>

## <span data-ttu-id="73cc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73cc2-102">SYNOPSIS</span></span>
<span data-ttu-id="73cc2-103">Ottenere le informazioni disponibili sullo SKU per la posizione</span><span class="sxs-lookup"><span data-stu-id="73cc2-103">Get the available SKU information for the location</span></span>

## <span data-ttu-id="73cc2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="73cc2-104">SYNTAX</span></span>

```
Get-AzPostgreSqlFlexibleServerLocationBasedCapability -Location <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="73cc2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="73cc2-105">DESCRIPTION</span></span>
<span data-ttu-id="73cc2-106">Ottenere le informazioni disponibili sullo SKU per la posizione</span><span class="sxs-lookup"><span data-stu-id="73cc2-106">Get the available SKU information for the location</span></span>

## <span data-ttu-id="73cc2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="73cc2-107">EXAMPLES</span></span>

### <span data-ttu-id="73cc2-108">Esempio 1: Ottenere funzionalità relative alla posizione in base al nome della posizione</span><span class="sxs-lookup"><span data-stu-id="73cc2-108">Example 1: Get location capabilities by location name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerLocationBasedCapability -Location eastus

SKU              Tier            Memory vCore
---              ----            ------ -----
Standard_B1ms    Burstable         2048     1
Standard_B2s     Burstable         2048     2
Standard_D2s_v3  GeneralPurpose    4096     2
Standard_D4s_v3  GeneralPurpose    4096     4
Standard_D8s_v3  GeneralPurpose    4096     8
Standard_D16s_v3 GeneralPurpose    4096    16
Standard_D32s_v3 GeneralPurpose    4096    32
Standard_D48s_v3 GeneralPurpose    4096    48
Standard_D64s_v3 GeneralPurpose    4096    64
Standard_E2s_v3  MemoryOptimized   8192     2
Standard_E4s_v3  MemoryOptimized   8192     4
Standard_E8s_v3  MemoryOptimized   8192     8
Standard_E16s_v3 MemoryOptimized   8192    16
Standard_E32s_v3 MemoryOptimized   8192    32
Standard_E48s_v3 MemoryOptimized   8192    48
Standard_E64s_v3 MemoryOptimized   6912    64
```

<span data-ttu-id="73cc2-109">Questo cmdlet mostra le informazioni di base sulle SKU della posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="73cc2-109">This cmdlet shows basic sku information of the provided location.</span></span>

## <span data-ttu-id="73cc2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73cc2-110">PARAMETERS</span></span>

### <span data-ttu-id="73cc2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73cc2-111">-DefaultProfile</span></span>
<span data-ttu-id="73cc2-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="73cc2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73cc2-113">-Location</span><span class="sxs-lookup"><span data-stu-id="73cc2-113">-Location</span></span>
<span data-ttu-id="73cc2-114">Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="73cc2-114">The name of the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73cc2-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="73cc2-115">-SubscriptionId</span></span>
<span data-ttu-id="73cc2-116">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="73cc2-116">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73cc2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73cc2-117">CommonParameters</span></span>
<span data-ttu-id="73cc2-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73cc2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73cc2-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="73cc2-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73cc2-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="73cc2-120">INPUTS</span></span>

## <span data-ttu-id="73cc2-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="73cc2-121">OUTPUTS</span></span>

### <span data-ttu-id="73cc2-122">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.ICapabilityProperties</span><span class="sxs-lookup"><span data-stu-id="73cc2-122">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.ICapabilityProperties</span></span>

## <span data-ttu-id="73cc2-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="73cc2-123">NOTES</span></span>

<span data-ttu-id="73cc2-124">ALIAS</span><span class="sxs-lookup"><span data-stu-id="73cc2-124">ALIASES</span></span>

## <span data-ttu-id="73cc2-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="73cc2-125">RELATED LINKS</span></span>

