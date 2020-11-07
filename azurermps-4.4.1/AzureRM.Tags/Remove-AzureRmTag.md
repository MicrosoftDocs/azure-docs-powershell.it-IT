---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
ms.openlocfilehash: 909781b8cd441daab8bf5f567404a5e99e88cd0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687662"
---
# <span data-ttu-id="d9b38-101">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="d9b38-101">Remove-AzureRmTag</span></span>

## <span data-ttu-id="d9b38-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9b38-102">SYNOPSIS</span></span>
<span data-ttu-id="d9b38-103">Elimina i valori o i tag di Azure predefiniti.</span><span class="sxs-lookup"><span data-stu-id="d9b38-103">Deletes predefined Azure tags or values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9b38-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9b38-104">SYNTAX</span></span>

```
Remove-AzureRmTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9b38-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9b38-105">DESCRIPTION</span></span>
<span data-ttu-id="d9b38-106">Il cmdlet **Remove-AzureRmTag** Elimina i tag e i valori di Azure predefiniti dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d9b38-106">The **Remove-AzureRmTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="d9b38-107">Per eliminare valori particolari da un tag predefinito, usare il parametro *value* .</span><span class="sxs-lookup"><span data-stu-id="d9b38-107">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="d9b38-108">Per impostazione predefinita, **Remove-AzureRmTag** Elimina il tag specificato e tutti i relativi valori. Non è possibile eliminare un tag o un valore attualmente applicato a una risorsa o a un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d9b38-108">By default, **Remove-AzureRmTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>

<span data-ttu-id="d9b38-109">Prima di usare **Remove-AzureRmTag** , usa il parametro *tag* del cmdlet Set-AzureRMResourceGroup per eliminare il tag o i valori dal gruppo Resource o Resource.</span><span class="sxs-lookup"><span data-stu-id="d9b38-109">Before using **Remove-AzureRmTag** , use the *Tag* parameter of the Set-AzureRMResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>

<span data-ttu-id="d9b38-110">Il modulo tag di Azure che **rimuove-AzureRmTag** fa parte di può aiutare a gestire i tag di Azure predefiniti.</span><span class="sxs-lookup"><span data-stu-id="d9b38-110">The Azure Tags module that **Remove-AzureRmTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="d9b38-111">Un tag Azure è una coppia nome-valore che puoi usare per categorizzare le risorse e i gruppi di risorse di Azure, ad esempio per reparto o centro costo, oppure per tenere traccia di note o commenti relativi a risorse e gruppi.</span><span class="sxs-lookup"><span data-stu-id="d9b38-111">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>

<span data-ttu-id="d9b38-112">È possibile definire e applicare i tag in un singolo passaggio, ma i tag predefiniti consentono di stabilire nomi e valori standard, coerenti e prevedibili per i tag nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d9b38-112">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="d9b38-113">Se l'abbonamento include eventuali tag predefiniti, non è possibile applicare tag o valori non definiti a qualsiasi risorsa o gruppo di risorse nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d9b38-113">If the subscription includes any predefined tags, you cannot apply undefined tags or values to any resource or resource group in the subscription.</span></span>

## <span data-ttu-id="d9b38-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9b38-114">EXAMPLES</span></span>

### <span data-ttu-id="d9b38-115">Esempio 1: eliminare un tag predefinito</span><span class="sxs-lookup"><span data-stu-id="d9b38-115">Example 1: Delete a predefined tag</span></span>
```
PS C:\>Remove-AzureRmTag -Name "Department"
```

<span data-ttu-id="d9b38-116">Questo comando Elimina il nome del tag predefinito Department e tutte le relative risorse.</span><span class="sxs-lookup"><span data-stu-id="d9b38-116">This command deletes the predefined tag named Department and all of its resources.</span></span>
<span data-ttu-id="d9b38-117">Se il tag è stato applicato a qualsiasi risorsa o gruppo di risorse, il comando non riesce.</span><span class="sxs-lookup"><span data-stu-id="d9b38-117">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="d9b38-118">Esempio 2: eliminare un valore da un tag predefinito</span><span class="sxs-lookup"><span data-stu-id="d9b38-118">Example 2: Delete a value from a predefined tag</span></span>
```
PS C:\>Remove-AzureRmTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

