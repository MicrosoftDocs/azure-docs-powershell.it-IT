---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 8e79fe1a0d0cc1c681c88cb3d5dfdd8d48dfd26b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987263"
---
# <span data-ttu-id="56c92-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="56c92-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="56c92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56c92-102">SYNOPSIS</span></span>
<span data-ttu-id="56c92-103">Rimuove un intervallo di codici di stato previsto da un oggetto profilo di Gestione traffico locale.</span><span class="sxs-lookup"><span data-stu-id="56c92-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="56c92-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56c92-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56c92-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="56c92-105">DESCRIPTION</span></span>
<span data-ttu-id="56c92-106">Il cmdlet **Remove-AzTrafficManagerExpectedStatusCodeRange** rimuove un intervallo di codici di stato previsti da un oggetto profilo di Gestione traffico Azure locale.</span><span class="sxs-lookup"><span data-stu-id="56c92-106">The **Remove-AzTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="56c92-107">È possibile ottenere un profilo usando i cmdlet New-AzTrafficManagerProfile o Get-AzTrafficManagerProfile di accesso.</span><span class="sxs-lookup"><span data-stu-id="56c92-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="56c92-108">Questo cmdlet opera sull'oggetto profilo locale.</span><span class="sxs-lookup"><span data-stu-id="56c92-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="56c92-109">Eseguire il commit delle modifiche nel profilo per Gestione traffico usando il cmdlet Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="56c92-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="56c92-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56c92-110">EXAMPLES</span></span>

### <span data-ttu-id="56c92-111">Esempio 1: Rimuovere un intervallo di codici di stato previsto da un profilo</span><span class="sxs-lookup"><span data-stu-id="56c92-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="56c92-112">Il primo comando ottiene un profilo di Gestione traffico di Azure usando il cmdlet **Get-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="56c92-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="56c92-113">Il secondo comando rimuove un intervallo di codici di stato previsto dal profilo archiviato in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="56c92-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="56c92-114">Il comando finale aggiorna il profilo in Gestione traffico in modo che corrisponda al valore locale in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="56c92-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="56c92-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56c92-115">PARAMETERS</span></span>

### <span data-ttu-id="56c92-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56c92-116">-DefaultProfile</span></span>
<span data-ttu-id="56c92-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56c92-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56c92-118">-Min</span><span class="sxs-lookup"><span data-stu-id="56c92-118">-Min</span></span>
<span data-ttu-id="56c92-119">Specifica il valore più basso nell'intervallo di codici di stato da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="56c92-119">Specifies the lowest value in the status code range to be removed.</span></span>

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

### <span data-ttu-id="56c92-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="56c92-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="56c92-121">Specifica un oggetto **TrafficManagerProfile** locale.</span><span class="sxs-lookup"><span data-stu-id="56c92-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="56c92-122">Questo cmdlet modifica l'oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="56c92-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="56c92-123">Per ottenere un **oggetto TrafficManagerProfile,** usare il cmdlet Get-AzTrafficManagerProfile TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="56c92-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="56c92-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56c92-124">-Confirm</span></span>
<span data-ttu-id="56c92-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56c92-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56c92-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56c92-126">-WhatIf</span></span>
<span data-ttu-id="56c92-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56c92-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56c92-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56c92-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56c92-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56c92-129">CommonParameters</span></span>
<span data-ttu-id="56c92-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56c92-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56c92-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56c92-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56c92-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="56c92-132">INPUTS</span></span>

### <span data-ttu-id="56c92-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="56c92-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="56c92-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56c92-134">OUTPUTS</span></span>

### <span data-ttu-id="56c92-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="56c92-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="56c92-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="56c92-136">NOTES</span></span>

## <span data-ttu-id="56c92-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56c92-137">RELATED LINKS</span></span>

[<span data-ttu-id="56c92-138">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="56c92-138">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="56c92-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="56c92-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="56c92-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="56c92-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
