---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: e9195a60b06f206a5b3133834f19cfdab68db31b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209506"
---
# <span data-ttu-id="bc626-101">New-AzFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="bc626-101">New-AzFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="bc626-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc626-102">SYNOPSIS</span></span>
<span data-ttu-id="bc626-103">Creare un oggetto PSLoadBalancingSetting per la creazione di Front Door</span><span class="sxs-lookup"><span data-stu-id="bc626-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="bc626-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc626-104">SYNTAX</span></span>

```
New-AzFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc626-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bc626-105">DESCRIPTION</span></span>
<span data-ttu-id="bc626-106">Creare un oggetto PSLoadBalancingSetting per la creazione di Front Door</span><span class="sxs-lookup"><span data-stu-id="bc626-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="bc626-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc626-107">EXAMPLES</span></span>

### <span data-ttu-id="bc626-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bc626-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorLoadBalancingSettingObject -Name "loadbalancingsetting1"


SampleSize                    : 4
AdditionalLatencyMilliseconds : 0
SuccessfulSamplesRequired     : 2
ResourceState                 :
Id                            :
Name                          : loadbalancingsetting1
Type                          :
```

<span data-ttu-id="bc626-109">Creare un oggetto PSLoadBalancingSetting per la creazione di Front Door</span><span class="sxs-lookup"><span data-stu-id="bc626-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="bc626-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc626-110">PARAMETERS</span></span>

### <span data-ttu-id="bc626-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="bc626-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="bc626-112">La latenza aggiuntiva in millisecondi per il ricadimento dei valori nel bucket di latenza più basso.</span><span class="sxs-lookup"><span data-stu-id="bc626-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="bc626-113">Il valore predefinito è 0</span><span class="sxs-lookup"><span data-stu-id="bc626-113">Default value is 0</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc626-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc626-114">-DefaultProfile</span></span>
<span data-ttu-id="bc626-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bc626-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc626-116">-Name</span><span class="sxs-lookup"><span data-stu-id="bc626-116">-Name</span></span>
<span data-ttu-id="bc626-117">health health setting name.</span><span class="sxs-lookup"><span data-stu-id="bc626-117">health probe setting name.</span></span>

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

### <span data-ttu-id="bc626-118">-SampleSize</span><span class="sxs-lookup"><span data-stu-id="bc626-118">-SampleSize</span></span>
<span data-ttu-id="bc626-119">Il numero di esempi da considerare per le decisioni di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="bc626-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="bc626-120">Il valore predefinito è 4</span><span class="sxs-lookup"><span data-stu-id="bc626-120">Default value is 4</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc626-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="bc626-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="bc626-122">Il numero di campioni che devono avere esito positivo nel periodo campione è 2</span><span class="sxs-lookup"><span data-stu-id="bc626-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc626-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc626-123">CommonParameters</span></span>
<span data-ttu-id="bc626-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc626-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc626-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bc626-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc626-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="bc626-126">INPUTS</span></span>

### <span data-ttu-id="bc626-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bc626-127">None</span></span>

## <span data-ttu-id="bc626-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc626-128">OUTPUTS</span></span>

### <span data-ttu-id="bc626-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="bc626-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="bc626-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="bc626-130">NOTES</span></span>

## <span data-ttu-id="bc626-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc626-131">RELATED LINKS</span></span>

<span data-ttu-id="bc626-132">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="bc626-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
