---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
ms.openlocfilehash: fc1370da73b9217c5f5f8b24705047f154b50f31
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202736"
---
# <span data-ttu-id="31798-101">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="31798-101">Disable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="31798-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31798-102">SYNOPSIS</span></span>
<span data-ttu-id="31798-103">Disabilita un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="31798-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="31798-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31798-104">SYNTAX</span></span>

### <span data-ttu-id="31798-105">Campi</span><span class="sxs-lookup"><span data-stu-id="31798-105">Fields</span></span>
```
Disable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31798-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="31798-106">Object</span></span>
```
Disable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31798-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31798-107">DESCRIPTION</span></span>
<span data-ttu-id="31798-108">Il cmdlet **Disable-AzTrafficManagerProfile Disabilita** un profilo di Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="31798-108">The **Disable-AzTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="31798-109">Puoi specificare l'oggetto profile usando la pipeline o come valore di parametro.</span><span class="sxs-lookup"><span data-stu-id="31798-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="31798-110">In alternativa, puoi specificare il profilo usando i parametri *Name* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="31798-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="31798-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31798-111">EXAMPLES</span></span>

### <span data-ttu-id="31798-112">Esempio 1: disabilitare un profilo specificato per nome</span><span class="sxs-lookup"><span data-stu-id="31798-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="31798-113">Questo comando Disabilita il profilo denominato ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="31798-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="31798-114">Il comando richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="31798-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="31798-115">Esempio 2: disabilitare un profilo tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="31798-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerProfile -Force
```

<span data-ttu-id="31798-116">Questo comando ottiene il profilo denominato ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="31798-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="31798-117">Il comando passa quindi il profilo al cmdlet **Disable-AzTrafficManagerProfile** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="31798-117">The command then passes that profile to the **Disable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="31798-118">Questo cmdlet disabilita tale profilo.</span><span class="sxs-lookup"><span data-stu-id="31798-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="31798-119">Il comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="31798-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="31798-120">Pertanto, non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="31798-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="31798-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31798-121">PARAMETERS</span></span>

### <span data-ttu-id="31798-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31798-122">-DefaultProfile</span></span>
<span data-ttu-id="31798-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31798-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31798-124">-Force</span><span class="sxs-lookup"><span data-stu-id="31798-124">-Force</span></span>
<span data-ttu-id="31798-125">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="31798-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="31798-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="31798-126">-Name</span></span>
<span data-ttu-id="31798-127">Specifica il nome del profilo di Traffic Manager disabilitato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31798-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="31798-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31798-128">-ResourceGroupName</span></span>
<span data-ttu-id="31798-129">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="31798-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="31798-130">Questo cmdlet disabilita un profilo di gestione traffico nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="31798-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="31798-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="31798-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="31798-132">Specifica un oggetto **TrafficManagerProfile** da disabilitare.</span><span class="sxs-lookup"><span data-stu-id="31798-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="31798-133">Per ottenere un oggetto **TrafficManagerProfile** , usa il cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="31798-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="31798-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="31798-134">-Confirm</span></span>
<span data-ttu-id="31798-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31798-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31798-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31798-136">-WhatIf</span></span>
<span data-ttu-id="31798-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31798-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31798-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31798-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31798-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31798-139">CommonParameters</span></span>
<span data-ttu-id="31798-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31798-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31798-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31798-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31798-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31798-142">INPUTS</span></span>

### <span data-ttu-id="31798-143">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="31798-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="31798-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31798-144">OUTPUTS</span></span>

### <span data-ttu-id="31798-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="31798-145">System.Boolean</span></span>

## <span data-ttu-id="31798-146">Note</span><span class="sxs-lookup"><span data-stu-id="31798-146">NOTES</span></span>

## <span data-ttu-id="31798-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31798-147">RELATED LINKS</span></span>

[<span data-ttu-id="31798-148">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="31798-148">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="31798-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="31798-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="31798-150">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="31798-150">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="31798-151">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="31798-151">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="31798-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="31798-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


