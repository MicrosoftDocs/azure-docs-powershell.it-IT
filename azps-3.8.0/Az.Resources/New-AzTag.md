---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 176328452c123c3d3cada88940efcdadf88943e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864623"
---
# <span data-ttu-id="f60ae-101">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="f60ae-101">New-AzTag</span></span>

## <span data-ttu-id="f60ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f60ae-102">SYNOPSIS</span></span>
<span data-ttu-id="f60ae-103">Crea un tag Azure predefinito o aggiunge valori a un tag esistente | Crea o aggiorna l'intero set di tag in una risorsa o un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f60ae-103">Creates a predefined Azure tag or adds values to an existing tag | Creates or updates the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="f60ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f60ae-104">SYNTAX</span></span>

### <span data-ttu-id="f60ae-105">CreatePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="f60ae-105">CreatePredefinedTagParameterSet</span></span>

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f60ae-106">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f60ae-106">CreateByResourceIdParameterSet</span></span>

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="f60ae-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f60ae-107">DESCRIPTION</span></span>

<span data-ttu-id="f60ae-108">**CreatePredefinedTagSet** : il cmdlet **New-AzTag** crea un tag Azure predefinito con un valore predefinito facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f60ae-108">**CreatePredefinedTagSet** : The **New-AzTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="f60ae-109">Puoi anche usarla per aggiungere altri valori ai tag predefiniti esistenti.</span><span class="sxs-lookup"><span data-stu-id="f60ae-109">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="f60ae-110">Per creare un tag predefinito, immetti un nome di tag univoco.</span><span class="sxs-lookup"><span data-stu-id="f60ae-110">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="f60ae-111">Per aggiungere un valore a un tag predefinito esistente, specificare il nome del tag esistente e il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="f60ae-111">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>
<span data-ttu-id="f60ae-112">Questo cmdlet restituisce un oggetto che rappresenta il tag New o Modified con i relativi valori e il numero di risorse a cui è stato applicato.</span><span class="sxs-lookup"><span data-stu-id="f60ae-112">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>
<span data-ttu-id="f60ae-113">Il modulo Tag Azure di cui fa parte **New-AzTag** può aiutarti a gestire i tag di Azure predefiniti.</span><span class="sxs-lookup"><span data-stu-id="f60ae-113">The Azure Tags module that **New-AzTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="f60ae-114">Un tag Azure è una coppia nome-valore che puoi usare per categorizzare le risorse e i gruppi di risorse di Azure, ad esempio per reparto o centro costo, oppure per tenere traccia di note o commenti relativi a risorse e gruppi.</span><span class="sxs-lookup"><span data-stu-id="f60ae-114">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="f60ae-115">È possibile definire e applicare i tag in un singolo passaggio, ma i tag predefiniti consentono di stabilire nomi e valori standard, coerenti e prevedibili per i tag nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f60ae-115">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="f60ae-116">Per applicare un contrassegno predefinito a una risorsa o a un gruppo di risorse, usare il parametro *tag* del cmdlet New-AzTag.</span><span class="sxs-lookup"><span data-stu-id="f60ae-116">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="f60ae-117">Per cercare gruppi di risorse con un nome di tag o un nome e un valore specificati, usare il parametro *tag* del cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f60ae-117">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="f60ae-118">Ogni tag ha un nome.</span><span class="sxs-lookup"><span data-stu-id="f60ae-118">Every tag has a name.</span></span>
<span data-ttu-id="f60ae-119">I valori sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="f60ae-119">The values are optional.</span></span>
<span data-ttu-id="f60ae-120">Un tag Azure predefinito può avere più valori, ma quando si applica il contrassegno a una risorsa o a un gruppo di risorse, è possibile applicare il nome del tag e solo uno dei relativi valori.</span><span class="sxs-lookup"><span data-stu-id="f60ae-120">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="f60ae-121">Ad esempio, puoi creare un tag di reparto predefinito con un valore per ogni reparto, come finanza, risorse umane e IT.</span><span class="sxs-lookup"><span data-stu-id="f60ae-121">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="f60ae-122">Quando si applica il tag Department a una risorsa, si applica un solo valore predefinito, ad esempio Finance.</span><span class="sxs-lookup"><span data-stu-id="f60ae-122">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

