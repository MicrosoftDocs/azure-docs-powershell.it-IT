---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
ms.openlocfilehash: 1b1dab7edc07242dab28daa6028adefb8b7090eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988663"
---
# <span data-ttu-id="0956d-101">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0956d-101">Remove-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="0956d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0956d-102">SYNOPSIS</span></span>
<span data-ttu-id="0956d-103">Elimina un profilo di Gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="0956d-103">Deletes a Traffic Manager profile.</span></span>

## <span data-ttu-id="0956d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0956d-104">SYNTAX</span></span>

### <span data-ttu-id="0956d-105">Campi</span><span class="sxs-lookup"><span data-stu-id="0956d-105">Fields</span></span>
```
Remove-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0956d-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="0956d-106">Object</span></span>
```
Remove-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0956d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0956d-107">DESCRIPTION</span></span>
<span data-ttu-id="0956d-108">Il cmdlet **Remove-AzTrafficManagerProfile** elimina un profilo di Gestione traffico di Azure.</span><span class="sxs-lookup"><span data-stu-id="0956d-108">The **Remove-AzTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="0956d-109">Specificare il profilo da eliminare usando i *parametri Name* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="0956d-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="0956d-110">In alternativa, è possibile specificare un **oggetto TrafficManagerProfile** usando il *parametro TrafficManagerProfile* oppure usare la pipeline.</span><span class="sxs-lookup"><span data-stu-id="0956d-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="0956d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0956d-111">EXAMPLES</span></span>

### <span data-ttu-id="0956d-112">Esempio 1: Eliminare un profilo specificato in base al nome</span><span class="sxs-lookup"><span data-stu-id="0956d-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="0956d-113">Questo comando elimina il profilo denominato ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0956d-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="0956d-114">Il comando chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="0956d-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="0956d-115">Esempio 2: Eliminare un profilo usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="0956d-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzTrafficManagerProfile -Force
```

<span data-ttu-id="0956d-116">Questo comando recupera il profilo denominato ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0956d-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="0956d-117">Il comando passa quindi il profilo al cmdlet **Remove-AzTrafficManagerProfile** usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="0956d-117">The command then passes that profile to the **Remove-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0956d-118">Questo cmdlet elimina il profilo.</span><span class="sxs-lookup"><span data-stu-id="0956d-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="0956d-119">Il comando specifica il *parametro Force.*</span><span class="sxs-lookup"><span data-stu-id="0956d-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="0956d-120">Di conseguenza, non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="0956d-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="0956d-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0956d-121">PARAMETERS</span></span>

### <span data-ttu-id="0956d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0956d-122">-DefaultProfile</span></span>
<span data-ttu-id="0956d-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0956d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0956d-124">-Force</span><span class="sxs-lookup"><span data-stu-id="0956d-124">-Force</span></span>
<span data-ttu-id="0956d-125">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="0956d-125">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0956d-126">-Name</span><span class="sxs-lookup"><span data-stu-id="0956d-126">-Name</span></span>
<span data-ttu-id="0956d-127">Specifica il nome del profilo di Gestione traffico eliminato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0956d-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0956d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0956d-128">-ResourceGroupName</span></span>
<span data-ttu-id="0956d-129">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0956d-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="0956d-130">Questo cmdlet elimina un profilo di Gestione traffico nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="0956d-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0956d-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0956d-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="0956d-132">Specifica un **oggetto TrafficManagerProfile** da eliminare.</span><span class="sxs-lookup"><span data-stu-id="0956d-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="0956d-133">Per ottenere un **oggetto TrafficManagerProfile,** usare il cmdlet Get-AzTrafficManagerProfile TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="0956d-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0956d-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0956d-134">-Confirm</span></span>
<span data-ttu-id="0956d-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0956d-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0956d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0956d-136">-WhatIf</span></span>
<span data-ttu-id="0956d-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0956d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0956d-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0956d-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0956d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0956d-139">CommonParameters</span></span>
<span data-ttu-id="0956d-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0956d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0956d-141">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0956d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0956d-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="0956d-142">INPUTS</span></span>

### <span data-ttu-id="0956d-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0956d-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="0956d-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0956d-144">OUTPUTS</span></span>

### <span data-ttu-id="0956d-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0956d-145">System.Boolean</span></span>

## <span data-ttu-id="0956d-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="0956d-146">NOTES</span></span>

## <span data-ttu-id="0956d-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0956d-147">RELATED LINKS</span></span>

[<span data-ttu-id="0956d-148">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0956d-148">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="0956d-149">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0956d-149">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="0956d-150">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0956d-150">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="0956d-151">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0956d-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="0956d-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0956d-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


