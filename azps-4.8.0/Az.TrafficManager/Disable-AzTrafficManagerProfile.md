---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
ms.openlocfilehash: fc1370da73b9217c5f5f8b24705047f154b50f31
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032792"
---
# <span data-ttu-id="f4fca-101">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f4fca-101">Disable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="f4fca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4fca-102">SYNOPSIS</span></span>
<span data-ttu-id="f4fca-103">Disabilita un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="f4fca-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="f4fca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4fca-104">SYNTAX</span></span>

### <span data-ttu-id="f4fca-105">Campi</span><span class="sxs-lookup"><span data-stu-id="f4fca-105">Fields</span></span>
```
Disable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4fca-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="f4fca-106">Object</span></span>
```
Disable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4fca-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4fca-107">DESCRIPTION</span></span>
<span data-ttu-id="f4fca-108">Il cmdlet **Disable-AzTrafficManagerProfile Disabilita** un profilo di Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="f4fca-108">The **Disable-AzTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="f4fca-109">Puoi specificare l'oggetto profile usando la pipeline o come valore di parametro.</span><span class="sxs-lookup"><span data-stu-id="f4fca-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="f4fca-110">In alternativa, puoi specificare il profilo usando i parametri *Name* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="f4fca-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="f4fca-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4fca-111">EXAMPLES</span></span>

### <span data-ttu-id="f4fca-112">Esempio 1: disabilitare un profilo specificato per nome</span><span class="sxs-lookup"><span data-stu-id="f4fca-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="f4fca-113">Questo comando Disabilita il profilo denominato ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f4fca-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="f4fca-114">Il comando richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="f4fca-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="f4fca-115">Esempio 2: disabilitare un profilo tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="f4fca-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerProfile -Force
```

<span data-ttu-id="f4fca-116">Questo comando ottiene il profilo denominato ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f4fca-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="f4fca-117">Il comando passa quindi il profilo al cmdlet **Disable-AzTrafficManagerProfile** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="f4fca-117">The command then passes that profile to the **Disable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f4fca-118">Questo cmdlet disabilita tale profilo.</span><span class="sxs-lookup"><span data-stu-id="f4fca-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="f4fca-119">Il comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="f4fca-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="f4fca-120">Pertanto, non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="f4fca-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f4fca-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4fca-121">PARAMETERS</span></span>

### <span data-ttu-id="f4fca-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4fca-122">-DefaultProfile</span></span>
<span data-ttu-id="f4fca-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4fca-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4fca-124">-Force</span><span class="sxs-lookup"><span data-stu-id="f4fca-124">-Force</span></span>
<span data-ttu-id="f4fca-125">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f4fca-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f4fca-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4fca-126">-Name</span></span>
<span data-ttu-id="f4fca-127">Specifica il nome del profilo di Traffic Manager disabilitato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4fca-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="f4fca-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4fca-128">-ResourceGroupName</span></span>
<span data-ttu-id="f4fca-129">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f4fca-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="f4fca-130">Questo cmdlet disabilita un profilo di gestione traffico nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="f4fca-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f4fca-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f4fca-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="f4fca-132">Specifica un oggetto **TrafficManagerProfile** da disabilitare.</span><span class="sxs-lookup"><span data-stu-id="f4fca-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="f4fca-133">Per ottenere un oggetto **TrafficManagerProfile** , usa il cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f4fca-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="f4fca-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f4fca-134">-Confirm</span></span>
<span data-ttu-id="f4fca-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4fca-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4fca-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4fca-136">-WhatIf</span></span>
<span data-ttu-id="f4fca-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4fca-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4fca-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4fca-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4fca-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4fca-139">CommonParameters</span></span>
<span data-ttu-id="f4fca-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4fca-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4fca-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4fca-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4fca-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4fca-142">INPUTS</span></span>

### <span data-ttu-id="f4fca-143">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f4fca-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="f4fca-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4fca-144">OUTPUTS</span></span>

### <span data-ttu-id="f4fca-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4fca-145">System.Boolean</span></span>

## <span data-ttu-id="f4fca-146">Note</span><span class="sxs-lookup"><span data-stu-id="f4fca-146">NOTES</span></span>

## <span data-ttu-id="f4fca-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4fca-147">RELATED LINKS</span></span>

[<span data-ttu-id="f4fca-148">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f4fca-148">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="f4fca-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f4fca-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="f4fca-150">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f4fca-150">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="f4fca-151">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f4fca-151">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="f4fca-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f4fca-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


