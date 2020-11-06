---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: de13a33aeaf60dbd83fcacebb8380bee27c18c46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511715"
---
# <span data-ttu-id="97b86-101">New-AzureRmFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="97b86-101">New-AzureRmFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="97b86-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97b86-102">SYNOPSIS</span></span>
<span data-ttu-id="97b86-103">Creare un oggetto PSLoadBalancingSetting per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="97b86-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97b86-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97b86-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97b86-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97b86-105">DESCRIPTION</span></span>
<span data-ttu-id="97b86-106">Creare un oggetto PSLoadBalancingSetting per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="97b86-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="97b86-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97b86-107">EXAMPLES</span></span>

### <span data-ttu-id="97b86-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="97b86-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorLoadBalancingSettingObject -Name "loadbalancingsetting1"


SampleSize                    : 4
AdditionalLatencyMilliseconds : 0
SuccessfulSamplesRequired     : 2
ResourceState                 :
Id                            :
Name                          : loadbalancingsetting1
Type                          :
```

<span data-ttu-id="97b86-109">Creare un oggetto PSLoadBalancingSetting per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="97b86-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="97b86-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97b86-110">PARAMETERS</span></span>

### <span data-ttu-id="97b86-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="97b86-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="97b86-112">Latenza aggiuntiva in millisecondi per le sonde che rientrano nel bucket di latenza più bassa.</span><span class="sxs-lookup"><span data-stu-id="97b86-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="97b86-113">Il valore predefinito è 0</span><span class="sxs-lookup"><span data-stu-id="97b86-113">Default value is 0</span></span>

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

### <span data-ttu-id="97b86-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97b86-114">-DefaultProfile</span></span>
<span data-ttu-id="97b86-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="97b86-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b86-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="97b86-116">-Name</span></span>
<span data-ttu-id="97b86-117">Nome impostazione sonda integrità.</span><span class="sxs-lookup"><span data-stu-id="97b86-117">health probe setting name.</span></span>

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

### <span data-ttu-id="97b86-118">-SampleSize</span><span class="sxs-lookup"><span data-stu-id="97b86-118">-SampleSize</span></span>
<span data-ttu-id="97b86-119">Numero di esempi da considerare per le decisioni di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="97b86-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="97b86-120">Il valore predefinito è 4</span><span class="sxs-lookup"><span data-stu-id="97b86-120">Default value is 4</span></span>

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

### <span data-ttu-id="97b86-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="97b86-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="97b86-122">Il numero di campioni nel periodo di esempio che deve avere esito negativo è 2</span><span class="sxs-lookup"><span data-stu-id="97b86-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

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

### <span data-ttu-id="97b86-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b86-123">CommonParameters</span></span>
<span data-ttu-id="97b86-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97b86-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b86-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97b86-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b86-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97b86-126">INPUTS</span></span>

### <span data-ttu-id="97b86-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="97b86-127">None</span></span>

## <span data-ttu-id="97b86-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97b86-128">OUTPUTS</span></span>

### <span data-ttu-id="97b86-129">Microsoft. Azure. Commands. FrontDoor. Models. PSLoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="97b86-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="97b86-130">Note</span><span class="sxs-lookup"><span data-stu-id="97b86-130">NOTES</span></span>

## <span data-ttu-id="97b86-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97b86-131">RELATED LINKS</span></span>

<span data-ttu-id="97b86-132">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="97b86-132">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
