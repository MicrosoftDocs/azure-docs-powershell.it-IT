---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: b44c861e06c1043fd53e470cfba1e322ce1f1f48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992444"
---
# <span data-ttu-id="354c3-101">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="354c3-101">Get-AzTag</span></span>

## <span data-ttu-id="354c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="354c3-102">SYNOPSIS</span></span>
<span data-ttu-id="354c3-103">Recupera i tag di Azure | Ottiene l'intero set di tag per una risorsa o un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="354c3-103">Gets predefined Azure tags | Gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="354c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="354c3-104">SYNTAX</span></span>

### <span data-ttu-id="354c3-105">GetPredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="354c3-105">GetPredefinedTagParameterSet</span></span>
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="354c3-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="354c3-106">GetByResourceIdParameterSet</span></span>
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="354c3-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="354c3-107">DESCRIPTION</span></span>

<span data-ttu-id="354c3-108">**GetPredefinedTagSet:** il cmdlet **Get-AzTag** ottiene tag Azure predefiniti nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="354c3-108">**GetPredefinedTagSet**: The **Get-AzTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="354c3-109">Questo cmdlet restituisce informazioni di base sui tag o informazioni dettagliate sui tag e i relativi valori.</span><span class="sxs-lookup"><span data-stu-id="354c3-109">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="354c3-110">Tutti gli oggetti di output includono una proprietà Count che rappresenta il numero di risorse e gruppi di risorse a cui sono stati applicati i tag e i valori.</span><span class="sxs-lookup"><span data-stu-id="354c3-110">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="354c3-111">Il modulo Tag di Azure di cui fa parte **Get-AzTag** può aiutare a gestire i tag di Azure predefiniti.</span><span class="sxs-lookup"><span data-stu-id="354c3-111">The Azure Tags module that **Get-AzTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="354c3-112">Un tag di Azure è una coppia nome-valore che è possibile usare per categorizzare le risorse e i gruppi di risorse di Azure, ad esempio per reparto o centro di costo, oppure per tenere traccia di note o commenti sulle risorse e i gruppi.</span><span class="sxs-lookup"><span data-stu-id="354c3-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="354c3-113">È possibile definire e applicare tag in un unico passaggio, ma i tag predefiniti consentono di definire nomi e valori standard, coerenti e prevedibili per i tag nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="354c3-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="354c3-114">Per creare un tag predefinito, usare il cmdlet New-AzTag tag.</span><span class="sxs-lookup"><span data-stu-id="354c3-114">To create a predefined tag, use the New-AzTag cmdlet.</span></span>
<span data-ttu-id="354c3-115">Per applicare un tag predefinito a un gruppo di risorse, usare il *parametro Tag* del cmdlet New-AzTag.</span><span class="sxs-lookup"><span data-stu-id="354c3-115">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="354c3-116">Per cercare un nome tag o un valore o un nome tag specifico nei gruppi di risorse, usare il *parametro Tag* del cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="354c3-116">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>

<span data-ttu-id="354c3-117">**GetByResourceIdParameterSet:** il cmdlet **Get-AzTag** con **un valore ResourceId** ottiene l'intero set di tag per una risorsa o una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="354c3-117">**GetByResourceIdParameterSet**: The **Get-AzTag** cmdlet with a **ResourceId** gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="354c3-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="354c3-118">EXAMPLES</span></span>

### <span data-ttu-id="354c3-119">Esempio 1: Ottenere tutti i tag predefiniti</span><span class="sxs-lookup"><span data-stu-id="354c3-119">Example 1: Get all predefined tags</span></span>
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="354c3-120">Questo comando recupera tutti i tag predefiniti nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="354c3-120">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="354c3-121">La proprietà Count indica quante volte il tag è stato applicato alle risorse e ai gruppi di risorse nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="354c3-121">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="354c3-122">Esempio 2: Ottenere un tag in base al nome</span><span class="sxs-lookup"><span data-stu-id="354c3-122">Example 2: Get a tag by name</span></span>
```powershell
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="354c3-123">Questo comando ottiene informazioni dettagliate sul tag Department e sui relativi valori.</span><span class="sxs-lookup"><span data-stu-id="354c3-123">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="354c3-124">La proprietà Count indica quante volte il tag e i relativi valori sono stati applicati alle risorse e ai gruppi di risorse nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="354c3-124">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="354c3-125">Esempio 3: Ottenere i valori di tutti i tag</span><span class="sxs-lookup"><span data-stu-id="354c3-125">Example 3: Get values of all tags</span></span>
```powershell
PS C:\>Get-AzTag -Detailed

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3


