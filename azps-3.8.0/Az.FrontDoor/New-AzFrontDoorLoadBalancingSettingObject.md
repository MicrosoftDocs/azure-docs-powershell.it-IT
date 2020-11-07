---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: e9195a60b06f206a5b3133834f19cfdab68db31b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864433"
---
# <span data-ttu-id="6a5bf-101">New-AzFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="6a5bf-101">New-AzFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="6a5bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a5bf-102">SYNOPSIS</span></span>
<span data-ttu-id="6a5bf-103">Creare un oggetto PSLoadBalancingSetting per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="6a5bf-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="6a5bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a5bf-104">SYNTAX</span></span>

```
New-AzFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a5bf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a5bf-105">DESCRIPTION</span></span>
<span data-ttu-id="6a5bf-106">Creare un oggetto PSLoadBalancingSetting per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="6a5bf-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="6a5bf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a5bf-107">EXAMPLES</span></span>

### <span data-ttu-id="6a5bf-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6a5bf-108">Example 1</span></span>
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

<span data-ttu-id="6a5bf-109">Creare un oggetto PSLoadBalancingSetting per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="6a5bf-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="6a5bf-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a5bf-110">PARAMETERS</span></span>

### <span data-ttu-id="6a5bf-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="6a5bf-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="6a5bf-112">Latenza aggiuntiva in millisecondi per le sonde che rientrano nel bucket di latenza più bassa.</span><span class="sxs-lookup"><span data-stu-id="6a5bf-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="6a5bf-113">Il valore predefinito è 0</span><span class="sxs-lookup"><span data-stu-id="6a5bf-113">Default value is 0</span></span>

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

### <span data-ttu-id="6a5bf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a5bf-114">-DefaultProfile</span></span>
<span data-ttu-id="6a5bf-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a5bf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a5bf-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a5bf-116">-Name</span></span>
<span data-ttu-id="6a5bf-117">Nome impostazione sonda integrità.</span><span class="sxs-lookup"><span data-stu-id="6a5bf-117">health probe setting name.</span></span>

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

### <span data-ttu-id="6a5bf-118">-SampleSize</span><span class="sxs-lookup"><span data-stu-id="6a5bf-118">-SampleSize</span></span>
<span data-ttu-id="6a5bf-119">Numero di esempi da considerare per le decisioni di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6a5bf-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="6a5bf-120">Il valore predefinito è 4</span><span class="sxs-lookup"><span data-stu-id="6a5bf-120">Default value is 4</span></span>

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

### <span data-ttu-id="6a5bf-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="6a5bf-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="6a5bf-122">Il numero di campioni nel periodo di esempio che deve avere esito negativo è 2</span><span class="sxs-lookup"><span data-stu-id="6a5bf-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

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

### <span data-ttu-id="6a5bf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a5bf-123">CommonParameters</span></span>
<span data-ttu-id="6a5bf-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a5bf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a5bf-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a5bf-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a5bf-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a5bf-126">INPUTS</span></span>

### <span data-ttu-id="6a5bf-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6a5bf-127">None</span></span>

## <span data-ttu-id="6a5bf-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a5bf-128">OUTPUTS</span></span>

### <span data-ttu-id="6a5bf-129">Microsoft. Azure. Commands. FrontDoor. Models. PSLoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="6a5bf-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="6a5bf-130">Note</span><span class="sxs-lookup"><span data-stu-id="6a5bf-130">NOTES</span></span>

## <span data-ttu-id="6a5bf-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a5bf-131">RELATED LINKS</span></span>

<span data-ttu-id="6a5bf-132">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="6a5bf-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
