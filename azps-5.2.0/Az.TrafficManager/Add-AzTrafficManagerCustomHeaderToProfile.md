---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
ms.openlocfilehash: b90e83a403be59f5c454c0c055f0fe4719c3116f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345640"
---
# <span data-ttu-id="0a4bd-101">Add-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="0a4bd-101">Add-AzTrafficManagerCustomHeaderToProfile</span></span>

## <span data-ttu-id="0a4bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0a4bd-102">SYNOPSIS</span></span>
<span data-ttu-id="0a4bd-103">Aggiunge informazioni di intestazione personalizzate a un oggetto profilo di gestione traffico locale.</span><span class="sxs-lookup"><span data-stu-id="0a4bd-103">Adds custom header information to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="0a4bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a4bd-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToProfile -Name <String> -Value <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a4bd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a4bd-105">DESCRIPTION</span></span>
<span data-ttu-id="0a4bd-106">Il cmdlet **Add-AzTrafficManagerCustomHeaderToProfile** aggiunge informazioni di intestazione personalizzate a un oggetto profilo di Azure Traffic Manager locale.</span><span class="sxs-lookup"><span data-stu-id="0a4bd-106">The **Add-AzTrafficManagerCustomHeaderToProfile** cmdlet adds custom header information to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="0a4bd-107">Puoi ottenere un profilo usando i cmdlet New-AzTrafficManagerProfile o Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="0a4bd-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="0a4bd-108">Questo cmdlet opera nell'oggetto profilo locale.</span><span class="sxs-lookup"><span data-stu-id="0a4bd-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="0a4bd-109">Eseguire il commit delle modifiche apportate al profilo per Traffic Manager usando il cmdlet Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="0a4bd-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="0a4bd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a4bd-110">EXAMPLES</span></span>

### <span data-ttu-id="0a4bd-111">Esempio 1: aggiungere informazioni di intestazione personalizzate a un profilo</span><span class="sxs-lookup"><span data-stu-id="0a4bd-111">Example 1: Add custom header information to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerCustomHeaderToProfile -TrafficManagerProfile $TrafficManagerProfile -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="0a4bd-112">Il primo comando ottiene un profilo di Azure Traffic Manager usando il cmdlet **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="0a4bd-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="0a4bd-113">Il comando Archivia il profilo locale nella variabile $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="0a4bd-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="0a4bd-114">Il secondo comando aggiunge informazioni di intestazione personalizzate al profilo archiviato in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="0a4bd-114">The second command adds custom header information to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="0a4bd-115">Il comando finale aggiorna il profilo in Traffic Manager in base al valore locale in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="0a4bd-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="0a4bd-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0a4bd-116">PARAMETERS</span></span>

### <span data-ttu-id="0a4bd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a4bd-117">-DefaultProfile</span></span>
<span data-ttu-id="0a4bd-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0a4bd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a4bd-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a4bd-119">-Name</span></span>
<span data-ttu-id="0a4bd-120">Specifica il nome delle informazioni di intestazione personalizzate da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="0a4bd-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="0a4bd-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0a4bd-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="0a4bd-122">Specifica un oggetto **TrafficManagerProfile** locale.</span><span class="sxs-lookup"><span data-stu-id="0a4bd-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="0a4bd-123">Questo cmdlet modifica questo oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="0a4bd-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="0a4bd-124">Per ottenere un oggetto **TrafficManagerProfile** , usa il cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="0a4bd-124">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="0a4bd-125">-Valore</span><span class="sxs-lookup"><span data-stu-id="0a4bd-125">-Value</span></span>
<span data-ttu-id="0a4bd-126">Specifica il valore delle informazioni di intestazione personalizzate da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="0a4bd-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="0a4bd-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0a4bd-127">-Confirm</span></span>
<span data-ttu-id="0a4bd-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a4bd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a4bd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a4bd-129">-WhatIf</span></span>
<span data-ttu-id="0a4bd-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a4bd-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a4bd-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a4bd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a4bd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a4bd-132">CommonParameters</span></span>
<span data-ttu-id="0a4bd-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a4bd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a4bd-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a4bd-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a4bd-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0a4bd-135">INPUTS</span></span>

### <span data-ttu-id="0a4bd-136">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0a4bd-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="0a4bd-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a4bd-137">OUTPUTS</span></span>

### <span data-ttu-id="0a4bd-138">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0a4bd-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="0a4bd-139">Note</span><span class="sxs-lookup"><span data-stu-id="0a4bd-139">NOTES</span></span>

## <span data-ttu-id="0a4bd-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a4bd-140">RELATED LINKS</span></span>

[<span data-ttu-id="0a4bd-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="0a4bd-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>](./Remove-AzTrafficManagerCustomHeaderFromProfile.md)

[<span data-ttu-id="0a4bd-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0a4bd-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="0a4bd-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0a4bd-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
