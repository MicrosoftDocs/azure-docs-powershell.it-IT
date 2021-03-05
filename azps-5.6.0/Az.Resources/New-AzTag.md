---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: b5f80abac4c114ab60dcb130f229265c4aafd78f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971789"
---
# <span data-ttu-id="acfc4-101">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="acfc4-101">New-AzTag</span></span>

## <span data-ttu-id="acfc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acfc4-102">SYNOPSIS</span></span>
<span data-ttu-id="acfc4-103">Crea un tag di Azure predefinito o aggiunge valori a un tag | Crea o aggiorna l'intero set di tag per una risorsa o un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="acfc4-103">Creates a predefined Azure tag or adds values to an existing tag | Creates or updates the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="acfc4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="acfc4-104">SYNTAX</span></span>

### <span data-ttu-id="acfc4-105">CreatePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="acfc4-105">CreatePredefinedTagParameterSet</span></span>

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acfc4-106">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="acfc4-106">CreateByResourceIdParameterSet</span></span>

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="acfc4-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="acfc4-107">DESCRIPTION</span></span>

<span data-ttu-id="acfc4-108">**CreatePredefinedTagSet:** il cmdlet **New-AzTag** crea un tag di Azure predefinito con un valore predefinito facoltativo.</span><span class="sxs-lookup"><span data-stu-id="acfc4-108">**CreatePredefinedTagSet**: The **New-AzTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="acfc4-109">È anche possibile usarla per aggiungere altri valori ai tag predefiniti esistenti.</span><span class="sxs-lookup"><span data-stu-id="acfc4-109">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="acfc4-110">Per creare un tag predefinito, immettere un nome tag univoco.</span><span class="sxs-lookup"><span data-stu-id="acfc4-110">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="acfc4-111">Per aggiungere un valore a un tag predefinito esistente, specificare il nome del tag esistente e il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="acfc4-111">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>
<span data-ttu-id="acfc4-112">Questo cmdlet restituisce un oggetto che rappresenta il tag nuovo o modificato con i relativi valori e il numero di risorse a cui è stato applicato.</span><span class="sxs-lookup"><span data-stu-id="acfc4-112">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>
<span data-ttu-id="acfc4-113">Il modulo Tag di Azure di cui fa parte **il nuovo AzTag** consente di gestire i tag di Azure predefiniti.</span><span class="sxs-lookup"><span data-stu-id="acfc4-113">The Azure Tags module that **New-AzTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="acfc4-114">Un tag di Azure è una coppia nome-valore che è possibile usare per categorizzare le risorse e i gruppi di risorse di Azure, ad esempio per reparto o centro di costo, oppure per tenere traccia di note o commenti sulle risorse e i gruppi.</span><span class="sxs-lookup"><span data-stu-id="acfc4-114">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="acfc4-115">È possibile definire e applicare i tag in un unico passaggio, ma i tag predefiniti consentono di definire nomi e valori standard, coerenti e prevedibili per i tag nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="acfc4-115">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="acfc4-116">Per applicare un tag predefinito a una risorsa o a un gruppo di risorse, usare il *parametro Tag* del cmdlet New-AzTag.</span><span class="sxs-lookup"><span data-stu-id="acfc4-116">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="acfc4-117">Per cercare gruppi di risorse con un nome tag o un nome e un valore specificati, usare il *parametro Tag* del cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="acfc4-117">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="acfc4-118">A ogni tag è stato specificato un nome.</span><span class="sxs-lookup"><span data-stu-id="acfc4-118">Every tag has a name.</span></span>
<span data-ttu-id="acfc4-119">I valori sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="acfc4-119">The values are optional.</span></span>
<span data-ttu-id="acfc4-120">Un tag predefinito di Azure può avere più valori, ma quando si applica il tag a una risorsa o a un gruppo di risorse, si applica il nome del tag e solo uno dei relativi valori.</span><span class="sxs-lookup"><span data-stu-id="acfc4-120">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="acfc4-121">Ad esempio, è possibile creare un tag Reparto predefinito con un valore per ogni reparto, ad esempio Finanze, Risorse umane e IT.</span><span class="sxs-lookup"><span data-stu-id="acfc4-121">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="acfc4-122">Quando si applica il tag Reparto a una risorsa, si applica un solo valore predefinito, ad esempio Finanze.</span><span class="sxs-lookup"><span data-stu-id="acfc4-122">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

