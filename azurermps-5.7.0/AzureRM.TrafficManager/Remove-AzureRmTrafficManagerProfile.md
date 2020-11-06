---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 459ede802e3a96805bb2c32e4e901592604f03b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514031"
---
# <span data-ttu-id="b1345-101">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b1345-101">Remove-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="b1345-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b1345-102">SYNOPSIS</span></span>
<span data-ttu-id="b1345-103">Elimina un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="b1345-103">Deletes a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1345-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1345-104">SYNTAX</span></span>

### <span data-ttu-id="b1345-105">Campi</span><span class="sxs-lookup"><span data-stu-id="b1345-105">Fields</span></span>
```
Remove-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1345-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="b1345-106">Object</span></span>
```
Remove-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1345-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1345-107">DESCRIPTION</span></span>
<span data-ttu-id="b1345-108">Il cmdlet **Remove-AzureRmTrafficManagerProfile** Elimina un profilo di Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="b1345-108">The **Remove-AzureRmTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="b1345-109">Specificare il profilo da eliminare usando i parametri *Name* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="b1345-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="b1345-110">In alternativa, puoi specificare un oggetto **TrafficManagerProfile** usando il parametro *TrafficManagerProfile* oppure puoi usare la pipeline.</span><span class="sxs-lookup"><span data-stu-id="b1345-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="b1345-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1345-111">EXAMPLES</span></span>

### <span data-ttu-id="b1345-112">Esempio 1: eliminare un profilo specificato per nome</span><span class="sxs-lookup"><span data-stu-id="b1345-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="b1345-113">Questo comando Elimina il profilo denominato ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b1345-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="b1345-114">Il comando richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="b1345-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="b1345-115">Esempio 2: eliminare un profilo tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="b1345-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="b1345-116">Questo comando ottiene il profilo denominato ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b1345-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="b1345-117">Il comando passa quindi il profilo al cmdlet **Remove-AzureRmTrafficManagerProfile** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="b1345-117">The command then passes that profile to the **Remove-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b1345-118">Questo cmdlet elimina tale profilo.</span><span class="sxs-lookup"><span data-stu-id="b1345-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="b1345-119">Il comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="b1345-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="b1345-120">Pertanto, non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="b1345-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b1345-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b1345-121">PARAMETERS</span></span>

### <span data-ttu-id="b1345-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1345-122">-DefaultProfile</span></span>
<span data-ttu-id="b1345-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b1345-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1345-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b1345-124">-Force</span></span>
<span data-ttu-id="b1345-125">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b1345-125">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1345-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1345-126">-Name</span></span>
<span data-ttu-id="b1345-127">Specifica il nome del profilo di Traffic Manager eliminato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1345-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1345-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1345-128">-ResourceGroupName</span></span>
<span data-ttu-id="b1345-129">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b1345-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="b1345-130">Questo cmdlet elimina un profilo di gestione traffico nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="b1345-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1345-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b1345-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="b1345-132">Specifica un oggetto **TrafficManagerProfile** da eliminare.</span><span class="sxs-lookup"><span data-stu-id="b1345-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="b1345-133">Per ottenere un oggetto **TrafficManagerProfile** , usa il cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="b1345-133">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: TrafficManagerProfile
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1345-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b1345-134">-Confirm</span></span>
<span data-ttu-id="b1345-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1345-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1345-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1345-136">-WhatIf</span></span>
<span data-ttu-id="b1345-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1345-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1345-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1345-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1345-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1345-139">CommonParameters</span></span>
<span data-ttu-id="b1345-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1345-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1345-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1345-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1345-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b1345-142">INPUTS</span></span>

### <span data-ttu-id="b1345-143">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b1345-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="b1345-144">Questo cmdlet accetta un oggetto **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="b1345-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="b1345-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1345-145">OUTPUTS</span></span>

### <span data-ttu-id="b1345-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="b1345-146">Boolean</span></span>
<span data-ttu-id="b1345-147">Questo cmdlet restituisce un valore di $True, se ha esito positivo o, se l'eliminazione non riesce, un valore di $False.</span><span class="sxs-lookup"><span data-stu-id="b1345-147">This cmdlet returns a value of $True, if it succeeds or, if the deletion fails, a value of $False.</span></span>

## <span data-ttu-id="b1345-148">Note</span><span class="sxs-lookup"><span data-stu-id="b1345-148">NOTES</span></span>

## <span data-ttu-id="b1345-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1345-149">RELATED LINKS</span></span>

[<span data-ttu-id="b1345-150">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b1345-150">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="b1345-151">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b1345-151">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="b1345-152">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b1345-152">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="b1345-153">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b1345-153">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="b1345-154">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b1345-154">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


