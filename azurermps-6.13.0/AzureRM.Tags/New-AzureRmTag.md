---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/new-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
ms.openlocfilehash: cd9700a633f1a9c09c5fafd060d318b35eaeaabb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521284"
---
# <span data-ttu-id="7a86a-101">New-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="7a86a-101">New-AzureRmTag</span></span>

## <span data-ttu-id="7a86a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7a86a-102">SYNOPSIS</span></span>
<span data-ttu-id="7a86a-103">Crea un tag Azure predefinito o aggiunge valori a un tag esistente.</span><span class="sxs-lookup"><span data-stu-id="7a86a-103">Creates a predefined Azure tag or adds values to an existing tag.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a86a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a86a-104">SYNTAX</span></span>

```
New-AzureRmTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a86a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a86a-105">DESCRIPTION</span></span>
<span data-ttu-id="7a86a-106">Il cmdlet **New-AzureRmTag** crea un tag Azure predefinito con un valore predefinito facoltativo.</span><span class="sxs-lookup"><span data-stu-id="7a86a-106">The **New-AzureRmTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="7a86a-107">Puoi anche usarla per aggiungere altri valori ai tag predefiniti esistenti.</span><span class="sxs-lookup"><span data-stu-id="7a86a-107">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="7a86a-108">Per creare un tag predefinito, immetti un nome di tag univoco.</span><span class="sxs-lookup"><span data-stu-id="7a86a-108">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="7a86a-109">Per aggiungere un valore a un tag predefinito esistente, specificare il nome del tag esistente e il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="7a86a-109">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>
<span data-ttu-id="7a86a-110">Questo cmdlet restituisce un oggetto che rappresenta il tag New o Modified con i relativi valori e il numero di risorse a cui è stato applicato.</span><span class="sxs-lookup"><span data-stu-id="7a86a-110">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>
<span data-ttu-id="7a86a-111">Il modulo Tag Azure di cui fa parte **New-AzureRmTag** può aiutarti a gestire i tag di Azure predefiniti.</span><span class="sxs-lookup"><span data-stu-id="7a86a-111">The Azure Tags module that **New-AzureRmTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="7a86a-112">Un tag Azure è una coppia nome-valore che puoi usare per categorizzare le risorse e i gruppi di risorse di Azure, ad esempio per reparto o centro costo, oppure per tenere traccia di note o commenti relativi a risorse e gruppi.</span><span class="sxs-lookup"><span data-stu-id="7a86a-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="7a86a-113">È possibile definire e applicare i tag in un singolo passaggio, ma i tag predefiniti consentono di stabilire nomi e valori standard, coerenti e prevedibili per i tag nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7a86a-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="7a86a-114">Per applicare un contrassegno predefinito a una risorsa o a un gruppo di risorse, usare il parametro *tag* del cmdlet New-AzureRmTag.</span><span class="sxs-lookup"><span data-stu-id="7a86a-114">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="7a86a-115">Per cercare gruppi di risorse con un nome di tag o un nome e un valore specificati, usare il parametro *tag* del cmdlet Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7a86a-115">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="7a86a-116">Ogni tag ha un nome.</span><span class="sxs-lookup"><span data-stu-id="7a86a-116">Every tag has a name.</span></span>
<span data-ttu-id="7a86a-117">I valori sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="7a86a-117">The values are optional.</span></span>
<span data-ttu-id="7a86a-118">Un tag Azure predefinito può avere più valori, ma quando si applica il contrassegno a una risorsa o a un gruppo di risorse, è possibile applicare il nome del tag e solo uno dei relativi valori.</span><span class="sxs-lookup"><span data-stu-id="7a86a-118">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="7a86a-119">Ad esempio, puoi creare un tag di reparto predefinito con un valore per ogni reparto, come finanza, risorse umane e IT.</span><span class="sxs-lookup"><span data-stu-id="7a86a-119">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="7a86a-120">Quando si applica il tag Department a una risorsa, si applica un solo valore predefinito, ad esempio Finance.</span><span class="sxs-lookup"><span data-stu-id="7a86a-120">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

## <span data-ttu-id="7a86a-121">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a86a-121">EXAMPLES</span></span>

### <span data-ttu-id="7a86a-122">Esempio 1: creare un tag predefinito</span><span class="sxs-lookup"><span data-stu-id="7a86a-122">Example 1: Create a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "FY2015"
Name:   FY2015
Count:  0
Values: 

        Name        Count
        =========   =====

        Finance     0
```