<span data-ttu-id="acfc4-123">**CreateByResourceIdParameterSet:** il cmdlet **New-AzTag** con **un valore ResourceId** crea o aggiorna l'intero set di tag in una risorsa o una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="acfc4-123">**CreateByResourceIdParameterSet**: The **New-AzTag** cmdlet with a **ResourceId** creates or updates the entire set of tags on a resource or subscription.</span></span>
<span data-ttu-id="acfc4-124">Questa operazione consente di aggiungere o sostituire l'intero set di tag nella risorsa o nella sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="acfc4-124">This operation allows adding or replacing the entire set of tags on the specified resource or subscription.</span></span> <span data-ttu-id="acfc4-125">L'entità specificata può contenere al massimo 50 tag.</span><span class="sxs-lookup"><span data-stu-id="acfc4-125">The specified entity can have a maximum of 50 tags.</span></span>

## <span data-ttu-id="acfc4-126">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="acfc4-126">EXAMPLES</span></span>

### <span data-ttu-id="acfc4-127">Esempio 1: Creare un tag predefinito</span><span class="sxs-lookup"><span data-stu-id="acfc4-127">Example 1: Create a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

<span data-ttu-id="acfc4-128">Questo comando crea un tag predefinito denominato FY2015.</span><span class="sxs-lookup"><span data-stu-id="acfc4-128">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="acfc4-129">Questo tag non ha valori.</span><span class="sxs-lookup"><span data-stu-id="acfc4-129">This tag has no values.</span></span>
<span data-ttu-id="acfc4-130">È possibile applicare un tag senza valori a una risorsa o a un gruppo di risorse oppure usare **New-AzTag** per aggiungere valori al tag.</span><span class="sxs-lookup"><span data-stu-id="acfc4-130">You can apply a tag with no values to a resource or resource group, or use **New-AzTag** to add values to the tag.</span></span>
<span data-ttu-id="acfc4-131">È anche possibile specificare un valore quando si applica il tag alla risorsa o al gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="acfc4-131">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="acfc4-132">Esempio 2: Creare un tag predefinito con un valore</span><span class="sxs-lookup"><span data-stu-id="acfc4-132">Example 2: Create a predefined tag with a value</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="acfc4-133">Questo comando crea un tag predefinito denominato Reparto con il valore Finanze.</span><span class="sxs-lookup"><span data-stu-id="acfc4-133">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="acfc4-134">Esempio 3: Aggiungere un valore a un tag predefinito</span><span class="sxs-lookup"><span data-stu-id="acfc4-134">Example 3: Add a value to a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 
PS C:\>New-AzTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

<span data-ttu-id="acfc4-135">Questi comandi creano un tag predefinito denominato Reparto con due valori.</span><span class="sxs-lookup"><span data-stu-id="acfc4-135">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="acfc4-136">Se il nome del tag esiste, **New-AzTag** aggiunge il valore al tag esistente invece di crearne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="acfc4-136">If the tag name exists, **New-AzTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="acfc4-137">Esempio 4: Usare un tag predefinito</span><span class="sxs-lookup"><span data-stu-id="acfc4-137">Example 4: Use a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 
PS C:\>Set-AzResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
Name:      EngineerBlog
Location:  East US
Resources: 
            
  Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US
    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001 
PS C:\>Get-AzTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 
PS C:\>Get-AzResourceGroup -Tag @{Name="CostCenter"}
Name:      EngineerBlog
Location:  East US
Resources: 
     Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US

    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001
```

<span data-ttu-id="acfc4-138">I comandi di questo esempio creano e usano un tag predefinito.</span><span class="sxs-lookup"><span data-stu-id="acfc4-138">The commands in this example create and use a predefined tag.</span></span>

### <span data-ttu-id="acfc4-139">Esempio 5: Creare o aggiornare l'intero set di tag in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="acfc4-139">Example 5: Creates or updates the entire set of tags on a subscription</span></span>

```powershell
PS C:\>$Tags = @{"tagKey1"="tagValue1"; "tagKey2"="tagValue2"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId} -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

<span data-ttu-id="acfc4-140">Questo comando crea o aggiorna l'intero set di tag nell'abbonamento con {subId}.</span><span class="sxs-lookup"><span data-stu-id="acfc4-140">This command creates or updates the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="acfc4-141">Esempio 6: Creare o aggiornare l'intero set di tag in una risorsa</span><span class="sxs-lookup"><span data-stu-id="acfc4-141">Example 6: Creates or updates the entire set of tags on a resource</span></span>

