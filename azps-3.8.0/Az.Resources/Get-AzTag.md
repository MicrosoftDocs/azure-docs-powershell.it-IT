---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 058f4a61f1e7ff2fe7f416ea0e4ada098c9efe51
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021738"
---
# <span data-ttu-id="36cd3-101">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="36cd3-101">Get-AzTag</span></span>

## <span data-ttu-id="36cd3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="36cd3-102">SYNOPSIS</span></span>
<span data-ttu-id="36cd3-103">Ottiene i tag Azure predefiniti | Ottiene l'intero set di tag in una risorsa o un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="36cd3-103">Gets predefined Azure tags | Gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="36cd3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36cd3-104">SYNTAX</span></span>

### <span data-ttu-id="36cd3-105">GetPredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="36cd3-105">GetPredefinedTagParameterSet</span></span>
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36cd3-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="36cd3-106">GetByResourceIdParameterSet</span></span>
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36cd3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36cd3-107">DESCRIPTION</span></span>

<span data-ttu-id="36cd3-108">**GetPredefinedTagSet** : il cmdlet **Get-AzTag** ottiene i tag di Azure predefiniti nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="36cd3-108">**GetPredefinedTagSet** : The **Get-AzTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="36cd3-109">Questo cmdlet restituisce le informazioni di base sui tag o le informazioni dettagliate sui tag e i relativi valori.</span><span class="sxs-lookup"><span data-stu-id="36cd3-109">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="36cd3-110">Tutti gli oggetti di output includono una proprietà Count che rappresenta il numero di risorse e gruppi di risorse a cui sono stati applicati i tag e i valori.</span><span class="sxs-lookup"><span data-stu-id="36cd3-110">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="36cd3-111">Il modulo tag di Azure che **Get-AzTag** fa parte di può aiutare a gestire i tag di Azure predefiniti.</span><span class="sxs-lookup"><span data-stu-id="36cd3-111">The Azure Tags module that **Get-AzTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="36cd3-112">Un tag Azure è una coppia nome-valore che puoi usare per categorizzare le risorse e i gruppi di risorse di Azure, ad esempio per reparto o centro costo, oppure per tenere traccia di note o commenti relativi a risorse e gruppi.</span><span class="sxs-lookup"><span data-stu-id="36cd3-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="36cd3-113">È possibile definire e applicare i tag in un singolo passaggio, ma i tag predefiniti consentono di stabilire nomi e valori standard, coerenti e prevedibili per i tag nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="36cd3-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="36cd3-114">Per creare un tag predefinito, usare il cmdlet New-AzTag.</span><span class="sxs-lookup"><span data-stu-id="36cd3-114">To create a predefined tag, use the New-AzTag cmdlet.</span></span>
<span data-ttu-id="36cd3-115">Per applicare un contrassegno predefinito a un gruppo di risorse, usa il parametro *tag* del cmdlet New-AzTag.</span><span class="sxs-lookup"><span data-stu-id="36cd3-115">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="36cd3-116">Per cercare un nome di tag specifico o un nome e un valore per i gruppi di risorse, usa il parametro *tag* del cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="36cd3-116">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>

<span data-ttu-id="36cd3-117">**GetByResourceIdParameterSet** : il cmdlet **Get-AzTag** con un **resourceId** Ottiene l'intero set di tag in una risorsa o un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="36cd3-117">**GetByResourceIdParameterSet** : The **Get-AzTag** cmdlet with a **ResourceId** gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="36cd3-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36cd3-118">EXAMPLES</span></span>

### <span data-ttu-id="36cd3-119">Esempio 1: ottenere tutti i tag predefiniti</span><span class="sxs-lookup"><span data-stu-id="36cd3-119">Example 1: Get all predefined tags</span></span>
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="36cd3-120">Questo comando ottiene tutti i tag predefiniti nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="36cd3-120">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="36cd3-121">La proprietà Count Mostra il numero di volte in cui il tag è stato applicato alle risorse e ai gruppi di risorse nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="36cd3-121">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="36cd3-122">Esempio 2: ottenere un tag per nome</span><span class="sxs-lookup"><span data-stu-id="36cd3-122">Example 2: Get a tag by name</span></span>
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

