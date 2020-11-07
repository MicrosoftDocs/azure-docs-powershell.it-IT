---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/remove-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
ms.openlocfilehash: 1c7f55bb3f84051326cd102c1c12a2d978a79f71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688046"
---
# <span data-ttu-id="040c4-101">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="040c4-101">Remove-AzureRmTag</span></span>

## <span data-ttu-id="040c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="040c4-102">SYNOPSIS</span></span>
<span data-ttu-id="040c4-103">Elimina i valori o i tag di Azure predefiniti.</span><span class="sxs-lookup"><span data-stu-id="040c4-103">Deletes predefined Azure tags or values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="040c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="040c4-104">SYNTAX</span></span>

```
Remove-AzureRmTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="040c4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="040c4-105">DESCRIPTION</span></span>
<span data-ttu-id="040c4-106">Il cmdlet **Remove-AzureRmTag** Elimina i tag e i valori di Azure predefiniti dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="040c4-106">The **Remove-AzureRmTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="040c4-107">Per eliminare valori particolari da un tag predefinito, usare il parametro *value* .</span><span class="sxs-lookup"><span data-stu-id="040c4-107">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="040c4-108">Per impostazione predefinita, **Remove-AzureRmTag** Elimina il tag specificato e tutti i relativi valori. Non è possibile eliminare un tag o un valore attualmente applicato a una risorsa o a un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="040c4-108">By default, **Remove-AzureRmTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="040c4-109">Prima di usare **Remove-AzureRmTag** , usa il parametro *tag* del cmdlet Set-AzureRMResourceGroup per eliminare il tag o i valori dal gruppo Resource o Resource.</span><span class="sxs-lookup"><span data-stu-id="040c4-109">Before using **Remove-AzureRmTag** , use the *Tag* parameter of the Set-AzureRMResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="040c4-110">Il modulo tag di Azure che **rimuove-AzureRmTag** fa parte di può aiutare a gestire i tag di Azure predefiniti.</span><span class="sxs-lookup"><span data-stu-id="040c4-110">The Azure Tags module that **Remove-AzureRmTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="040c4-111">Un tag Azure è una coppia nome-valore che puoi usare per categorizzare le risorse e i gruppi di risorse di Azure, ad esempio per reparto o centro costo, oppure per tenere traccia di note o commenti relativi a risorse e gruppi.</span><span class="sxs-lookup"><span data-stu-id="040c4-111">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="040c4-112">È possibile definire e applicare i tag in un singolo passaggio, ma i tag predefiniti consentono di stabilire nomi e valori standard, coerenti e prevedibili per i tag nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="040c4-112">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

## <span data-ttu-id="040c4-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="040c4-113">EXAMPLES</span></span>

### <span data-ttu-id="040c4-114">Esempio 1: eliminare un tag predefinito</span><span class="sxs-lookup"><span data-stu-id="040c4-114">Example 1: Delete a predefined tag</span></span>
```
PS C:\>Remove-AzureRmTag -Name "Department"
```

<span data-ttu-id="040c4-115">Questo comando Elimina il nome del tag predefinito Department e tutte le relative risorse.</span><span class="sxs-lookup"><span data-stu-id="040c4-115">This command deletes the predefined tag named Department and all of its resources.</span></span>
<span data-ttu-id="040c4-116">Se il tag è stato applicato a qualsiasi risorsa o gruppo di risorse, il comando non riesce.</span><span class="sxs-lookup"><span data-stu-id="040c4-116">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="040c4-117">Esempio 2: eliminare un valore da un tag predefinito</span><span class="sxs-lookup"><span data-stu-id="040c4-117">Example 2: Delete a value from a predefined tag</span></span>
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

<span data-ttu-id="040c4-118">Questo comando Elimina il valore HumanResources dal tag Department predefinito.</span><span class="sxs-lookup"><span data-stu-id="040c4-118">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="040c4-119">Il tag non viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="040c4-119">It does not delete the tag.</span></span>
<span data-ttu-id="040c4-120">Se il valore è stato applicato a tutte le risorse o ai gruppi di risorse, il comando non riesce.</span><span class="sxs-lookup"><span data-stu-id="040c4-120">If the value has been applied to any resources or resource groups, the command fails.</span></span>

## <span data-ttu-id="040c4-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="040c4-121">PARAMETERS</span></span>

### <span data-ttu-id="040c4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="040c4-122">-DefaultProfile</span></span>
<span data-ttu-id="040c4-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="040c4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="040c4-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="040c4-124">-Name</span></span>
<span data-ttu-id="040c4-125">Specifica il nome del tag da eliminare.</span><span class="sxs-lookup"><span data-stu-id="040c4-125">Specifies the name of the tag to be deleted.</span></span>
<span data-ttu-id="040c4-126">Per impostazione predefinita, **Remove-AzureRmTag** rimuove il tag specificato e tutti i relativi valori.</span><span class="sxs-lookup"><span data-stu-id="040c4-126">By default, **Remove-AzureRmTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="040c4-127">Per eliminare i valori selezionati, ma non eliminare il tag, usa il parametro *value* .</span><span class="sxs-lookup"><span data-stu-id="040c4-127">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

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

### <span data-ttu-id="040c4-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="040c4-128">-PassThru</span></span>
<span data-ttu-id="040c4-129">Restituisce un oggetto che rappresenta il tag eliminato o il tag risultante con il valore deleted.</span><span class="sxs-lookup"><span data-stu-id="040c4-129">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

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

### <span data-ttu-id="040c4-130">-Valore</span><span class="sxs-lookup"><span data-stu-id="040c4-130">-Value</span></span>
<span data-ttu-id="040c4-131">Elimina i valori specificati dal tag predefinito, ma non elimina il tag.</span><span class="sxs-lookup"><span data-stu-id="040c4-131">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

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

### <span data-ttu-id="040c4-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="040c4-132">-Confirm</span></span>
<span data-ttu-id="040c4-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="040c4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="040c4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="040c4-134">-WhatIf</span></span>
<span data-ttu-id="040c4-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="040c4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="040c4-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="040c4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="040c4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="040c4-137">CommonParameters</span></span>
<span data-ttu-id="040c4-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="040c4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="040c4-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="040c4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="040c4-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="040c4-140">INPUTS</span></span>

### <span data-ttu-id="040c4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="040c4-141">System.String</span></span>

### <span data-ttu-id="040c4-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="040c4-142">System.String[]</span></span>

### <span data-ttu-id="040c4-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="040c4-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="040c4-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="040c4-144">OUTPUTS</span></span>

### <span data-ttu-id="040c4-145">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag</span><span class="sxs-lookup"><span data-stu-id="040c4-145">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="040c4-146">Note</span><span class="sxs-lookup"><span data-stu-id="040c4-146">NOTES</span></span>

## <span data-ttu-id="040c4-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="040c4-147">RELATED LINKS</span></span>

[<span data-ttu-id="040c4-148">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="040c4-148">Get-AzureRmTag</span></span>](./Get-AzureRmTag.md)

[<span data-ttu-id="040c4-149">New-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="040c4-149">New-AzureRmTag</span></span>](./New-AzureRmTag.md)


