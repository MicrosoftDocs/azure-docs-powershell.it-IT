---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/get-azfunctionappavailablelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
ms.openlocfilehash: 987c4e351e024452231b5a5367ea7c2905d57863
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969086"
---
# <span data-ttu-id="e36a5-101">Get-AzFunctionAppAvailableLocation</span><span class="sxs-lookup"><span data-stu-id="e36a5-101">Get-AzFunctionAppAvailableLocation</span></span>

## <span data-ttu-id="e36a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e36a5-102">SYNOPSIS</span></span>
<span data-ttu-id="e36a5-103">Ottiene la posizione in cui è disponibile un'app per il sistema operativo e il tipo di piano specificato.</span><span class="sxs-lookup"><span data-stu-id="e36a5-103">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="e36a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e36a5-104">SYNTAX</span></span>

```
Get-AzFunctionAppAvailableLocation [[-SubscriptionId] <String[]>] [[-PlanType] <String>] [[-OSType] <String>]
 [[-DefaultProfile] <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e36a5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e36a5-105">DESCRIPTION</span></span>
<span data-ttu-id="e36a5-106">Ottiene la posizione in cui è disponibile un'app per le funzioni per il tipo di piano e di sistema specificato.</span><span class="sxs-lookup"><span data-stu-id="e36a5-106">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="e36a5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e36a5-107">EXAMPLES</span></span>

### <span data-ttu-id="e36a5-108">Esempio 1: Ottieni le località in cui Premium è disponibile per Windows.</span><span class="sxs-lookup"><span data-stu-id="e36a5-108">Example 1: Get the locations where Premium is available for Windows.</span></span> <span data-ttu-id="e36a5-109">Se non vengono specificati parametri, PlanType è impostato su "Premium" e OSType su "Windows".</span><span class="sxs-lookup"><span data-stu-id="e36a5-109">If no parameters are specified, PlanType is set to 'Premium' and OSType is set to 'Windows'.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
East Asia (Stage)
West India
South India
Canada Central
West US 2
UK West
UK South
East US 2 EUAP
Central US EUAP
Korea Central
France Central
Australia Central 2
Australia Central
Germany West Central
Norway East
```

<span data-ttu-id="e36a5-110">Questo comando consente di ottenere le posizioni in cui Premium è disponibile per Windows.</span><span class="sxs-lookup"><span data-stu-id="e36a5-110">This command gets the locations where Premium is available for Windows.</span></span>

### <span data-ttu-id="e36a5-111">Esempio 2: Ottieni le località in cui Premium è disponibile per Linux.</span><span class="sxs-lookup"><span data-stu-id="e36a5-111">Example 2: Get the locations where Premium is available for Linux.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation -PlanType Premium -OSType Linux

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
West India
Canada Central
West Central US
West US 2
UK West
UK South
Central US EUAP
Korea Central
France Central
Norway East
```

<span data-ttu-id="e36a5-112">Questo comando ottiene le posizioni in cui Premium è disponibile per Linux.</span><span class="sxs-lookup"><span data-stu-id="e36a5-112">This command gets the locations where Premium is available for Linux.</span></span>

### <span data-ttu-id="e36a5-113">Esempio 3: Ottenere le località in cui l'utilizzo è disponibile per Windows.</span><span class="sxs-lookup"><span data-stu-id="e36a5-113">Example 3: Get the locations where Consumption is available for Windows.</span></span>
```powershell
PS C:\> Get-AzFunctionAppAvailableLocation -PlanType Consumption -OSType Windows

Name
----
Central US
North Europe
West Europe
Southeast Asia
East Asia
West US
East US
Japan West
Japan East
East US 2
North Central US
South Central US
Brazil South
Australia East
Australia Southeast
East Asia (Stage)
Central India
West India
South India
Canada Central
Canada East
West Central US
West US 2
UK West
UK South
East US 2 EUAP
Central US EUAP
Korea Central
France Central
Australia Central 2
Australia Central
South Africa North
Switzerland North
Germany West Central
```

<span data-ttu-id="e36a5-114">Questo comando recupera le posizioni in cui Consumo è disponibile per Windows.</span><span class="sxs-lookup"><span data-stu-id="e36a5-114">This command gets the locations where Consumption is available for Windows.</span></span>

## <span data-ttu-id="e36a5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e36a5-115">PARAMETERS</span></span>

### <span data-ttu-id="e36a5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e36a5-116">-DefaultProfile</span></span>
<span data-ttu-id="e36a5-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e36a5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36a5-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="e36a5-118">-OSType</span></span>
<span data-ttu-id="e36a5-119">Tipo di sistema operativo per il piano di servizio.</span><span class="sxs-lookup"><span data-stu-id="e36a5-119">The OS type for the service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36a5-120">-PlanType</span><span class="sxs-lookup"><span data-stu-id="e36a5-120">-PlanType</span></span>
<span data-ttu-id="e36a5-121">Tipo di piano.</span><span class="sxs-lookup"><span data-stu-id="e36a5-121">The plan type.</span></span>
<span data-ttu-id="e36a5-122">Input validi: Consumo o Premium</span><span class="sxs-lookup"><span data-stu-id="e36a5-122">Valid inputs: Consumption or Premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36a5-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e36a5-123">-SubscriptionId</span></span>
<span data-ttu-id="e36a5-124">ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e36a5-124">The Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e36a5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e36a5-125">CommonParameters</span></span>
<span data-ttu-id="e36a5-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e36a5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e36a5-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e36a5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e36a5-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="e36a5-128">INPUTS</span></span>

## <span data-ttu-id="e36a5-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e36a5-129">OUTPUTS</span></span>

### <span data-ttu-id="e36a5-130">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IGeoRegion</span><span class="sxs-lookup"><span data-stu-id="e36a5-130">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IGeoRegion</span></span>

## <span data-ttu-id="e36a5-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="e36a5-131">NOTES</span></span>

<span data-ttu-id="e36a5-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e36a5-132">ALIASES</span></span>

## <span data-ttu-id="e36a5-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e36a5-133">RELATED LINKS</span></span>