<span data-ttu-id="36cd3-123">Questo comando consente di ottenere informazioni dettagliate sul tag Department e sui relativi valori.</span><span class="sxs-lookup"><span data-stu-id="36cd3-123">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="36cd3-124">La proprietà Count Mostra il numero di volte in cui il tag e ognuno dei relativi valori sono stati applicati alle risorse e ai gruppi di risorse nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="36cd3-124">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="36cd3-125">Esempio 3: ottenere i valori di tutti i tag</span><span class="sxs-lookup"><span data-stu-id="36cd3-125">Example 3: Get values of all tags</span></span>
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

<span data-ttu-id="36cd3-126">Questo comando usa il parametro *detailed* per ottenere informazioni dettagliate su tutti i tag predefiniti nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="36cd3-126">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="36cd3-127">L'uso del parametro *detailed* equivale all'uso del parametro *Name* per ogni tag.</span><span class="sxs-lookup"><span data-stu-id="36cd3-127">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

### <span data-ttu-id="36cd3-128">Esempio 4: ottenere l'intero set di tag in una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="36cd3-128">Example 4: Get the entire set of tags on a subscription</span></span>

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

<span data-ttu-id="36cd3-129">Questo comando consente di ottenere l'intero set di tag nell'abbonamento con {subId}.</span><span class="sxs-lookup"><span data-stu-id="36cd3-129">This command gets the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="36cd3-130">Esempio 5: ottenere l'intero set di tag in una risorsa</span><span class="sxs-lookup"><span data-stu-id="36cd3-130">Example 5: Get the entire set of tags on a resource</span></span>

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

<span data-ttu-id="36cd3-131">Questo comando consente di ottenere l'intero set di tag nella risorsa con {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="36cd3-131">This command gets the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="36cd3-132">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36cd3-132">PARAMETERS</span></span>

### <span data-ttu-id="36cd3-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36cd3-133">-DefaultProfile</span></span>
<span data-ttu-id="36cd3-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36cd3-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36cd3-135">-Dettagli</span><span class="sxs-lookup"><span data-stu-id="36cd3-135">-Detailed</span></span>
<span data-ttu-id="36cd3-136">Indica che questa operazione aggiunge informazioni sui valori di tag nell'output.</span><span class="sxs-lookup"><span data-stu-id="36cd3-136">Indicates that this operation adds information about tag values to the output.</span></span>

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

### <span data-ttu-id="36cd3-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="36cd3-137">-Name</span></span>
<span data-ttu-id="36cd3-138">Nome del tag predefinito.</span><span class="sxs-lookup"><span data-stu-id="36cd3-138">Name of the predefined tag.</span></span>
<span data-ttu-id="36cd3-139">Per impostazione predefinita, **Get-AzTag** ottiene le informazioni di base su tutti i tag predefiniti nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="36cd3-139">By default, **Get-AzTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="36cd3-140">Quando specifichi il parametro *Name* , il parametro *detailed* non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="36cd3-140">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

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

### <span data-ttu-id="36cd3-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36cd3-141">-ResourceId</span></span>
<span data-ttu-id="36cd3-142">Identificatore delle risorse per l'entità Tagged.</span><span class="sxs-lookup"><span data-stu-id="36cd3-142">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="36cd3-143">Una risorsa, un gruppo di risorse o un abbonamento possono essere contrassegnati.</span><span class="sxs-lookup"><span data-stu-id="36cd3-143">A resource, a resource group or a subscription may be tagged.</span></span>

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

### <span data-ttu-id="36cd3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36cd3-144">CommonParameters</span></span>
<span data-ttu-id="36cd3-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36cd3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36cd3-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36cd3-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36cd3-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="36cd3-147">INPUTS</span></span>

### <span data-ttu-id="36cd3-148">System. String</span><span class="sxs-lookup"><span data-stu-id="36cd3-148">System.String</span></span>

### <span data-ttu-id="36cd3-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="36cd3-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="36cd3-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36cd3-150">OUTPUTS</span></span>

### <span data-ttu-id="36cd3-151">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. Model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="36cd3-151">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="36cd3-152">Note</span><span class="sxs-lookup"><span data-stu-id="36cd3-152">NOTES</span></span>

## <span data-ttu-id="36cd3-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36cd3-153">RELATED LINKS</span></span>

[<span data-ttu-id="36cd3-154">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="36cd3-154">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="36cd3-155">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="36cd3-155">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="36cd3-156">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="36cd3-156">Update-AzTag</span></span>](./Update-AzTag.md)