<span data-ttu-id="d9b38-119">Questo comando Elimina il valore HumanResources dal tag Department predefinito.</span><span class="sxs-lookup"><span data-stu-id="d9b38-119">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="d9b38-120">Il tag non viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="d9b38-120">It does not delete the tag.</span></span>
<span data-ttu-id="d9b38-121">Se il valore è stato applicato a tutte le risorse o ai gruppi di risorse, il comando non riesce.</span><span class="sxs-lookup"><span data-stu-id="d9b38-121">If the value has been applied to any resources or resource groups, the command fails.</span></span>

## <span data-ttu-id="d9b38-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9b38-122">PARAMETERS</span></span>

### <span data-ttu-id="d9b38-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9b38-123">-Name</span></span>
<span data-ttu-id="d9b38-124">Specifica il nome del tag da eliminare.</span><span class="sxs-lookup"><span data-stu-id="d9b38-124">Specifies the name of the tag to be deleted.</span></span>
<span data-ttu-id="d9b38-125">Per impostazione predefinita, **Remove-AzureRmTag** rimuove il tag specificato e tutti i relativi valori.</span><span class="sxs-lookup"><span data-stu-id="d9b38-125">By default, **Remove-AzureRmTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="d9b38-126">Per eliminare i valori selezionati, ma non eliminare il tag, usa il parametro *value* .</span><span class="sxs-lookup"><span data-stu-id="d9b38-126">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

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

### <span data-ttu-id="d9b38-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9b38-127">-PassThru</span></span>
<span data-ttu-id="d9b38-128">Restituisce un oggetto che rappresenta il tag eliminato o il tag risultante con il valore deleted.</span><span class="sxs-lookup"><span data-stu-id="d9b38-128">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

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

### <span data-ttu-id="d9b38-129">-Valore</span><span class="sxs-lookup"><span data-stu-id="d9b38-129">-Value</span></span>
<span data-ttu-id="d9b38-130">Elimina i valori specificati dal tag predefinito, ma non elimina il tag.</span><span class="sxs-lookup"><span data-stu-id="d9b38-130">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9b38-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d9b38-131">-Confirm</span></span>
<span data-ttu-id="d9b38-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9b38-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9b38-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9b38-133">-WhatIf</span></span>
<span data-ttu-id="d9b38-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9b38-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9b38-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9b38-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9b38-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9b38-136">-DefaultProfile</span></span>
<span data-ttu-id="d9b38-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9b38-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9b38-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9b38-138">CommonParameters</span></span>
<span data-ttu-id="d9b38-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9b38-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9b38-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9b38-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9b38-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9b38-141">INPUTS</span></span>

### <span data-ttu-id="d9b38-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d9b38-142">None</span></span>

## <span data-ttu-id="d9b38-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9b38-143">OUTPUTS</span></span>

### <span data-ttu-id="d9b38-144">None o Microsoft. Azure. Commands. Tags. Model. PSTag</span><span class="sxs-lookup"><span data-stu-id="d9b38-144">None or Microsoft.Azure.Commands.Tags.Model.PSTag</span></span>

## <span data-ttu-id="d9b38-145">Note</span><span class="sxs-lookup"><span data-stu-id="d9b38-145">NOTES</span></span>

## <span data-ttu-id="d9b38-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9b38-146">RELATED LINKS</span></span>

[<span data-ttu-id="d9b38-147">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="d9b38-147">Get-AzureRmTag</span></span>](./Get-AzureRmTag.md)

[<span data-ttu-id="d9b38-148">New-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="d9b38-148">New-AzureRmTag</span></span>](./New-AzureRmTag.md)


