---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappavailablelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppAvailableLocation.md
ms.openlocfilehash: 3ab2ab4778b7fdb12334db416c953a7c373c63b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193388"
---
# <span data-ttu-id="debca-101">Get-AzFunctionAppAvailableLocation</span><span class="sxs-lookup"><span data-stu-id="debca-101">Get-AzFunctionAppAvailableLocation</span></span>

## <span data-ttu-id="debca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="debca-102">SYNOPSIS</span></span>
<span data-ttu-id="debca-103">Ottiene la posizione in cui è disponibile un'app di funzione per il sistema operativo e il tipo di piano specificati.</span><span class="sxs-lookup"><span data-stu-id="debca-103">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="debca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="debca-104">SYNTAX</span></span>

```
Get-AzFunctionAppAvailableLocation [[-SubscriptionId] <String[]>] [[-PlanType] <String>] [[-OSType] <String>]
 [[-DefaultProfile] <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="debca-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="debca-105">DESCRIPTION</span></span>
<span data-ttu-id="debca-106">Ottiene la posizione in cui è disponibile un'app di funzione per il sistema operativo e il tipo di piano specificati.</span><span class="sxs-lookup"><span data-stu-id="debca-106">Gets the location where a function app for the given os and plan type is available.</span></span>

## <span data-ttu-id="debca-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="debca-107">EXAMPLES</span></span>

### <span data-ttu-id="debca-108">Esempio 1: ottenere le posizioni in cui Premium è disponibile per Windows.</span><span class="sxs-lookup"><span data-stu-id="debca-108">Example 1: Get the locations where Premium is available for Windows.</span></span> <span data-ttu-id="debca-109">Se non sono specificati parametri, PlanType è impostato su "Premium" e OSType è impostato su "Windows".</span><span class="sxs-lookup"><span data-stu-id="debca-109">If no parameters are specified, PlanType is set to 'Premium' and OSType is set to 'Windows'.</span></span>
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

<span data-ttu-id="debca-110">Questo comando consente di ottenere le posizioni in cui Premium è disponibile per Windows.</span><span class="sxs-lookup"><span data-stu-id="debca-110">This command gets the locations where Premium is available for Windows.</span></span>

### <span data-ttu-id="debca-111">Esempio 2: ottenere le posizioni in cui Premium è disponibile per Linux.</span><span class="sxs-lookup"><span data-stu-id="debca-111">Example 2: Get the locations where Premium is available for Linux.</span></span>
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

<span data-ttu-id="debca-112">Questo comando consente di ottenere le posizioni in cui Premium è disponibile per Linux.</span><span class="sxs-lookup"><span data-stu-id="debca-112">This command gets the locations where Premium is available for Linux.</span></span>

### <span data-ttu-id="debca-113">Esempio 3: ottenere le posizioni in cui il consumo è disponibile per Windows.</span><span class="sxs-lookup"><span data-stu-id="debca-113">Example 3: Get the locations where Consumption is available for Windows.</span></span>
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

<span data-ttu-id="debca-114">Questo comando consente di ottenere le posizioni in cui il consumo è disponibile per Windows.</span><span class="sxs-lookup"><span data-stu-id="debca-114">This command gets the locations where Consumption is available for Windows.</span></span>

## <span data-ttu-id="debca-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="debca-115">PARAMETERS</span></span>

### <span data-ttu-id="debca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="debca-116">-DefaultProfile</span></span>
<span data-ttu-id="debca-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="debca-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="debca-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="debca-118">-OSType</span></span>
<span data-ttu-id="debca-119">Tipo di sistema operativo per il piano di servizio.</span><span class="sxs-lookup"><span data-stu-id="debca-119">The OS type for the service plan.</span></span>

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

### <span data-ttu-id="debca-120">-PlanType</span><span class="sxs-lookup"><span data-stu-id="debca-120">-PlanType</span></span>
<span data-ttu-id="debca-121">Tipo di piano.</span><span class="sxs-lookup"><span data-stu-id="debca-121">The plan type.</span></span>
<span data-ttu-id="debca-122">Input validi: consumi o Premium</span><span class="sxs-lookup"><span data-stu-id="debca-122">Valid inputs: Consumption or Premium</span></span>

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

### <span data-ttu-id="debca-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="debca-123">-SubscriptionId</span></span>
<span data-ttu-id="debca-124">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="debca-124">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="debca-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="debca-125">CommonParameters</span></span>
<span data-ttu-id="debca-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="debca-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="debca-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="debca-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="debca-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="debca-128">INPUTS</span></span>

## <span data-ttu-id="debca-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="debca-129">OUTPUTS</span></span>

### <span data-ttu-id="debca-130">Microsoft. Azure. PowerShell. Cmdlets. Functions. Models. Api20190801. IGeoRegion</span><span class="sxs-lookup"><span data-stu-id="debca-130">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IGeoRegion</span></span>

## <span data-ttu-id="debca-131">Note</span><span class="sxs-lookup"><span data-stu-id="debca-131">NOTES</span></span>

<span data-ttu-id="debca-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="debca-132">ALIASES</span></span>

## <span data-ttu-id="debca-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="debca-133">RELATED LINKS</span></span>

