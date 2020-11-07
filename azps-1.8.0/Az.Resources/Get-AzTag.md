---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: ce672284a3d9887fe52c33081f04a86e1e072405
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677368"
---
# <span data-ttu-id="774ba-101">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="774ba-101">Get-AzTag</span></span>

## <span data-ttu-id="774ba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="774ba-102">SYNOPSIS</span></span>
<span data-ttu-id="774ba-103">Ottiene i contrassegni di Azure predefiniti.</span><span class="sxs-lookup"><span data-stu-id="774ba-103">Gets predefined Azure tags.</span></span>

## <span data-ttu-id="774ba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="774ba-104">SYNTAX</span></span>

```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="774ba-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="774ba-105">DESCRIPTION</span></span>
<span data-ttu-id="774ba-106">Il cmdlet **Get-AzTag** ottiene i tag di Azure predefiniti nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="774ba-106">The **Get-AzTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="774ba-107">Questo cmdlet restituisce le informazioni di base sui tag o le informazioni dettagliate sui tag e i relativi valori.</span><span class="sxs-lookup"><span data-stu-id="774ba-107">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="774ba-108">Tutti gli oggetti di output includono una proprietà Count che rappresenta il numero di risorse e gruppi di risorse a cui sono stati applicati i tag e i valori.</span><span class="sxs-lookup"><span data-stu-id="774ba-108">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="774ba-109">Il modulo tag di Azure che **Get-AzTag** fa parte di può aiutare a gestire i tag di Azure predefiniti.</span><span class="sxs-lookup"><span data-stu-id="774ba-109">The Azure Tags module that **Get-AzTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="774ba-110">Un tag Azure è una coppia nome-valore che puoi usare per categorizzare le risorse e i gruppi di risorse di Azure, ad esempio per reparto o centro costo, oppure per tenere traccia di note o commenti relativi a risorse e gruppi.</span><span class="sxs-lookup"><span data-stu-id="774ba-110">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="774ba-111">È possibile definire e applicare i tag in un singolo passaggio, ma i tag predefiniti consentono di stabilire nomi e valori standard, coerenti e prevedibili per i tag nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="774ba-111">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="774ba-112">Per creare un tag predefinito, usare il cmdlet New-AzTag.</span><span class="sxs-lookup"><span data-stu-id="774ba-112">To create a predefined tag, use the New-AzTag cmdlet.</span></span>
<span data-ttu-id="774ba-113">Per applicare un contrassegno predefinito a un gruppo di risorse, usa il parametro *tag* del cmdlet New-AzTag.</span><span class="sxs-lookup"><span data-stu-id="774ba-113">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="774ba-114">Per cercare un nome di tag specifico o un nome e un valore per i gruppi di risorse, usa il parametro *tag* del cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="774ba-114">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="774ba-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="774ba-115">EXAMPLES</span></span>

### <span data-ttu-id="774ba-116">Esempio 1: ottenere tutti i tag predefiniti</span><span class="sxs-lookup"><span data-stu-id="774ba-116">Example 1: Get all predefined tags</span></span>
```
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="774ba-117">Questo comando ottiene tutti i tag predefiniti nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="774ba-117">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="774ba-118">La proprietà Count Mostra il numero di volte in cui il tag è stato applicato alle risorse e ai gruppi di risorse nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="774ba-118">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="774ba-119">Esempio 2: ottenere un tag per nome</span><span class="sxs-lookup"><span data-stu-id="774ba-119">Example 2: Get a tag by name</span></span>
```
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="774ba-120">Questo comando consente di ottenere informazioni dettagliate sul tag Department e sui relativi valori.</span><span class="sxs-lookup"><span data-stu-id="774ba-120">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="774ba-121">La proprietà Count Mostra il numero di volte in cui il tag e ognuno dei relativi valori sono stati applicati alle risorse e ai gruppi di risorse nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="774ba-121">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="774ba-122">Esempio 3: ottenere i valori di tutti i tag</span><span class="sxs-lookup"><span data-stu-id="774ba-122">Example 3: Get values of all tags</span></span>
```
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

<span data-ttu-id="774ba-123">Questo comando usa il parametro *detailed* per ottenere informazioni dettagliate su tutti i tag predefiniti nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="774ba-123">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="774ba-124">L'uso del parametro *detailed* equivale all'uso del parametro *Name* per ogni tag.</span><span class="sxs-lookup"><span data-stu-id="774ba-124">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

## <span data-ttu-id="774ba-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="774ba-125">PARAMETERS</span></span>

### <span data-ttu-id="774ba-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="774ba-126">-DefaultProfile</span></span>
<span data-ttu-id="774ba-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="774ba-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="774ba-128">-Dettagli</span><span class="sxs-lookup"><span data-stu-id="774ba-128">-Detailed</span></span>
<span data-ttu-id="774ba-129">Indica che questa operazione aggiunge informazioni sui valori di tag nell'output.</span><span class="sxs-lookup"><span data-stu-id="774ba-129">Indicates that this operation adds information about tag values to the output.</span></span>

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

### <span data-ttu-id="774ba-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="774ba-130">-Name</span></span>
<span data-ttu-id="774ba-131">Specifica il nome del tag da ottenere.</span><span class="sxs-lookup"><span data-stu-id="774ba-131">Specifies the name of the tag to get.</span></span>
<span data-ttu-id="774ba-132">Per impostazione predefinita, **Get-AzTag** ottiene le informazioni di base su tutti i tag predefiniti nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="774ba-132">By default, **Get-AzTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="774ba-133">Quando specifichi il parametro *Name* , il parametro *detailed* non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="774ba-133">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="774ba-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="774ba-134">CommonParameters</span></span>
<span data-ttu-id="774ba-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="774ba-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="774ba-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="774ba-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="774ba-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="774ba-137">INPUTS</span></span>

### <span data-ttu-id="774ba-138">System. String</span><span class="sxs-lookup"><span data-stu-id="774ba-138">System.String</span></span>

### <span data-ttu-id="774ba-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="774ba-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="774ba-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="774ba-140">OUTPUTS</span></span>

### <span data-ttu-id="774ba-141">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag</span><span class="sxs-lookup"><span data-stu-id="774ba-141">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="774ba-142">Note</span><span class="sxs-lookup"><span data-stu-id="774ba-142">NOTES</span></span>

## <span data-ttu-id="774ba-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="774ba-143">RELATED LINKS</span></span>

[<span data-ttu-id="774ba-144">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="774ba-144">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="774ba-145">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="774ba-145">Remove-AzTag</span></span>](./Remove-AzTag.md)