```powershell
PS C:\>$Tags = @{"Dept"="Finance"; "Status"="Normal"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="acfc4-142">Questo comando crea o aggiorna l'intero set di tag della risorsa con {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="acfc4-142">This command creates or updates the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="acfc4-143">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acfc4-143">PARAMETERS</span></span>

### <span data-ttu-id="acfc4-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acfc4-144">-DefaultProfile</span></span>
<span data-ttu-id="acfc4-145">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="acfc4-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acfc4-146">-Name</span><span class="sxs-lookup"><span data-stu-id="acfc4-146">-Name</span></span>
<span data-ttu-id="acfc4-147">Specifica il nome del tag predefinito.</span><span class="sxs-lookup"><span data-stu-id="acfc4-147">Specifies the predefined tag name.</span></span>
<span data-ttu-id="acfc4-148">Per creare un nuovo tag predefinito, immettere un nome univoco.</span><span class="sxs-lookup"><span data-stu-id="acfc4-148">To create a new predefined tag, enter a unique name.</span></span>
<span data-ttu-id="acfc4-149">Per aggiungere un valore a un tag esistente, immettere il nome del tag esistente.</span><span class="sxs-lookup"><span data-stu-id="acfc4-149">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="acfc4-150">Se un tag predefinito esistente ha il nome specificato, **New-AzTag** aggiunge il valore specificato, se presente, al tag con quel nome invece di creare un nuovo tag.</span><span class="sxs-lookup"><span data-stu-id="acfc4-150">If an existing predefined tag has the specified name, **New-AzTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acfc4-151">-Value</span><span class="sxs-lookup"><span data-stu-id="acfc4-151">-Value</span></span>
<span data-ttu-id="acfc4-152">Specifica un valore di tag predefinito.</span><span class="sxs-lookup"><span data-stu-id="acfc4-152">Specifies a predefined tag value.</span></span>
<span data-ttu-id="acfc4-153">I tag predefiniti possono avere più valori, ma è possibile immettere un solo valore in ogni comando.</span><span class="sxs-lookup"><span data-stu-id="acfc4-153">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="acfc4-154">Questo parametro è facoltativo, perché i tag possono avere nomi senza valori.</span><span class="sxs-lookup"><span data-stu-id="acfc4-154">This parameter is optional, because tags can have names without values.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acfc4-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acfc4-155">-ResourceId</span></span>
<span data-ttu-id="acfc4-156">Identificatore di risorsa per l'entità contrassegnata.</span><span class="sxs-lookup"><span data-stu-id="acfc4-156">The resource identifier for the entity being tagged.</span></span> <span data-ttu-id="acfc4-157">Una risorsa, un gruppo di risorse o una sottoscrizione può essere contrassegnata.</span><span class="sxs-lookup"><span data-stu-id="acfc4-157">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acfc4-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="acfc4-158">-Tag</span></span>
<span data-ttu-id="acfc4-159">I tag da inserire nella risorsa.</span><span class="sxs-lookup"><span data-stu-id="acfc4-159">The tags to put on the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acfc4-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="acfc4-160">-Confirm</span></span>
<span data-ttu-id="acfc4-161">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acfc4-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acfc4-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acfc4-162">-WhatIf</span></span>
<span data-ttu-id="acfc4-163">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="acfc4-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acfc4-164">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="acfc4-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acfc4-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acfc4-165">CommonParameters</span></span>
<span data-ttu-id="acfc4-166">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acfc4-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acfc4-167">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="acfc4-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acfc4-168">INPUT</span><span class="sxs-lookup"><span data-stu-id="acfc4-168">INPUTS</span></span>

### <span data-ttu-id="acfc4-169">System.String</span><span class="sxs-lookup"><span data-stu-id="acfc4-169">System.String</span></span>

### <span data-ttu-id="acfc4-170">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="acfc4-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="acfc4-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="acfc4-171">OUTPUTS</span></span>

### <span data-ttu-id="acfc4-172">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="acfc4-172">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="acfc4-173">NOTE</span><span class="sxs-lookup"><span data-stu-id="acfc4-173">NOTES</span></span>

## <span data-ttu-id="acfc4-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="acfc4-174">RELATED LINKS</span></span>

[<span data-ttu-id="acfc4-175">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="acfc4-175">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="acfc4-176">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="acfc4-176">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="acfc4-177">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="acfc4-177">Update-AzTag</span></span>](./Update-AzTag.md)