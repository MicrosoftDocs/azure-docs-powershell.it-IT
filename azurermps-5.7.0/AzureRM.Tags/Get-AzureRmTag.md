---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/get-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
ms.openlocfilehash: 79fa1522ed0eec95a1e388ed5d113cf98ad7f525
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519818"
---
# <span data-ttu-id="f11ff-101">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="f11ff-101">Get-AzureRmTag</span></span>

## <span data-ttu-id="f11ff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f11ff-102">SYNOPSIS</span></span>
<span data-ttu-id="f11ff-103">Ottiene i contrassegni di Azure predefiniti.</span><span class="sxs-lookup"><span data-stu-id="f11ff-103">Gets predefined Azure tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f11ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f11ff-104">SYNTAX</span></span>

```
Get-AzureRmTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f11ff-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f11ff-105">DESCRIPTION</span></span>
<span data-ttu-id="f11ff-106">Il cmdlet **Get-AzureRmTag** ottiene i tag di Azure predefiniti nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f11ff-106">The **Get-AzureRmTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="f11ff-107">Questo cmdlet restituisce le informazioni di base sui tag o le informazioni dettagliate sui tag e i relativi valori.</span><span class="sxs-lookup"><span data-stu-id="f11ff-107">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="f11ff-108">Tutti gli oggetti di output includono una proprietà Count che rappresenta il numero di risorse e gruppi di risorse a cui sono stati applicati i tag e i valori.</span><span class="sxs-lookup"><span data-stu-id="f11ff-108">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>

<span data-ttu-id="f11ff-109">Il modulo tag di Azure che **Get-AzureRMTag** fa parte di può aiutare a gestire i tag di Azure predefiniti.</span><span class="sxs-lookup"><span data-stu-id="f11ff-109">The Azure Tags module that **Get-AzureRMTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="f11ff-110">Un tag Azure è una coppia nome-valore che puoi usare per categorizzare le risorse e i gruppi di risorse di Azure, ad esempio per reparto o centro costo, oppure per tenere traccia di note o commenti relativi a risorse e gruppi.</span><span class="sxs-lookup"><span data-stu-id="f11ff-110">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>

<span data-ttu-id="f11ff-111">È possibile definire e applicare i tag in un singolo passaggio, ma i tag predefiniti consentono di stabilire nomi e valori standard, coerenti e prevedibili per i tag nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f11ff-111">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="f11ff-112">Se l'abbonamento include eventuali tag predefiniti, non è possibile applicare tag o valori non definiti a qualsiasi risorsa o gruppo di risorse nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f11ff-112">If the subscription includes any predefined tags, you cannot apply undefined tags or values to any resource or resource group in the subscription.</span></span>

<span data-ttu-id="f11ff-113">Per creare un tag predefinito, usare il cmdlet New-AzureRmTag.</span><span class="sxs-lookup"><span data-stu-id="f11ff-113">To create a predefined tag, use the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="f11ff-114">Per applicare un contrassegno predefinito a un gruppo di risorse, usa il parametro *tag* del cmdlet New-AzureRmTag.</span><span class="sxs-lookup"><span data-stu-id="f11ff-114">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="f11ff-115">Per cercare un nome di tag specifico o un nome e un valore per i gruppi di risorse, usa il parametro *tag* del cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f11ff-115">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzureRMResourceGroup cmdlet.</span></span>

## <span data-ttu-id="f11ff-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f11ff-116">EXAMPLES</span></span>

### <span data-ttu-id="f11ff-117">Esempio 1: ottenere tutti i tag predefiniti</span><span class="sxs-lookup"><span data-stu-id="f11ff-117">Example 1: Get all predefined tags</span></span>
```
PS C:\>Get-AzureRmTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="f11ff-118">Questo comando ottiene tutti i tag predefiniti nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f11ff-118">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="f11ff-119">La proprietà Count Mostra il numero di volte in cui il tag è stato applicato alle risorse e ai gruppi di risorse nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f11ff-119">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="f11ff-120">Esempio 2: ottenere un tag per nome</span><span class="sxs-lookup"><span data-stu-id="f11ff-120">Example 2: Get a tag by name</span></span>
```
PS C:\>Get-AzureRmTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="f11ff-121">Questo comando consente di ottenere informazioni dettagliate sul tag Department e sui relativi valori.</span><span class="sxs-lookup"><span data-stu-id="f11ff-121">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="f11ff-122">La proprietà Count Mostra il numero di volte in cui il tag e ognuno dei relativi valori sono stati applicati alle risorse e ai gruppi di risorse nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f11ff-122">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="f11ff-123">Esempio 3: ottenere i valori di tutti i tag</span><span class="sxs-lookup"><span data-stu-id="f11ff-123">Example 3: Get values of all tags</span></span>
```
PS C:\>Get-AzureRmTag -Detailed

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

<span data-ttu-id="f11ff-124">Questo comando usa il parametro *detailed* per ottenere informazioni dettagliate su tutti i tag predefiniti nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f11ff-124">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="f11ff-125">L'uso del parametro *detailed* equivale all'uso del parametro *Name* per ogni tag.</span><span class="sxs-lookup"><span data-stu-id="f11ff-125">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

## <span data-ttu-id="f11ff-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f11ff-126">PARAMETERS</span></span>

### <span data-ttu-id="f11ff-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f11ff-127">-DefaultProfile</span></span>
<span data-ttu-id="f11ff-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f11ff-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f11ff-129">-Dettagli</span><span class="sxs-lookup"><span data-stu-id="f11ff-129">-Detailed</span></span>
<span data-ttu-id="f11ff-130">Indica che questa operazione aggiunge informazioni sui valori di tag nell'output.</span><span class="sxs-lookup"><span data-stu-id="f11ff-130">Indicates that this operation adds information about tag values to the output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f11ff-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="f11ff-131">-Name</span></span>
<span data-ttu-id="f11ff-132">Specifica il nome del tag da ottenere.</span><span class="sxs-lookup"><span data-stu-id="f11ff-132">Specifies the name of the tag to get.</span></span>
<span data-ttu-id="f11ff-133">Per impostazione predefinita, **Get-AzureRmTag** ottiene le informazioni di base su tutti i tag predefiniti nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f11ff-133">By default, **Get-AzureRmTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="f11ff-134">Quando specifichi il parametro *Name* , il parametro *detailed* non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="f11ff-134">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f11ff-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f11ff-135">CommonParameters</span></span>
<span data-ttu-id="f11ff-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f11ff-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f11ff-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f11ff-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f11ff-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f11ff-138">INPUTS</span></span>

### <span data-ttu-id="f11ff-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f11ff-139">None</span></span>

## <span data-ttu-id="f11ff-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f11ff-140">OUTPUTS</span></span>

### <span data-ttu-id="f11ff-141">Microsoft. Azure. Commands. Tags. Model. PSTag, Microsoft. Azure. Commands. Tags</span><span class="sxs-lookup"><span data-stu-id="f11ff-141">Microsoft.Azure.Commands.Tags.Model.PSTag, Microsoft.Azure.Commands.Tags</span></span>

## <span data-ttu-id="f11ff-142">Note</span><span class="sxs-lookup"><span data-stu-id="f11ff-142">NOTES</span></span>

## <span data-ttu-id="f11ff-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f11ff-143">RELATED LINKS</span></span>

[<span data-ttu-id="f11ff-144">New-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="f11ff-144">New-AzureRmTag</span></span>](./New-AzureRmTag.md)

[<span data-ttu-id="f11ff-145">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="f11ff-145">Remove-AzureRmTag</span></span>](./Remove-AzureRmTag.md)


