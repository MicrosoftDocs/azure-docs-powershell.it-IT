---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 05ee8609c7ee8bccd435e6e861f67829b9988d74
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188897"
---
# <span data-ttu-id="262f7-101">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="262f7-101">Remove-AzTag</span></span>

## <span data-ttu-id="262f7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="262f7-102">SYNOPSIS</span></span>
<span data-ttu-id="262f7-103">Elimina i tag o i valori di Azure predefiniti | Elimina l'intero set di tag in una risorsa o un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="262f7-103">Deletes predefined Azure tags or values | Deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="262f7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="262f7-104">SYNTAX</span></span>

### <span data-ttu-id="262f7-105">RemovePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="262f7-105">RemovePredefinedTagParameterSet</span></span>

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="262f7-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="262f7-106">RemoveByResourceIdParameterSet</span></span>

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="262f7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="262f7-107">DESCRIPTION</span></span>

<span data-ttu-id="262f7-108">**RemovePredefinedTagSet** : il cmdlet **Remove-AzTag** Elimina i tag e i valori di Azure predefiniti dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="262f7-108">**RemovePredefinedTagSet** : The **Remove-AzTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="262f7-109">Per eliminare valori particolari da un tag predefinito, usare il parametro *value* .</span><span class="sxs-lookup"><span data-stu-id="262f7-109">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="262f7-110">Per impostazione predefinita, **Remove-AzTag** Elimina il tag specificato e tutti i relativi valori. Non è possibile eliminare un tag o un valore attualmente applicato a una risorsa o a un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="262f7-110">By default, **Remove-AzTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="262f7-111">Prima di usare **Remove-AzTag** , usa il parametro *tag* del cmdlet Set-AzResourceGroup per eliminare il tag o i valori dal gruppo Resource o Resource.</span><span class="sxs-lookup"><span data-stu-id="262f7-111">Before using **Remove-AzTag** , use the *Tag* parameter of the Set-AzResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="262f7-112">Il modulo tag di Azure che **rimuove-AzTag** fa parte di può aiutare a gestire i tag di Azure predefiniti.</span><span class="sxs-lookup"><span data-stu-id="262f7-112">The Azure Tags module that **Remove-AzTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="262f7-113">Un tag Azure è una coppia nome-valore che puoi usare per categorizzare le risorse e i gruppi di risorse di Azure, ad esempio per reparto o centro costo, oppure per tenere traccia di note o commenti relativi a risorse e gruppi.</span><span class="sxs-lookup"><span data-stu-id="262f7-113">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="262f7-114">È possibile definire e applicare i tag in un singolo passaggio, ma i tag predefiniti consentono di stabilire nomi e valori standard, coerenti e prevedibili per i tag nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="262f7-114">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

<span data-ttu-id="262f7-115">**RemoveByResourceIdParameterSet** : il cmdlet **Remove-AzTag** con un **resourceId** Elimina l'intero set di tag in una risorsa o un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="262f7-115">**RemoveByResourceIdParameterSet** : The **Remove-AzTag** cmdlet with a **ResourceId** deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="262f7-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="262f7-116">EXAMPLES</span></span>

### <span data-ttu-id="262f7-117">Esempio 1: eliminare un tag predefinito</span><span class="sxs-lookup"><span data-stu-id="262f7-117">Example 1: Delete a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

<span data-ttu-id="262f7-118">Questo comando Elimina il nome del tag predefinito Department e tutti i relativi valori.</span><span class="sxs-lookup"><span data-stu-id="262f7-118">This command deletes the predefined tag named Department and all of its values.</span></span>
<span data-ttu-id="262f7-119">Se il tag è stato applicato a qualsiasi risorsa o gruppo di risorse, il comando non riesce.</span><span class="sxs-lookup"><span data-stu-id="262f7-119">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="262f7-120">Esempio 2: eliminare un valore da un tag predefinito</span><span class="sxs-lookup"><span data-stu-id="262f7-120">Example 2: Delete a value from a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

<span data-ttu-id="262f7-121">Questo comando Elimina il valore HumanResources dal tag Department predefinito.</span><span class="sxs-lookup"><span data-stu-id="262f7-121">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="262f7-122">Il tag non viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="262f7-122">It does not delete the tag.</span></span>
<span data-ttu-id="262f7-123">Se il valore è stato applicato a tutte le risorse o ai gruppi di risorse, il comando non riesce.</span><span class="sxs-lookup"><span data-stu-id="262f7-123">If the value has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="262f7-124">Esempio 3: Elimina l'intero set di tag in una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="262f7-124">Example 3: Deletes the entire set of tags on a subscription</span></span>

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

