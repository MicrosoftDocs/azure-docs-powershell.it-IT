---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlflexibleserverlocationbasedcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerLocationBasedCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerLocationBasedCapability.md
ms.openlocfilehash: 063abe34cbbd6c0f10e275e5b4b63f3c163b87e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179151"
---
# <span data-ttu-id="a6f91-101">Get-AzPostgreSqlFlexibleServerLocationBasedCapability</span><span class="sxs-lookup"><span data-stu-id="a6f91-101">Get-AzPostgreSqlFlexibleServerLocationBasedCapability</span></span>

## <span data-ttu-id="a6f91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6f91-102">SYNOPSIS</span></span>
<span data-ttu-id="a6f91-103">Ottenere le informazioni disponibili sullo SKU per la posizione</span><span class="sxs-lookup"><span data-stu-id="a6f91-103">Get the available SKU information for the location</span></span>

## <span data-ttu-id="a6f91-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6f91-104">SYNTAX</span></span>

```
Get-AzPostgreSqlFlexibleServerLocationBasedCapability -Location <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a6f91-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a6f91-105">DESCRIPTION</span></span>
<span data-ttu-id="a6f91-106">Ottenere le informazioni disponibili sullo SKU per la posizione</span><span class="sxs-lookup"><span data-stu-id="a6f91-106">Get the available SKU information for the location</span></span>

## <span data-ttu-id="a6f91-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6f91-107">EXAMPLES</span></span>

### <span data-ttu-id="a6f91-108">Esempio 1: Ottenere funzionalità relative alla posizione in base al nome della posizione</span><span class="sxs-lookup"><span data-stu-id="a6f91-108">Example 1: Get location capabilities by location name</span></span>
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

<span data-ttu-id="a6f91-109">Questo cmdlet mostra le informazioni di base sulle SKU della posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="a6f91-109">This cmdlet shows basic sku information of the provided location.</span></span>

## <span data-ttu-id="a6f91-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6f91-110">PARAMETERS</span></span>

### <span data-ttu-id="a6f91-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6f91-111">-DefaultProfile</span></span>
<span data-ttu-id="a6f91-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6f91-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6f91-113">-Location</span><span class="sxs-lookup"><span data-stu-id="a6f91-113">-Location</span></span>
<span data-ttu-id="a6f91-114">Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="a6f91-114">The name of the location.</span></span>

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

### <span data-ttu-id="a6f91-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a6f91-115">-SubscriptionId</span></span>
<span data-ttu-id="a6f91-116">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a6f91-116">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a6f91-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6f91-117">CommonParameters</span></span>
<span data-ttu-id="a6f91-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6f91-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6f91-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a6f91-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6f91-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="a6f91-120">INPUTS</span></span>

## <span data-ttu-id="a6f91-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6f91-121">OUTPUTS</span></span>

### <span data-ttu-id="a6f91-122">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.ICapabilityProperties</span><span class="sxs-lookup"><span data-stu-id="a6f91-122">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.ICapabilityProperties</span></span>

## <span data-ttu-id="a6f91-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="a6f91-123">NOTES</span></span>

<span data-ttu-id="a6f91-124">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a6f91-124">ALIASES</span></span>

## <span data-ttu-id="a6f91-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6f91-125">RELATED LINKS</span></span>

