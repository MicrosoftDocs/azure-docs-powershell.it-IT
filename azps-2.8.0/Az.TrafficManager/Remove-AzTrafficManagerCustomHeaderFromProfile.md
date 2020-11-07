---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D343
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
ms.openlocfilehash: f7870cd3c6786388e34a9b243c962aa48788f91a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858421"
---
# <span data-ttu-id="dbd7d-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="dbd7d-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>

## <span data-ttu-id="dbd7d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dbd7d-102">SYNOPSIS</span></span>
<span data-ttu-id="dbd7d-103">Rimuove le informazioni di intestazione personalizzate da un oggetto profilo di gestione traffico locale.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-103">Removes custom header information from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="dbd7d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dbd7d-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromProfile -Name <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbd7d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dbd7d-105">DESCRIPTION</span></span>
<span data-ttu-id="dbd7d-106">Il cmdlet **Remove-AzTrafficManagerCustomHeaderFromProfile** rimuove le informazioni di intestazione personalizzate da un oggetto profilo di Azure Traffic Manager locale.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-106">The **Remove-AzTrafficManagerCustomHeaderFromProfile** cmdlet removes custom header information from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="dbd7d-107">Puoi ottenere un profilo usando i cmdlet New-AzTrafficManagerProfile o Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="dbd7d-108">Questo cmdlet opera nell'oggetto profilo locale.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="dbd7d-109">Eseguire il commit delle modifiche apportate al profilo per Traffic Manager usando il cmdlet Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="dbd7d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dbd7d-110">EXAMPLES</span></span>

### <span data-ttu-id="dbd7d-111">Esempio 1: rimuovere le informazioni di intestazione personalizzate da un profilo</span><span class="sxs-lookup"><span data-stu-id="dbd7d-111">Example 1: Remove custom header information from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerProfile $TrafficManagerProfile -Name "host"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="dbd7d-112">Il primo comando ottiene un profilo di Azure Traffic Manager usando il cmdlet **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="dbd7d-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="dbd7d-113">Il secondo comando rimuove le informazioni di intestazione personalizzate dal profilo archiviato in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-113">The second command removes custom header information from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="dbd7d-114">Il comando finale aggiorna il profilo in Traffic Manager in base al valore locale in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="dbd7d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dbd7d-115">PARAMETERS</span></span>

### <span data-ttu-id="dbd7d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbd7d-116">-DefaultProfile</span></span>
<span data-ttu-id="dbd7d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbd7d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="dbd7d-118">-Name</span></span>
<span data-ttu-id="dbd7d-119">Specifica il nome delle informazioni di intestazione personalizzate da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="dbd7d-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="dbd7d-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="dbd7d-121">Specifica un oggetto **TrafficManagerProfile** locale.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="dbd7d-122">Questo cmdlet modifica questo oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="dbd7d-123">Per ottenere un oggetto **TrafficManagerProfile** , usa il cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="dbd7d-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dbd7d-124">-Confirm</span></span>
<span data-ttu-id="dbd7d-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbd7d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbd7d-126">-WhatIf</span></span>
<span data-ttu-id="dbd7d-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dbd7d-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbd7d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbd7d-129">CommonParameters</span></span>
<span data-ttu-id="dbd7d-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbd7d-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbd7d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbd7d-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dbd7d-132">INPUTS</span></span>

### <span data-ttu-id="dbd7d-133">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="dbd7d-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="dbd7d-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dbd7d-134">OUTPUTS</span></span>

### <span data-ttu-id="dbd7d-135">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="dbd7d-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="dbd7d-136">Note</span><span class="sxs-lookup"><span data-stu-id="dbd7d-136">NOTES</span></span>

## <span data-ttu-id="dbd7d-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dbd7d-137">RELATED LINKS</span></span>

[<span data-ttu-id="dbd7d-138">Add-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="dbd7d-138">Add-AzTrafficManagerCustomHeaderToProfile</span></span>](./Add-AzTrafficManagerCustomHeaderToProfile.md)

[<span data-ttu-id="dbd7d-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="dbd7d-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="dbd7d-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="dbd7d-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
