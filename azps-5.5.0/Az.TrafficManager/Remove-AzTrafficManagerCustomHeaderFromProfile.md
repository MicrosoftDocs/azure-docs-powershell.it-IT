---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D343
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
ms.openlocfilehash: 62dbdfe69feddcbd942a51c05c65e486653a2405
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182591"
---
# <span data-ttu-id="ff9df-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="ff9df-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>

## <span data-ttu-id="ff9df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff9df-102">SYNOPSIS</span></span>
<span data-ttu-id="ff9df-103">Rimuove le informazioni di intestazione personalizzate da un oggetto profilo di Gestione traffico locale.</span><span class="sxs-lookup"><span data-stu-id="ff9df-103">Removes custom header information from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="ff9df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff9df-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromProfile -Name <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff9df-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ff9df-105">DESCRIPTION</span></span>
<span data-ttu-id="ff9df-106">Il cmdlet **Remove-AzTrafficManagerCustomHeaderFromProfile** rimuove le informazioni di intestazione personalizzate da un oggetto profilo di Gestione traffico Di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="ff9df-106">The **Remove-AzTrafficManagerCustomHeaderFromProfile** cmdlet removes custom header information from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="ff9df-107">È possibile ottenere un profilo usando i cmdlet New-AzTrafficManagerProfile o Get-AzTrafficManagerProfile di accesso.</span><span class="sxs-lookup"><span data-stu-id="ff9df-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="ff9df-108">Questo cmdlet opera sull'oggetto profilo locale.</span><span class="sxs-lookup"><span data-stu-id="ff9df-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="ff9df-109">Eseguire il commit delle modifiche nel profilo per Gestione traffico usando il cmdlet Set-AzTrafficManagerProfile></span><span class="sxs-lookup"><span data-stu-id="ff9df-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="ff9df-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff9df-110">EXAMPLES</span></span>

### <span data-ttu-id="ff9df-111">Esempio 1: Rimuovere informazioni di intestazione personalizzate da un profilo</span><span class="sxs-lookup"><span data-stu-id="ff9df-111">Example 1: Remove custom header information from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerProfile $TrafficManagerProfile -Name "host"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="ff9df-112">Il primo comando ottiene un profilo di Gestione traffico di Azure usando il cmdlet **Get-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="ff9df-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="ff9df-113">Il secondo comando rimuove le informazioni di intestazione personalizzate dal profilo archiviato in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="ff9df-113">The second command removes custom header information from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="ff9df-114">Il comando finale aggiorna il profilo in Gestione traffico in modo che corrisponda al valore locale in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="ff9df-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="ff9df-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff9df-115">PARAMETERS</span></span>

### <span data-ttu-id="ff9df-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff9df-116">-DefaultProfile</span></span>
<span data-ttu-id="ff9df-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ff9df-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff9df-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ff9df-118">-Name</span></span>
<span data-ttu-id="ff9df-119">Specifica il nome delle informazioni di intestazione personalizzate da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ff9df-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="ff9df-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ff9df-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="ff9df-121">Specifica un oggetto **TrafficManagerProfile** locale.</span><span class="sxs-lookup"><span data-stu-id="ff9df-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="ff9df-122">Questo cmdlet modifica l'oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="ff9df-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="ff9df-123">Per ottenere un **oggetto TrafficManagerProfile,** usare il cmdlet Get-AzTrafficManagerProfile TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="ff9df-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="ff9df-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff9df-124">-Confirm</span></span>
<span data-ttu-id="ff9df-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff9df-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff9df-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff9df-126">-WhatIf</span></span>
<span data-ttu-id="ff9df-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff9df-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff9df-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff9df-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff9df-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff9df-129">CommonParameters</span></span>
<span data-ttu-id="ff9df-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff9df-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff9df-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff9df-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff9df-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="ff9df-132">INPUTS</span></span>

### <span data-ttu-id="ff9df-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ff9df-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="ff9df-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff9df-134">OUTPUTS</span></span>

### <span data-ttu-id="ff9df-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ff9df-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="ff9df-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="ff9df-136">NOTES</span></span>

## <span data-ttu-id="ff9df-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff9df-137">RELATED LINKS</span></span>

[<span data-ttu-id="ff9df-138">Add-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="ff9df-138">Add-AzTrafficManagerCustomHeaderToProfile</span></span>](./Add-AzTrafficManagerCustomHeaderToProfile.md)

[<span data-ttu-id="ff9df-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ff9df-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="ff9df-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ff9df-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