<span data-ttu-id="f60ae-123">**CreateByResourceIdParameterSet** : il cmdlet **New-AzTag** con un **resourceId** crea o aggiorna l'intero set di tag in una risorsa o un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f60ae-123">**CreateByResourceIdParameterSet** : The **New-AzTag** cmdlet with a **ResourceId** creates or updates the entire set of tags on a resource or subscription.</span></span>
<span data-ttu-id="f60ae-124">Questa operazione consente di aggiungere o sostituire l'intero set di tag nella risorsa o nell'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="f60ae-124">This operation allows adding or replacing the entire set of tags on the specified resource or subscription.</span></span> <span data-ttu-id="f60ae-125">L'entità specificata può avere un massimo di 50 contrassegni.</span><span class="sxs-lookup"><span data-stu-id="f60ae-125">The specified entity can have a maximum of 50 tags.</span></span>

## <span data-ttu-id="f60ae-126">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f60ae-126">EXAMPLES</span></span>

### <span data-ttu-id="f60ae-127">Esempio 1: creare un tag predefinito</span><span class="sxs-lookup"><span data-stu-id="f60ae-127">Example 1: Create a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

<span data-ttu-id="f60ae-128">Questo comando crea un tag predefinito denominato FY2015.</span><span class="sxs-lookup"><span data-stu-id="f60ae-128">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="f60ae-129">Questo tag non contiene valori.</span><span class="sxs-lookup"><span data-stu-id="f60ae-129">This tag has no values.</span></span>
<span data-ttu-id="f60ae-130">Puoi applicare un contrassegno senza valori a una risorsa o a un gruppo di risorse oppure usare **New-AzTag** per aggiungere valori al tag.</span><span class="sxs-lookup"><span data-stu-id="f60ae-130">You can apply a tag with no values to a resource or resource group, or use **New-AzTag** to add values to the tag.</span></span>
<span data-ttu-id="f60ae-131">Puoi anche specificare un valore quando applichi il tag al gruppo di risorse o risorse.</span><span class="sxs-lookup"><span data-stu-id="f60ae-131">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="f60ae-132">Esempio 2: creare un tag predefinito con un valore</span><span class="sxs-lookup"><span data-stu-id="f60ae-132">Example 2: Create a predefined tag with a value</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="f60ae-133">Questo comando crea un tag predefinito denominato Department con un valore di Finance.</span><span class="sxs-lookup"><span data-stu-id="f60ae-133">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="f60ae-134">Esempio 3: aggiungere un valore a un tag predefinito</span><span class="sxs-lookup"><span data-stu-id="f60ae-134">Example 3: Add a value to a predefined tag</span></span>
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

<span data-ttu-id="f60ae-135">Questi comandi creano un tag predefinito denominato Department con due valori.</span><span class="sxs-lookup"><span data-stu-id="f60ae-135">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="f60ae-136">Se il nome del tag esiste, **New-AzTag** aggiunge il valore al tag esistente anziché crearne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="f60ae-136">If the tag name exists, **New-AzTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="f60ae-137">Esempio 4: usare un tag predefinito</span><span class="sxs-lookup"><span data-stu-id="f60ae-137">Example 4: Use a predefined tag</span></span>
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

<span data-ttu-id="f60ae-138">I comandi in questo esempio creano e usano un tag predefinito.</span><span class="sxs-lookup"><span data-stu-id="f60ae-138">The commands in this example create and use a predefined tag.</span></span>

### <span data-ttu-id="f60ae-139">Esempio 5: crea o aggiorna l'intero set di tag in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="f60ae-139">Example 5: Creates or updates the entire set of tags on a subscription</span></span>

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

<span data-ttu-id="f60ae-140">Questo comando crea o aggiorna l'intero set di tag nell'abbonamento con {subId}.</span><span class="sxs-lookup"><span data-stu-id="f60ae-140">This command creates or updates the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="f60ae-141">Esempio 6: crea o aggiorna l'intero set di tag in una risorsa</span><span class="sxs-lookup"><span data-stu-id="f60ae-141">Example 6: Creates or updates the entire set of tags on a resource</span></span>

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

<span data-ttu-id="f60ae-142">Questo comando crea o aggiorna l'intero set di tag nella risorsa con {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="f60ae-142">This command creates or updates the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="f60ae-143">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f60ae-143">PARAMETERS</span></span>