Name:   FY2015
Count:  2


Name:   CostCenter
Count:  20
Values: 

        Name        Count
        ==========  =====

        0001          5
        0002         10
        0003          5
```

<span data-ttu-id="354c3-126">Questo comando usa il *parametro Detailed* per ottenere informazioni dettagliate su tutti i tag predefiniti dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="354c3-126">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="354c3-127">*L'uso del parametro Detailed* equivale a usare il *parametro Name* per ogni tag.</span><span class="sxs-lookup"><span data-stu-id="354c3-127">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

### <span data-ttu-id="354c3-128">Esempio 4: Ottenere l'intero set di tag in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="354c3-128">Example 4: Get the entire set of tags on a subscription</span></span>

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

<span data-ttu-id="354c3-129">Questo comando recupera l'intero set di tag nell'abbonamento con {subId}.</span><span class="sxs-lookup"><span data-stu-id="354c3-129">This command gets the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="354c3-130">Esempio 5: Ottenere l'intero set di tag per una risorsa</span><span class="sxs-lookup"><span data-stu-id="354c3-130">Example 5: Get the entire set of tags on a resource</span></span>

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="354c3-131">Questo comando ottiene l'intero set di tag per la risorsa con {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="354c3-131">This command gets the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="354c3-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="354c3-132">PARAMETERS</span></span>

### <span data-ttu-id="354c3-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="354c3-133">-DefaultProfile</span></span>
<span data-ttu-id="354c3-134">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="354c3-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="354c3-135">-Detailed</span><span class="sxs-lookup"><span data-stu-id="354c3-135">-Detailed</span></span>
<span data-ttu-id="354c3-136">Indica che questa operazione aggiunge all'output informazioni sui valori dei tag.</span><span class="sxs-lookup"><span data-stu-id="354c3-136">Indicates that this operation adds information about tag values to the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="354c3-137">-Name</span><span class="sxs-lookup"><span data-stu-id="354c3-137">-Name</span></span>
<span data-ttu-id="354c3-138">Nome del tag predefinito.</span><span class="sxs-lookup"><span data-stu-id="354c3-138">Name of the predefined tag.</span></span>
<span data-ttu-id="354c3-139">Per impostazione predefinita, **Get-AzTag** ottiene informazioni di base su tutti i tag predefiniti dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="354c3-139">By default, **Get-AzTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="354c3-140">Quando si specifica il *parametro Name,* il *parametro Detailed* non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="354c3-140">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

```yaml
Type: System.String
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="354c3-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="354c3-141">-ResourceId</span></span>
<span data-ttu-id="354c3-142">Identificatore di risorsa per l'entità con tag.</span><span class="sxs-lookup"><span data-stu-id="354c3-142">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="354c3-143">Una risorsa, un gruppo di risorse o una sottoscrizione può essere contrassegnata.</span><span class="sxs-lookup"><span data-stu-id="354c3-143">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="354c3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="354c3-144">CommonParameters</span></span>
<span data-ttu-id="354c3-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="354c3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="354c3-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="354c3-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="354c3-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="354c3-147">INPUTS</span></span>

### <span data-ttu-id="354c3-148">System.String</span><span class="sxs-lookup"><span data-stu-id="354c3-148">System.String</span></span>

### <span data-ttu-id="354c3-149">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="354c3-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="354c3-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="354c3-150">OUTPUTS</span></span>

### <span data-ttu-id="354c3-151">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="354c3-151">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="354c3-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="354c3-152">NOTES</span></span>

## <span data-ttu-id="354c3-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="354c3-153">RELATED LINKS</span></span>

[<span data-ttu-id="354c3-154">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="354c3-154">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="354c3-155">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="354c3-155">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="354c3-156">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="354c3-156">Update-AzTag</span></span>](./Update-AzTag.md)