<span data-ttu-id="262f7-125">Questo comando Elimina l'intero set di tag nell'abbonamento con {subId}.</span><span class="sxs-lookup"><span data-stu-id="262f7-125">This command deletes the entire set of tags on the subscription with {subId}.</span></span> <span data-ttu-id="262f7-126">Non restituirà l'oggetto eliminato se non viene passato "-PassThru".</span><span class="sxs-lookup"><span data-stu-id="262f7-126">It will not return the object deleted if not passing in "-PassThru".</span></span>

### <span data-ttu-id="262f7-127">Esempio 4: Elimina l'intero set di tag in una risorsa</span><span class="sxs-lookup"><span data-stu-id="262f7-127">Example 4: Deletes the entire set of tags on a resource</span></span>

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -PassThru

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="262f7-128">Questo comando Elimina l'intero set di tag nella risorsa con {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="262f7-128">This command deletes the entire set of tags on the resource with {resourceId}.</span></span> <span data-ttu-id="262f7-129">Restituisce il oject eliminato quando passa "-PassThru".</span><span class="sxs-lookup"><span data-stu-id="262f7-129">It returns the deleted oject when passing in "-PassThru".</span></span>

## <span data-ttu-id="262f7-130">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="262f7-130">PARAMETERS</span></span>

### <span data-ttu-id="262f7-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="262f7-131">-DefaultProfile</span></span>
<span data-ttu-id="262f7-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="262f7-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="262f7-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="262f7-133">-Name</span></span>
<span data-ttu-id="262f7-134">Specifica il nome del tag predefinito da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="262f7-134">Specifies the Name of the predefined tag to remove.</span></span>
<span data-ttu-id="262f7-135">Per impostazione predefinita, **Remove-AzTag** rimuove il tag specificato e tutti i relativi valori.</span><span class="sxs-lookup"><span data-stu-id="262f7-135">By default, **Remove-AzTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="262f7-136">Per eliminare i valori selezionati, ma non eliminare il tag, usa il parametro *value* .</span><span class="sxs-lookup"><span data-stu-id="262f7-136">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="262f7-137">-Valore</span><span class="sxs-lookup"><span data-stu-id="262f7-137">-Value</span></span>
<span data-ttu-id="262f7-138">Elimina i valori specificati dal tag predefinito, ma non elimina il tag.</span><span class="sxs-lookup"><span data-stu-id="262f7-138">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

```yaml
Type: System.String[]
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="262f7-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="262f7-139">-ResourceId</span></span>
<span data-ttu-id="262f7-140">Identificatore delle risorse per l'entità Tagged.</span><span class="sxs-lookup"><span data-stu-id="262f7-140">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="262f7-141">Una risorsa, un gruppo di risorse o un abbonamento possono essere contrassegnati.</span><span class="sxs-lookup"><span data-stu-id="262f7-141">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="262f7-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="262f7-142">-PassThru</span></span>
<span data-ttu-id="262f7-143">Restituisce un oggetto che rappresenta il tag eliminato o il tag risultante con il valore deleted.</span><span class="sxs-lookup"><span data-stu-id="262f7-143">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="262f7-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="262f7-144">-Confirm</span></span>
<span data-ttu-id="262f7-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="262f7-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="262f7-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="262f7-146">-WhatIf</span></span>
<span data-ttu-id="262f7-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="262f7-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="262f7-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="262f7-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="262f7-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="262f7-149">CommonParameters</span></span>
<span data-ttu-id="262f7-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="262f7-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="262f7-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="262f7-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="262f7-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="262f7-152">INPUTS</span></span>

### <span data-ttu-id="262f7-153">System. String</span><span class="sxs-lookup"><span data-stu-id="262f7-153">System.String</span></span>

### <span data-ttu-id="262f7-154">System. String []</span><span class="sxs-lookup"><span data-stu-id="262f7-154">System.String[]</span></span>

### <span data-ttu-id="262f7-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="262f7-155">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="262f7-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="262f7-156">OUTPUTS</span></span>

### <span data-ttu-id="262f7-157">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. Model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="262f7-157">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="262f7-158">Note</span><span class="sxs-lookup"><span data-stu-id="262f7-158">NOTES</span></span>

## <span data-ttu-id="262f7-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="262f7-159">RELATED LINKS</span></span>

[<span data-ttu-id="262f7-160">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="262f7-160">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="262f7-161">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="262f7-161">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="262f7-162">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="262f7-162">Update-AzTag</span></span>](./Update-AzTag.md)