### <span data-ttu-id="f60ae-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f60ae-144">-DefaultProfile</span></span>
<span data-ttu-id="f60ae-145">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f60ae-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f60ae-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="f60ae-146">-Name</span></span>
<span data-ttu-id="f60ae-147">Specifica il nome del tag predefinito.</span><span class="sxs-lookup"><span data-stu-id="f60ae-147">Specifies the predefined tag name.</span></span>
<span data-ttu-id="f60ae-148">Per creare un nuovo tag predefinito, immettere un nome univoco.</span><span class="sxs-lookup"><span data-stu-id="f60ae-148">To create a new predefined tag, enter a unique name.</span></span>
<span data-ttu-id="f60ae-149">Per aggiungere un valore a un tag esistente, immettere il nome del tag esistente.</span><span class="sxs-lookup"><span data-stu-id="f60ae-149">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="f60ae-150">Se un tag predefinito esistente ha il nome specificato, **New-AzTag** aggiunge il valore specificato, se presente, al tag con quel nome invece di creare un nuovo tag.</span><span class="sxs-lookup"><span data-stu-id="f60ae-150">If an existing predefined tag has the specified name, **New-AzTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

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

### <span data-ttu-id="f60ae-151">-Valore</span><span class="sxs-lookup"><span data-stu-id="f60ae-151">-Value</span></span>
<span data-ttu-id="f60ae-152">Specifica un valore di tag predefinito.</span><span class="sxs-lookup"><span data-stu-id="f60ae-152">Specifies a predefined tag value.</span></span>
<span data-ttu-id="f60ae-153">I tag predefiniti possono avere più valori, ma è possibile immettere un solo valore in ogni comando.</span><span class="sxs-lookup"><span data-stu-id="f60ae-153">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="f60ae-154">Questo parametro è facoltativo, perché i tag possono avere nomi senza valori.</span><span class="sxs-lookup"><span data-stu-id="f60ae-154">This parameter is optional, because tags can have names without values.</span></span>

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

### <span data-ttu-id="f60ae-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f60ae-155">-ResourceId</span></span>
<span data-ttu-id="f60ae-156">Identificatore delle risorse per l'entità da contrassegnare.</span><span class="sxs-lookup"><span data-stu-id="f60ae-156">The resource identifier for the entity being tagged.</span></span> <span data-ttu-id="f60ae-157">Una risorsa, un gruppo di risorse o un abbonamento possono essere contrassegnati.</span><span class="sxs-lookup"><span data-stu-id="f60ae-157">A resource, a resource group or a subscription may be tagged.</span></span>

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

### <span data-ttu-id="f60ae-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="f60ae-158">-Tag</span></span>
<span data-ttu-id="f60ae-159">Tag da inserire nella risorsa.</span><span class="sxs-lookup"><span data-stu-id="f60ae-159">The tags to put on the resource.</span></span>

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

### <span data-ttu-id="f60ae-160">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f60ae-160">-Confirm</span></span>
<span data-ttu-id="f60ae-161">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f60ae-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f60ae-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f60ae-162">-WhatIf</span></span>
<span data-ttu-id="f60ae-163">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f60ae-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f60ae-164">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f60ae-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f60ae-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f60ae-165">CommonParameters</span></span>
<span data-ttu-id="f60ae-166">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f60ae-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f60ae-167">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f60ae-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f60ae-168">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f60ae-168">INPUTS</span></span>

### <span data-ttu-id="f60ae-169">System. String</span><span class="sxs-lookup"><span data-stu-id="f60ae-169">System.String</span></span>

### <span data-ttu-id="f60ae-170">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f60ae-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f60ae-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f60ae-171">OUTPUTS</span></span>

### <span data-ttu-id="f60ae-172">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. Model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="f60ae-172">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="f60ae-173">Note</span><span class="sxs-lookup"><span data-stu-id="f60ae-173">NOTES</span></span>

## <span data-ttu-id="f60ae-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f60ae-174">RELATED LINKS</span></span>

[<span data-ttu-id="f60ae-175">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="f60ae-175">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="f60ae-176">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="f60ae-176">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="f60ae-177">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="f60ae-177">Update-AzTag</span></span>](./Update-AzTag.md)
