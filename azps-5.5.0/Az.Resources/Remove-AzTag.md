---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 22a43739ec63f8287ce51c4c4f4a125b4e5b1c65
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189222"
---
# <span data-ttu-id="0635f-101">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="0635f-101">Remove-AzTag</span></span>

## <span data-ttu-id="0635f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0635f-102">SYNOPSIS</span></span>
<span data-ttu-id="0635f-103">Elimina i tag o i valori predefiniti di Azure | Elimina l'intero set di tag per una risorsa o un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="0635f-103">Deletes predefined Azure tags or values | Deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="0635f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0635f-104">SYNTAX</span></span>

### <span data-ttu-id="0635f-105">RemovePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="0635f-105">RemovePredefinedTagParameterSet</span></span>

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0635f-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0635f-106">RemoveByResourceIdParameterSet</span></span>

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="0635f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0635f-107">DESCRIPTION</span></span>

<span data-ttu-id="0635f-108">**RemovePredefinedTagSet:** il cmdlet **Remove-AzTag** elimina i tag e i valori predefiniti di Azure dalla sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="0635f-108">**RemovePredefinedTagSet**: The **Remove-AzTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="0635f-109">Per eliminare determinati valori da un tag predefinito, usare il *parametro Value.*</span><span class="sxs-lookup"><span data-stu-id="0635f-109">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="0635f-110">Per impostazione predefinita, **Remove-AzTag** elimina il tag specificato e tutti i relativi valori. Non è possibile eliminare un tag o un valore attualmente applicato a una risorsa o a un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0635f-110">By default, **Remove-AzTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="0635f-111">Prima di **usare Remove-AzTag,** usare il parametro *Tag* del cmdlet Set-AzResourceGroup per eliminare il tag o i valori dalla risorsa o dal gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0635f-111">Before using **Remove-AzTag**, use the *Tag* parameter of the Set-AzResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="0635f-112">Il modulo Tag di Azure **di cui remove-AzTag** fa parte consente di gestire i tag di Azure predefiniti.</span><span class="sxs-lookup"><span data-stu-id="0635f-112">The Azure Tags module that **Remove-AzTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="0635f-113">Un tag di Azure è una coppia nome-valore che è possibile usare per categorizzare le risorse e i gruppi di risorse di Azure, ad esempio per reparto o centro di costo, oppure per tenere traccia di note o commenti sulle risorse e i gruppi.</span><span class="sxs-lookup"><span data-stu-id="0635f-113">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="0635f-114">È possibile definire e applicare tag in un unico passaggio, ma i tag predefiniti consentono di definire nomi e valori standard, coerenti e prevedibili per i tag nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="0635f-114">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

<span data-ttu-id="0635f-115">**RemoveByResourceIdParameterSet:** il cmdlet **Remove-AzTag** con **un valore ResourceId** elimina l'intero set di tag per una risorsa o una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="0635f-115">**RemoveByResourceIdParameterSet**: The **Remove-AzTag** cmdlet with a **ResourceId** deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="0635f-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0635f-116">EXAMPLES</span></span>

### <span data-ttu-id="0635f-117">Esempio 1: Eliminare un tag predefinito</span><span class="sxs-lookup"><span data-stu-id="0635f-117">Example 1: Delete a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

<span data-ttu-id="0635f-118">Questo comando elimina il tag predefinito denominato Reparto e tutti i relativi valori.</span><span class="sxs-lookup"><span data-stu-id="0635f-118">This command deletes the predefined tag named Department and all of its values.</span></span>
<span data-ttu-id="0635f-119">Se il tag è stato applicato a qualsiasi risorsa o gruppo di risorse, il comando non riesce.</span><span class="sxs-lookup"><span data-stu-id="0635f-119">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="0635f-120">Esempio 2: Eliminare un valore da un tag predefinito</span><span class="sxs-lookup"><span data-stu-id="0635f-120">Example 2: Delete a value from a predefined tag</span></span>
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

<span data-ttu-id="0635f-121">Questo comando elimina il valore HumanResources dal tag department predefinito.</span><span class="sxs-lookup"><span data-stu-id="0635f-121">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="0635f-122">Il tag non viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="0635f-122">It does not delete the tag.</span></span>
<span data-ttu-id="0635f-123">Se il valore è stato applicato a qualsiasi risorsa o gruppo di risorse, il comando non riesce.</span><span class="sxs-lookup"><span data-stu-id="0635f-123">If the value has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="0635f-124">Esempio 3: Elimina l'intero set di tag in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="0635f-124">Example 3: Deletes the entire set of tags on a subscription</span></span>

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

