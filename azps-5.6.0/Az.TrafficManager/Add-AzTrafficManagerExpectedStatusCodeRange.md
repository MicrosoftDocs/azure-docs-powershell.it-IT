---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/add-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 88755e6830342dc7636bdb0b338269c47bc23398
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987376"
---
# <span data-ttu-id="d120f-101">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="d120f-101">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="d120f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d120f-102">SYNOPSIS</span></span>
<span data-ttu-id="d120f-103">Aggiunge un intervallo di codici di stato previsto a un oggetto profilo di Gestione traffico locale.</span><span class="sxs-lookup"><span data-stu-id="d120f-103">Adds an expected status code range to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="d120f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d120f-104">SYNTAX</span></span>

```
Add-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d120f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d120f-105">DESCRIPTION</span></span>
<span data-ttu-id="d120f-106">Il cmdlet **Add-AzTrafficManagerExpectedStatusCodeRange** aggiunge un intervallo di codici di stato previsti a un oggetto profilo di Gestione traffico Azure locale.</span><span class="sxs-lookup"><span data-stu-id="d120f-106">The **Add-AzTrafficManagerExpectedStatusCodeRange** cmdlet adds a range of expected status codes to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="d120f-107">È possibile ottenere un profilo usando i cmdlet New-AzTrafficManagerProfile o Get-AzTrafficManagerProfile servizio.</span><span class="sxs-lookup"><span data-stu-id="d120f-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="d120f-108">Questo cmdlet opera sull'oggetto profilo locale.</span><span class="sxs-lookup"><span data-stu-id="d120f-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="d120f-109">Eseguire il commit delle modifiche nel profilo per Gestione traffico usando il cmdlet Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="d120f-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="d120f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d120f-110">EXAMPLES</span></span>

### <span data-ttu-id="d120f-111">Esempio 1: Aggiungere un intervallo di codici di stato previsto a un profilo</span><span class="sxs-lookup"><span data-stu-id="d120f-111">Example 1: Add an expected status code range to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="d120f-112">Il primo comando ottiene un profilo di Gestione traffico di Azure usando il cmdlet **Get-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="d120f-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="d120f-113">Il comando archivia il profilo locale nella $TrafficManagerProfile variabile.</span><span class="sxs-lookup"><span data-stu-id="d120f-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="d120f-114">Il secondo comando aggiunge un intervallo di codici di stato previsto al profilo archiviato in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="d120f-114">The second command adds an expected status code range to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="d120f-115">Il comando finale aggiorna il profilo in Gestione traffico in modo che corrisponda al valore locale in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="d120f-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="d120f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d120f-116">PARAMETERS</span></span>

### <span data-ttu-id="d120f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d120f-117">-DefaultProfile</span></span>
<span data-ttu-id="d120f-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d120f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d120f-119">-Max</span><span class="sxs-lookup"><span data-stu-id="d120f-119">-Max</span></span>
<span data-ttu-id="d120f-120">Specifica il valore più alto nell'intervallo di codici di stato da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="d120f-120">Specifies the highest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="d120f-121">-Min</span><span class="sxs-lookup"><span data-stu-id="d120f-121">-Min</span></span>
<span data-ttu-id="d120f-122">Specifica il valore più basso nell'intervallo di codici di stato da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="d120f-122">Specifies the lowest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="d120f-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d120f-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="d120f-124">Specifica un oggetto **TrafficManagerProfile** locale.</span><span class="sxs-lookup"><span data-stu-id="d120f-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="d120f-125">Questo cmdlet modifica l'oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="d120f-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="d120f-126">Per ottenere un **oggetto TrafficManagerProfile,** usare il cmdlet Get-AzTrafficManagerProfile TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="d120f-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="d120f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d120f-127">-Confirm</span></span>
<span data-ttu-id="d120f-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d120f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d120f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d120f-129">-WhatIf</span></span>
<span data-ttu-id="d120f-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d120f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d120f-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d120f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d120f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d120f-132">CommonParameters</span></span>
<span data-ttu-id="d120f-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d120f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d120f-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d120f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d120f-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="d120f-135">INPUTS</span></span>

### <span data-ttu-id="d120f-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d120f-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="d120f-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d120f-137">OUTPUTS</span></span>

### <span data-ttu-id="d120f-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d120f-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="d120f-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="d120f-139">NOTES</span></span>

## <span data-ttu-id="d120f-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d120f-140">RELATED LINKS</span></span>

[<span data-ttu-id="d120f-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="d120f-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Remove-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="d120f-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d120f-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="d120f-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d120f-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