<span data-ttu-id="7a86a-123">Questo comando crea un tag predefinito denominato FY2015.</span><span class="sxs-lookup"><span data-stu-id="7a86a-123">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="7a86a-124">Questo tag non contiene valori.</span><span class="sxs-lookup"><span data-stu-id="7a86a-124">This tag has no values.</span></span>
<span data-ttu-id="7a86a-125">Puoi applicare un contrassegno senza valori a una risorsa o a un gruppo di risorse oppure usare **New-AzureRmTag** per aggiungere valori al tag.</span><span class="sxs-lookup"><span data-stu-id="7a86a-125">You can apply a tag with no values to a resource or resource group, or use **New-AzureRmTag** to add values to the tag.</span></span>
<span data-ttu-id="7a86a-126">Puoi anche specificare un valore quando applichi il tag al gruppo di risorse o risorse.</span><span class="sxs-lookup"><span data-stu-id="7a86a-126">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="7a86a-127">Esempio 2: creare un tag predefinito con un valore</span><span class="sxs-lookup"><span data-stu-id="7a86a-127">Example 2: Create a predefined tag with a value</span></span>
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="7a86a-128">Questo comando crea un tag predefinito denominato Department con un valore di Finance.</span><span class="sxs-lookup"><span data-stu-id="7a86a-128">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="7a86a-129">Esempio 3: aggiungere un valore a un tag predefinito</span><span class="sxs-lookup"><span data-stu-id="7a86a-129">Example 3: Add a value to a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 
PS C:\>New-AzureRmTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

<span data-ttu-id="7a86a-130">Questi comandi creano un tag predefinito denominato Department con due valori.</span><span class="sxs-lookup"><span data-stu-id="7a86a-130">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="7a86a-131">Se il nome del tag esiste, **New-AzureRmTag** aggiunge il valore al tag esistente anziché crearne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="7a86a-131">If the tag name exists, **New-AzureRmTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="7a86a-132">Esempio 4: usare un tag predefinito</span><span class="sxs-lookup"><span data-stu-id="7a86a-132">Example 4: Use a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 
PS C:\>Set-AzureRmResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
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
PS C:\>Get-AzureRmTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 
PS C:\>Get-AzureRmResourceGroup -Tag @{Name="CostCenter"}
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

<span data-ttu-id="7a86a-133">I comandi in questo esempio creano e usano un tag predefinito.</span><span class="sxs-lookup"><span data-stu-id="7a86a-133">The commands in this example create and use a predefined tag.</span></span>

## <span data-ttu-id="7a86a-134">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7a86a-134">PARAMETERS</span></span>

### <span data-ttu-id="7a86a-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a86a-135">-DefaultProfile</span></span>
<span data-ttu-id="7a86a-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7a86a-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a86a-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a86a-137">-Name</span></span>
<span data-ttu-id="7a86a-138">Specifica il nome del tag.</span><span class="sxs-lookup"><span data-stu-id="7a86a-138">Specifies the tag name.</span></span>
<span data-ttu-id="7a86a-139">Per creare un nuovo tag predefinito, immettere un nome univoco.</span><span class="sxs-lookup"><span data-stu-id="7a86a-139">To create a new predefined tag, enter a unique name.</span></span>
<span data-ttu-id="7a86a-140">Per aggiungere un valore a un tag esistente, immettere il nome del tag esistente.</span><span class="sxs-lookup"><span data-stu-id="7a86a-140">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="7a86a-141">Se un tag predefinito esistente ha il nome specificato, **New-AzureRmTag** aggiunge il valore specificato, se presente, al tag con quel nome invece di creare un nuovo tag.</span><span class="sxs-lookup"><span data-stu-id="7a86a-141">If an existing predefined tag has the specified name, **New-AzureRmTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a86a-142">-Valore</span><span class="sxs-lookup"><span data-stu-id="7a86a-142">-Value</span></span>
<span data-ttu-id="7a86a-143">Specifica un valore di tag.</span><span class="sxs-lookup"><span data-stu-id="7a86a-143">Specifies a tag value.</span></span>
<span data-ttu-id="7a86a-144">I tag predefiniti possono avere più valori, ma è possibile immettere un solo valore in ogni comando.</span><span class="sxs-lookup"><span data-stu-id="7a86a-144">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="7a86a-145">Questo parametro è facoltativo, perché i tag possono avere nomi senza valori.</span><span class="sxs-lookup"><span data-stu-id="7a86a-145">This parameter is optional, because tags can have names without values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a86a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a86a-146">CommonParameters</span></span>
<span data-ttu-id="7a86a-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a86a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a86a-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a86a-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a86a-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7a86a-149">INPUTS</span></span>

### <span data-ttu-id="7a86a-150">System. String</span><span class="sxs-lookup"><span data-stu-id="7a86a-150">System.String</span></span>

## <span data-ttu-id="7a86a-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a86a-151">OUTPUTS</span></span>

### <span data-ttu-id="7a86a-152">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag</span><span class="sxs-lookup"><span data-stu-id="7a86a-152">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="7a86a-153">Note</span><span class="sxs-lookup"><span data-stu-id="7a86a-153">NOTES</span></span>

## <span data-ttu-id="7a86a-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a86a-154">RELATED LINKS</span></span>

[<span data-ttu-id="7a86a-155">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="7a86a-155">Get-AzureRmTag</span></span>](./Get-AzureRmTag.md)

[<span data-ttu-id="7a86a-156">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="7a86a-156">Remove-AzureRmTag</span></span>](./Remove-AzureRmTag.md)


