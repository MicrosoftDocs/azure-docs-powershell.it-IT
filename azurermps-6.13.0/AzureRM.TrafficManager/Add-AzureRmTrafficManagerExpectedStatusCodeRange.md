---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurertmtrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 32a00a6dce3d6a370f7b7f79f05794a312277a09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507256"
---
# <span data-ttu-id="f1c68-101">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="f1c68-101">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="f1c68-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f1c68-102">SYNOPSIS</span></span>
<span data-ttu-id="f1c68-103">Aggiunge un intervallo di codice di stato previsto a un oggetto profilo di gestione traffico locale.</span><span class="sxs-lookup"><span data-stu-id="f1c68-103">Adds an expected status code range to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1c68-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f1c68-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1c68-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1c68-105">DESCRIPTION</span></span>
<span data-ttu-id="f1c68-106">Il cmdlet **Add-AzureRmTrafficManagerExpectedStatusCodeRange** aggiunge un intervallo di codici di stato previsti a un oggetto profilo di Azure Traffic Manager locale.</span><span class="sxs-lookup"><span data-stu-id="f1c68-106">The **Add-AzureRmTrafficManagerExpectedStatusCodeRange** cmdlet adds a range of expected status codes to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="f1c68-107">Puoi ottenere un profilo usando i cmdlet New-AzureRmTrafficManagerProfile o Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f1c68-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="f1c68-108">Questo cmdlet opera nell'oggetto profilo locale.</span><span class="sxs-lookup"><span data-stu-id="f1c68-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="f1c68-109">Eseguire il commit delle modifiche apportate al profilo per Traffic Manager usando il cmdlet Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f1c68-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="f1c68-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f1c68-110">EXAMPLES</span></span>

### <span data-ttu-id="f1c68-111">Esempio 1: aggiungere un intervallo di codice di stato previsto a un profilo</span><span class="sxs-lookup"><span data-stu-id="f1c68-111">Example 1: Add an expected status code range to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="f1c68-112">Il primo comando ottiene un profilo di Azure Traffic Manager usando il cmdlet **Get-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="f1c68-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="f1c68-113">Il comando Archivia il profilo locale nella variabile $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f1c68-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="f1c68-114">Il secondo comando aggiunge un intervallo di codice di stato previsto al profilo archiviato in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f1c68-114">The second command adds an expected status code range to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="f1c68-115">Il comando finale aggiorna il profilo in Traffic Manager in base al valore locale in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f1c68-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="f1c68-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f1c68-116">PARAMETERS</span></span>

### <span data-ttu-id="f1c68-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1c68-117">-DefaultProfile</span></span>
<span data-ttu-id="f1c68-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f1c68-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1c68-119">-Max</span><span class="sxs-lookup"><span data-stu-id="f1c68-119">-Max</span></span>
<span data-ttu-id="f1c68-120">Specifica il valore massimo nell'intervallo di codice di stato da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="f1c68-120">Specifies the highest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="f1c68-121">-Min</span><span class="sxs-lookup"><span data-stu-id="f1c68-121">-Min</span></span>
<span data-ttu-id="f1c68-122">Specifica il valore più basso nell'intervallo di codice di stato da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="f1c68-122">Specifies the lowest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="f1c68-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f1c68-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="f1c68-124">Specifica un oggetto **TrafficManagerProfile** locale.</span><span class="sxs-lookup"><span data-stu-id="f1c68-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="f1c68-125">Questo cmdlet modifica questo oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="f1c68-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="f1c68-126">Per ottenere un oggetto **TrafficManagerProfile** , usa il cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f1c68-126">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="f1c68-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f1c68-127">-Confirm</span></span>
<span data-ttu-id="f1c68-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1c68-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1c68-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1c68-129">-WhatIf</span></span>
<span data-ttu-id="f1c68-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f1c68-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1c68-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f1c68-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1c68-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1c68-132">CommonParameters</span></span>
<span data-ttu-id="f1c68-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1c68-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1c68-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1c68-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1c68-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f1c68-135">INPUTS</span></span>

### <span data-ttu-id="f1c68-136">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f1c68-136">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="f1c68-137">Questo cmdlet accetta un oggetto **TrafficManagerProfile** per questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1c68-137">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="f1c68-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f1c68-138">OUTPUTS</span></span>

### <span data-ttu-id="f1c68-139">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f1c68-139">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="f1c68-140">Questo cmdlet restituisce un oggetto **TrafficManagerProfile** modificato.</span><span class="sxs-lookup"><span data-stu-id="f1c68-140">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="f1c68-141">Note</span><span class="sxs-lookup"><span data-stu-id="f1c68-141">NOTES</span></span>

## <span data-ttu-id="f1c68-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f1c68-142">RELATED LINKS</span></span>

[<span data-ttu-id="f1c68-143">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="f1c68-143">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>](./Remove-AzureRmTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="f1c68-144">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f1c68-144">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="f1c68-145">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f1c68-145">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)
