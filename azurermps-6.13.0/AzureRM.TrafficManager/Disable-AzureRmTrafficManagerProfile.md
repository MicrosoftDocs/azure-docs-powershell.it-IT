---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/disable-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: e714caedb86bd647ccc0692c47233833bc2db867
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508988"
---
# <span data-ttu-id="c0f10-101">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c0f10-101">Disable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="c0f10-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c0f10-102">SYNOPSIS</span></span>
<span data-ttu-id="c0f10-103">Disabilita un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="c0f10-103">Disables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0f10-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0f10-104">SYNTAX</span></span>

### <span data-ttu-id="c0f10-105">Campi</span><span class="sxs-lookup"><span data-stu-id="c0f10-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0f10-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="c0f10-106">Object</span></span>
```
Disable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0f10-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0f10-107">DESCRIPTION</span></span>
<span data-ttu-id="c0f10-108">Il cmdlet **Disable-AzureRmTrafficManagerProfile Disabilita** un profilo di Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="c0f10-108">The **Disable-AzureRmTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="c0f10-109">Puoi specificare l'oggetto profile usando la pipeline o come valore di parametro.</span><span class="sxs-lookup"><span data-stu-id="c0f10-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="c0f10-110">In alternativa, puoi specificare il profilo usando i parametri *Name* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="c0f10-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="c0f10-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0f10-111">EXAMPLES</span></span>

### <span data-ttu-id="c0f10-112">Esempio 1: disabilitare un profilo specificato per nome</span><span class="sxs-lookup"><span data-stu-id="c0f10-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="c0f10-113">Questo comando Disabilita il profilo denominato ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c0f10-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="c0f10-114">Il comando richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="c0f10-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="c0f10-115">Esempio 2: disabilitare un profilo tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="c0f10-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="c0f10-116">Questo comando ottiene il profilo denominato ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c0f10-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="c0f10-117">Il comando passa quindi il profilo al cmdlet **Disable-AzureRmTrafficManagerProfile** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="c0f10-117">The command then passes that profile to the **Disable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c0f10-118">Questo cmdlet disabilita tale profilo.</span><span class="sxs-lookup"><span data-stu-id="c0f10-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="c0f10-119">Il comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="c0f10-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c0f10-120">Pertanto, non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="c0f10-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c0f10-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c0f10-121">PARAMETERS</span></span>

### <span data-ttu-id="c0f10-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0f10-122">-DefaultProfile</span></span>
<span data-ttu-id="c0f10-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c0f10-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0f10-124">-Force</span><span class="sxs-lookup"><span data-stu-id="c0f10-124">-Force</span></span>
<span data-ttu-id="c0f10-125">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c0f10-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c0f10-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="c0f10-126">-Name</span></span>
<span data-ttu-id="c0f10-127">Specifica il nome del profilo di Traffic Manager disabilitato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0f10-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="c0f10-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0f10-128">-ResourceGroupName</span></span>
<span data-ttu-id="c0f10-129">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c0f10-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="c0f10-130">Questo cmdlet disabilita un profilo di gestione traffico nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c0f10-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c0f10-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c0f10-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="c0f10-132">Specifica un oggetto **TrafficManagerProfile** da disabilitare.</span><span class="sxs-lookup"><span data-stu-id="c0f10-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="c0f10-133">Per ottenere un oggetto **TrafficManagerProfile** , usa il cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="c0f10-133">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="c0f10-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c0f10-134">-Confirm</span></span>
<span data-ttu-id="c0f10-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0f10-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0f10-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0f10-136">-WhatIf</span></span>
<span data-ttu-id="c0f10-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0f10-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0f10-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0f10-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0f10-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0f10-139">CommonParameters</span></span>
<span data-ttu-id="c0f10-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0f10-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0f10-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0f10-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0f10-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c0f10-142">INPUTS</span></span>

### <span data-ttu-id="c0f10-143">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c0f10-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="c0f10-144">Questo cmdlet accetta un oggetto **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="c0f10-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="c0f10-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0f10-145">OUTPUTS</span></span>

### <span data-ttu-id="c0f10-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c0f10-146">System.Boolean</span></span>

## <span data-ttu-id="c0f10-147">Note</span><span class="sxs-lookup"><span data-stu-id="c0f10-147">NOTES</span></span>

## <span data-ttu-id="c0f10-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0f10-148">RELATED LINKS</span></span>

[<span data-ttu-id="c0f10-149">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c0f10-149">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="c0f10-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c0f10-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="c0f10-151">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c0f10-151">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="c0f10-152">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c0f10-152">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="c0f10-153">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c0f10-153">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