<span data-ttu-id="0635f-125">Questo comando elimina l'intero set di tag nell'abbonamento con {subId}.</span><span class="sxs-lookup"><span data-stu-id="0635f-125">This command deletes the entire set of tags on the subscription with {subId}.</span></span> <span data-ttu-id="0635f-126">Non restituirà l'oggetto eliminato se non passa "-PassThru".</span><span class="sxs-lookup"><span data-stu-id="0635f-126">It will not return the object deleted if not passing in "-PassThru".</span></span>

### <span data-ttu-id="0635f-127">Esempio 4: Eliminare l'intero set di tag in una risorsa</span><span class="sxs-lookup"><span data-stu-id="0635f-127">Example 4: Deletes the entire set of tags on a resource</span></span>

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

<span data-ttu-id="0635f-128">Questo comando elimina l'intero set di tag per la risorsa con {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="0635f-128">This command deletes the entire set of tags on the resource with {resourceId}.</span></span> <span data-ttu-id="0635f-129">Restituisce l'oggetto eliminato quando si passa "-PassThru".</span><span class="sxs-lookup"><span data-stu-id="0635f-129">It returns the deleted oject when passing in "-PassThru".</span></span>

## <span data-ttu-id="0635f-130">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0635f-130">PARAMETERS</span></span>

### <span data-ttu-id="0635f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0635f-131">-DefaultProfile</span></span>
<span data-ttu-id="0635f-132">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0635f-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0635f-133">-Name</span><span class="sxs-lookup"><span data-stu-id="0635f-133">-Name</span></span>
<span data-ttu-id="0635f-134">Specifica il nome del tag predefinito da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="0635f-134">Specifies the Name of the predefined tag to remove.</span></span>
<span data-ttu-id="0635f-135">Per impostazione predefinita, **Remove-AzTag** rimuove il tag specificato e tutti i relativi valori.</span><span class="sxs-lookup"><span data-stu-id="0635f-135">By default, **Remove-AzTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="0635f-136">Per eliminare i valori selezionati, ma non eliminare il tag, usare il *parametro* Value.</span><span class="sxs-lookup"><span data-stu-id="0635f-136">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

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

### <span data-ttu-id="0635f-137">-Value</span><span class="sxs-lookup"><span data-stu-id="0635f-137">-Value</span></span>
<span data-ttu-id="0635f-138">Elimina i valori specificati dal tag predefinito, ma non elimina il tag.</span><span class="sxs-lookup"><span data-stu-id="0635f-138">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

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

### <span data-ttu-id="0635f-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0635f-139">-ResourceId</span></span>
<span data-ttu-id="0635f-140">Identificatore di risorsa per l'entità con tag.</span><span class="sxs-lookup"><span data-stu-id="0635f-140">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="0635f-141">Una risorsa, un gruppo di risorse o una sottoscrizione può essere contrassegnata.</span><span class="sxs-lookup"><span data-stu-id="0635f-141">A resource, a resource group or a subscription may be tagged.</span></span>

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

### <span data-ttu-id="0635f-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0635f-142">-PassThru</span></span>
<span data-ttu-id="0635f-143">Restituisce un oggetto che rappresenta il tag eliminato o il tag risultante con valore eliminato.</span><span class="sxs-lookup"><span data-stu-id="0635f-143">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

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

### <span data-ttu-id="0635f-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0635f-144">-Confirm</span></span>
<span data-ttu-id="0635f-145">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0635f-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0635f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0635f-146">-WhatIf</span></span>
<span data-ttu-id="0635f-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0635f-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0635f-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0635f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0635f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0635f-149">CommonParameters</span></span>
<span data-ttu-id="0635f-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0635f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0635f-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0635f-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0635f-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="0635f-152">INPUTS</span></span>

### <span data-ttu-id="0635f-153">System.String</span><span class="sxs-lookup"><span data-stu-id="0635f-153">System.String</span></span>

### <span data-ttu-id="0635f-154">System.String[]</span><span class="sxs-lookup"><span data-stu-id="0635f-154">System.String[]</span></span>

### <span data-ttu-id="0635f-155">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0635f-155">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0635f-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0635f-156">OUTPUTS</span></span>

### <span data-ttu-id="0635f-157">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="0635f-157">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="0635f-158">NOTE</span><span class="sxs-lookup"><span data-stu-id="0635f-158">NOTES</span></span>

## <span data-ttu-id="0635f-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0635f-159">RELATED LINKS</span></span>

[<span data-ttu-id="0635f-160">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="0635f-160">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="0635f-161">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="0635f-161">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="0635f-162">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="0635f-162">Update-AzTag</span></span>](./Update-AzTag.md)