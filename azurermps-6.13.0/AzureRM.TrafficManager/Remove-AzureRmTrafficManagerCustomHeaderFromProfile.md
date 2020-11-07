---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D343
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagercustomheaderfromprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromProfile.md
ms.openlocfilehash: af18a5a93cf08fe4806af429aee667b569c527d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688044"
---
# <span data-ttu-id="de771-101">Remove-AzureRmTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="de771-101">Remove-AzureRmTrafficManagerCustomHeaderFromProfile</span></span>

## <span data-ttu-id="de771-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="de771-102">SYNOPSIS</span></span>
<span data-ttu-id="de771-103">Rimuove le informazioni di intestazione personalizzate da un oggetto profilo di gestione traffico locale.</span><span class="sxs-lookup"><span data-stu-id="de771-103">Removes custom header information from a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de771-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de771-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerCustomHeaderFromProfile -Name <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de771-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de771-105">DESCRIPTION</span></span>
<span data-ttu-id="de771-106">Il cmdlet **Remove-AzureRmTrafficManagerCustomHeaderFromProfile** rimuove le informazioni di intestazione personalizzate da un oggetto profilo di Azure Traffic Manager locale.</span><span class="sxs-lookup"><span data-stu-id="de771-106">The **Remove-AzureRmTrafficManagerCustomHeaderFromProfile** cmdlet removes custom header information from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="de771-107">Puoi ottenere un profilo usando i cmdlet New-AzureRmTrafficManagerProfile o Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="de771-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="de771-108">Questo cmdlet opera nell'oggetto profilo locale.</span><span class="sxs-lookup"><span data-stu-id="de771-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="de771-109">Eseguire il commit delle modifiche apportate al profilo per Traffic Manager usando il cmdlet Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="de771-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="de771-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de771-110">EXAMPLES</span></span>

### <span data-ttu-id="de771-111">Esempio 1: rimuovere le informazioni di intestazione personalizzate da un profilo</span><span class="sxs-lookup"><span data-stu-id="de771-111">Example 1: Remove custom header information from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint -TrafficManagerProfile $TrafficManagerProfile -Name "host"
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="de771-112">Il primo comando ottiene un profilo di Azure Traffic Manager usando il cmdlet **Get-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="de771-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="de771-113">Il secondo comando rimuove le informazioni di intestazione personalizzate dal profilo archiviato in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="de771-113">The second command removes custom header information from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="de771-114">Il comando finale aggiorna il profilo in Traffic Manager in base al valore locale in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="de771-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="de771-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="de771-115">PARAMETERS</span></span>

### <span data-ttu-id="de771-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de771-116">-DefaultProfile</span></span>
<span data-ttu-id="de771-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de771-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de771-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="de771-118">-Name</span></span>
<span data-ttu-id="de771-119">Specifica il nome delle informazioni di intestazione personalizzate da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="de771-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="de771-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="de771-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="de771-121">Specifica un oggetto **TrafficManagerProfile** locale.</span><span class="sxs-lookup"><span data-stu-id="de771-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="de771-122">Questo cmdlet modifica questo oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="de771-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="de771-123">Per ottenere un oggetto **TrafficManagerProfile** , usa il cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="de771-123">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="de771-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="de771-124">-Confirm</span></span>
<span data-ttu-id="de771-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de771-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de771-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de771-126">-WhatIf</span></span>
<span data-ttu-id="de771-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de771-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de771-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de771-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de771-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de771-129">CommonParameters</span></span>
<span data-ttu-id="de771-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de771-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de771-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de771-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de771-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="de771-132">INPUTS</span></span>

### <span data-ttu-id="de771-133">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="de771-133">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="de771-134">Questo cmdlet accetta un oggetto **TrafficManagerProfile** per questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de771-134">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="de771-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de771-135">OUTPUTS</span></span>

### <span data-ttu-id="de771-136">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="de771-136">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="de771-137">Questo cmdlet restituisce un oggetto **TrafficManagerProfile** modificato.</span><span class="sxs-lookup"><span data-stu-id="de771-137">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="de771-138">Note</span><span class="sxs-lookup"><span data-stu-id="de771-138">NOTES</span></span>

## <span data-ttu-id="de771-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de771-139">RELATED LINKS</span></span>

[<span data-ttu-id="de771-140">Add-AzureRmTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="de771-140">Add-AzureRmTrafficManagerCustomHeaderToProfile</span></span>](./Add-AzureRmTrafficManagerCustomHeaderToProfile.md)

[<span data-ttu-id="de771-141">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="de771-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="de771-142">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="de771-142">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)
