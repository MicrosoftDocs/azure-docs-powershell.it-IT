---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: ee249b7e3d811a527a9322e09ba65075883e73b6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198319"
---
# <span data-ttu-id="fec09-101">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="fec09-101">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="fec09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fec09-102">SYNOPSIS</span></span>
<span data-ttu-id="fec09-103">Aggiunge un intervallo di codici di stato previsto a un oggetto profilo di Gestione traffico locale.</span><span class="sxs-lookup"><span data-stu-id="fec09-103">Adds an expected status code range to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="fec09-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fec09-104">SYNTAX</span></span>

```
Add-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fec09-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fec09-105">DESCRIPTION</span></span>
<span data-ttu-id="fec09-106">Il cmdlet **Add-AzTrafficManagerExpectedStatusCodeRange** aggiunge un intervallo di codici di stato previsti a un oggetto profilo di Gestione traffico Azure locale.</span><span class="sxs-lookup"><span data-stu-id="fec09-106">The **Add-AzTrafficManagerExpectedStatusCodeRange** cmdlet adds a range of expected status codes to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="fec09-107">È possibile ottenere un profilo usando i cmdlet New-AzTrafficManagerProfile o Get-AzTrafficManagerProfile di accesso.</span><span class="sxs-lookup"><span data-stu-id="fec09-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="fec09-108">Questo cmdlet opera sull'oggetto profilo locale.</span><span class="sxs-lookup"><span data-stu-id="fec09-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="fec09-109">Eseguire il commit delle modifiche nel profilo per Gestione traffico usando il cmdlet Set-AzTrafficManagerProfile></span><span class="sxs-lookup"><span data-stu-id="fec09-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="fec09-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fec09-110">EXAMPLES</span></span>

### <span data-ttu-id="fec09-111">Esempio 1: Aggiungere un intervallo di codici di stato previsto a un profilo</span><span class="sxs-lookup"><span data-stu-id="fec09-111">Example 1: Add an expected status code range to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="fec09-112">Il primo comando ottiene un profilo di Gestione traffico di Azure usando il cmdlet **Get-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="fec09-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="fec09-113">Il comando archivia il profilo locale nella $TrafficManagerProfile variabile.</span><span class="sxs-lookup"><span data-stu-id="fec09-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="fec09-114">Il secondo comando aggiunge un intervallo di codici di stato previsto al profilo archiviato in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="fec09-114">The second command adds an expected status code range to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="fec09-115">Il comando finale aggiorna il profilo in Gestione traffico in modo che corrisponda al valore locale in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="fec09-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="fec09-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fec09-116">PARAMETERS</span></span>

### <span data-ttu-id="fec09-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fec09-117">-DefaultProfile</span></span>
<span data-ttu-id="fec09-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fec09-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fec09-119">-Max</span><span class="sxs-lookup"><span data-stu-id="fec09-119">-Max</span></span>
<span data-ttu-id="fec09-120">Specifica il valore più alto nell'intervallo di codici di stato da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="fec09-120">Specifies the highest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="fec09-121">-Min</span><span class="sxs-lookup"><span data-stu-id="fec09-121">-Min</span></span>
<span data-ttu-id="fec09-122">Specifica il valore più basso nell'intervallo di codici di stato da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="fec09-122">Specifies the lowest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="fec09-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fec09-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="fec09-124">Specifica un oggetto **TrafficManagerProfile** locale.</span><span class="sxs-lookup"><span data-stu-id="fec09-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="fec09-125">Questo cmdlet modifica l'oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="fec09-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="fec09-126">Per ottenere un **oggetto TrafficManagerProfile,** usare il cmdlet Get-AzTrafficManagerProfile TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="fec09-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="fec09-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fec09-127">-Confirm</span></span>
<span data-ttu-id="fec09-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fec09-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fec09-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fec09-129">-WhatIf</span></span>
<span data-ttu-id="fec09-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fec09-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fec09-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fec09-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fec09-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fec09-132">CommonParameters</span></span>
<span data-ttu-id="fec09-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fec09-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fec09-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fec09-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fec09-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="fec09-135">INPUTS</span></span>

### <span data-ttu-id="fec09-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fec09-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="fec09-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fec09-137">OUTPUTS</span></span>

### <span data-ttu-id="fec09-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fec09-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="fec09-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="fec09-139">NOTES</span></span>

## <span data-ttu-id="fec09-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fec09-140">RELATED LINKS</span></span>

[<span data-ttu-id="fec09-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="fec09-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Remove-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="fec09-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fec09-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="fec09-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fec09-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
