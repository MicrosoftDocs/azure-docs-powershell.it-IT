---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
ms.openlocfilehash: 640aed5ccfb38a2dca6989048e3185774ceda15a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346420"
---
# <span data-ttu-id="ca3a2-101">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ca3a2-101">Remove-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="ca3a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca3a2-102">SYNOPSIS</span></span>
<span data-ttu-id="ca3a2-103">Elimina un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="ca3a2-103">Deletes a Traffic Manager profile.</span></span>

## <span data-ttu-id="ca3a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca3a2-104">SYNTAX</span></span>

### <span data-ttu-id="ca3a2-105">Campi</span><span class="sxs-lookup"><span data-stu-id="ca3a2-105">Fields</span></span>
```
Remove-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca3a2-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="ca3a2-106">Object</span></span>
```
Remove-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca3a2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca3a2-107">DESCRIPTION</span></span>
<span data-ttu-id="ca3a2-108">Il cmdlet **Remove-AzTrafficManagerProfile** Elimina un profilo di Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="ca3a2-108">The **Remove-AzTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="ca3a2-109">Specificare il profilo da eliminare usando i parametri *Name* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="ca3a2-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="ca3a2-110">In alternativa, puoi specificare un oggetto **TrafficManagerProfile** usando il parametro *TrafficManagerProfile* oppure puoi usare la pipeline.</span><span class="sxs-lookup"><span data-stu-id="ca3a2-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="ca3a2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca3a2-111">EXAMPLES</span></span>

### <span data-ttu-id="ca3a2-112">Esempio 1: eliminare un profilo specificato per nome</span><span class="sxs-lookup"><span data-stu-id="ca3a2-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="ca3a2-113">Questo comando Elimina il profilo denominato ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ca3a2-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="ca3a2-114">Il comando richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="ca3a2-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="ca3a2-115">Esempio 2: eliminare un profilo tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="ca3a2-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzTrafficManagerProfile -Force
```

<span data-ttu-id="ca3a2-116">Questo comando ottiene il profilo denominato ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ca3a2-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="ca3a2-117">Il comando passa quindi il profilo al cmdlet **Remove-AzTrafficManagerProfile** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="ca3a2-117">The command then passes that profile to the **Remove-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ca3a2-118">Questo cmdlet elimina tale profilo.</span><span class="sxs-lookup"><span data-stu-id="ca3a2-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="ca3a2-119">Il comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="ca3a2-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="ca3a2-120">Pertanto, non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="ca3a2-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ca3a2-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca3a2-121">PARAMETERS</span></span>

### <span data-ttu-id="ca3a2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca3a2-122">-DefaultProfile</span></span>
<span data-ttu-id="ca3a2-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca3a2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca3a2-124">-Force</span><span class="sxs-lookup"><span data-stu-id="ca3a2-124">-Force</span></span>
<span data-ttu-id="ca3a2-125">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ca3a2-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ca3a2-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca3a2-126">-Name</span></span>
<span data-ttu-id="ca3a2-127">Specifica il nome del profilo di Traffic Manager eliminato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca3a2-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="ca3a2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca3a2-128">-ResourceGroupName</span></span>
<span data-ttu-id="ca3a2-129">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ca3a2-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ca3a2-130">Questo cmdlet elimina un profilo di gestione traffico nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ca3a2-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ca3a2-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ca3a2-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="ca3a2-132">Specifica un oggetto **TrafficManagerProfile** da eliminare.</span><span class="sxs-lookup"><span data-stu-id="ca3a2-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="ca3a2-133">Per ottenere un oggetto **TrafficManagerProfile** , usa il cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="ca3a2-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="ca3a2-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ca3a2-134">-Confirm</span></span>
<span data-ttu-id="ca3a2-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca3a2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca3a2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca3a2-136">-WhatIf</span></span>
<span data-ttu-id="ca3a2-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca3a2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca3a2-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca3a2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca3a2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca3a2-139">CommonParameters</span></span>
<span data-ttu-id="ca3a2-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca3a2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca3a2-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca3a2-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca3a2-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca3a2-142">INPUTS</span></span>

### <span data-ttu-id="ca3a2-143">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ca3a2-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="ca3a2-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca3a2-144">OUTPUTS</span></span>

### <span data-ttu-id="ca3a2-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ca3a2-145">System.Boolean</span></span>

## <span data-ttu-id="ca3a2-146">Note</span><span class="sxs-lookup"><span data-stu-id="ca3a2-146">NOTES</span></span>

## <span data-ttu-id="ca3a2-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca3a2-147">RELATED LINKS</span></span>

[<span data-ttu-id="ca3a2-148">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ca3a2-148">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="ca3a2-149">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ca3a2-149">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="ca3a2-150">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ca3a2-150">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="ca3a2-151">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ca3a2-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="ca3a2-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ca3a2-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


