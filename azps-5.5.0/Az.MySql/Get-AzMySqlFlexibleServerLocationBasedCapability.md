---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverlocationbasedcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerLocationBasedCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerLocationBasedCapability.md
ms.openlocfilehash: 20c142df2a3df0ea6448c2bcb58ad47169d9e483
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180094"
---
# <span data-ttu-id="a3ded-101">Get-AzMySqlFlexibleServerLocationBasedCapability</span><span class="sxs-lookup"><span data-stu-id="a3ded-101">Get-AzMySqlFlexibleServerLocationBasedCapability</span></span>

## <span data-ttu-id="a3ded-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3ded-102">SYNOPSIS</span></span>
<span data-ttu-id="a3ded-103">Ottenere le informazioni disponibili sullo SKU per la posizione</span><span class="sxs-lookup"><span data-stu-id="a3ded-103">Get the available SKU information for the location</span></span>

## <span data-ttu-id="a3ded-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3ded-104">SYNTAX</span></span>

```
Get-AzMySqlFlexibleServerLocationBasedCapability -Location <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a3ded-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a3ded-105">DESCRIPTION</span></span>
<span data-ttu-id="a3ded-106">Ottenere le informazioni disponibili sullo SKU per la posizione</span><span class="sxs-lookup"><span data-stu-id="a3ded-106">Get the available SKU information for the location</span></span>

## <span data-ttu-id="a3ded-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3ded-107">EXAMPLES</span></span>

### <span data-ttu-id="a3ded-108">Esempio 1: Ottenere funzionalità relative alla posizione in base al nome della posizione</span><span class="sxs-lookup"><span data-stu-id="a3ded-108">Example 1: Get location capabilities by location name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerLocationBasedCapability -Location westus2
"Please refer to https://aka.ms/mysql-pricing for pricing details"

SKU               Tier            Memory vCore
---               ----            ------ -----
Standard_B1s      Burstable         1024     1
Standard_B1ms     Burstable         2048     1
Standard_B2s      Burstable         2048     2
Standard_D2ds_v4  GeneralPurpose    4096     2
Standard_D4ds_v4  GeneralPurpose    4096     4
Standard_D8ds_v4  GeneralPurpose    4096     8
Standard_D16ds_v4 GeneralPurpose    4096    16
Standard_D32ds_v4 GeneralPurpose    4096    32
Standard_D48ds_v4 GeneralPurpose    4096    48
Standard_D64ds_v4 GeneralPurpose    4096    64
Standard_E2ds_v4  MemoryOptimized   8192     2
Standard_E4ds_v4  MemoryOptimized   8192     4
Standard_E8ds_v4  MemoryOptimized   8192     8
Standard_E16ds_v4 MemoryOptimized   8192    16
Standard_E32ds_v4 MemoryOptimized   8192    32
Standard_E48ds_v4 MemoryOptimized   8192    48
Standard_E64ds_v4 MemoryOptimized   8192    64

```

<span data-ttu-id="a3ded-109">Questo cmdlet mostra le informazioni di base sulle SKU della posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="a3ded-109">This cmdlet shows basic sku information of the provided location.</span></span>

## <span data-ttu-id="a3ded-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3ded-110">PARAMETERS</span></span>

### <span data-ttu-id="a3ded-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3ded-111">-DefaultProfile</span></span>
<span data-ttu-id="a3ded-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a3ded-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3ded-113">-Location</span><span class="sxs-lookup"><span data-stu-id="a3ded-113">-Location</span></span>
<span data-ttu-id="a3ded-114">Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="a3ded-114">The name of the location.</span></span>

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

### <span data-ttu-id="a3ded-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a3ded-115">-SubscriptionId</span></span>
<span data-ttu-id="a3ded-116">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a3ded-116">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a3ded-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3ded-117">CommonParameters</span></span>
<span data-ttu-id="a3ded-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3ded-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3ded-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a3ded-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3ded-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="a3ded-120">INPUTS</span></span>

## <span data-ttu-id="a3ded-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3ded-121">OUTPUTS</span></span>

### <span data-ttu-id="a3ded-122">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.ICapabilityProperties</span><span class="sxs-lookup"><span data-stu-id="a3ded-122">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.ICapabilityProperties</span></span>

## <span data-ttu-id="a3ded-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="a3ded-123">NOTES</span></span>

<span data-ttu-id="a3ded-124">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a3ded-124">ALIASES</span></span>

## <span data-ttu-id="a3ded-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3ded-125">RELATED LINKS</span></span>

