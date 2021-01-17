---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: ee249b7e3d811a527a9322e09ba65075883e73b6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382955"
---
# <span data-ttu-id="e3955-101">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="e3955-101">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="e3955-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3955-102">SYNOPSIS</span></span>
<span data-ttu-id="e3955-103">Aggiunge un intervallo di codice di stato previsto a un oggetto profilo di gestione traffico locale.</span><span class="sxs-lookup"><span data-stu-id="e3955-103">Adds an expected status code range to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="e3955-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3955-104">SYNTAX</span></span>

```
Add-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3955-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3955-105">DESCRIPTION</span></span>
<span data-ttu-id="e3955-106">Il cmdlet **Add-AzTrafficManagerExpectedStatusCodeRange** aggiunge un intervallo di codici di stato previsti a un oggetto profilo di Azure Traffic Manager locale.</span><span class="sxs-lookup"><span data-stu-id="e3955-106">The **Add-AzTrafficManagerExpectedStatusCodeRange** cmdlet adds a range of expected status codes to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="e3955-107">Puoi ottenere un profilo usando i cmdlet New-AzTrafficManagerProfile o Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="e3955-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="e3955-108">Questo cmdlet opera nell'oggetto profilo locale.</span><span class="sxs-lookup"><span data-stu-id="e3955-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="e3955-109">Eseguire il commit delle modifiche apportate al profilo per Traffic Manager usando il cmdlet Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="e3955-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="e3955-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3955-110">EXAMPLES</span></span>

### <span data-ttu-id="e3955-111">Esempio 1: aggiungere un intervallo di codice di stato previsto a un profilo</span><span class="sxs-lookup"><span data-stu-id="e3955-111">Example 1: Add an expected status code range to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="e3955-112">Il primo comando ottiene un profilo di Azure Traffic Manager usando il cmdlet **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="e3955-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="e3955-113">Il comando Archivia il profilo locale nella variabile $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="e3955-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="e3955-114">Il secondo comando aggiunge un intervallo di codice di stato previsto al profilo archiviato in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="e3955-114">The second command adds an expected status code range to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="e3955-115">Il comando finale aggiorna il profilo in Traffic Manager in base al valore locale in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="e3955-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="e3955-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3955-116">PARAMETERS</span></span>

### <span data-ttu-id="e3955-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3955-117">-DefaultProfile</span></span>
<span data-ttu-id="e3955-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3955-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3955-119">-Max</span><span class="sxs-lookup"><span data-stu-id="e3955-119">-Max</span></span>
<span data-ttu-id="e3955-120">Specifica il valore massimo nell'intervallo di codice di stato da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="e3955-120">Specifies the highest value in the status code range to be added.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3955-121">-Min</span><span class="sxs-lookup"><span data-stu-id="e3955-121">-Min</span></span>
<span data-ttu-id="e3955-122">Specifica il valore più basso nell'intervallo di codice di stato da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="e3955-122">Specifies the lowest value in the status code range to be added.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3955-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e3955-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="e3955-124">Specifica un oggetto **TrafficManagerProfile** locale.</span><span class="sxs-lookup"><span data-stu-id="e3955-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="e3955-125">Questo cmdlet modifica questo oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="e3955-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="e3955-126">Per ottenere un oggetto **TrafficManagerProfile** , usa il cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="e3955-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3955-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e3955-127">-Confirm</span></span>
<span data-ttu-id="e3955-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3955-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3955-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3955-129">-WhatIf</span></span>
<span data-ttu-id="e3955-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3955-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3955-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3955-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3955-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3955-132">CommonParameters</span></span>
<span data-ttu-id="e3955-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3955-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3955-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3955-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3955-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3955-135">INPUTS</span></span>

### <span data-ttu-id="e3955-136">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e3955-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="e3955-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3955-137">OUTPUTS</span></span>

### <span data-ttu-id="e3955-138">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e3955-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="e3955-139">Note</span><span class="sxs-lookup"><span data-stu-id="e3955-139">NOTES</span></span>

## <span data-ttu-id="e3955-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3955-140">RELATED LINKS</span></span>

[<span data-ttu-id="e3955-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="e3955-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Remove-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="e3955-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e3955-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="e3955-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e3955-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
