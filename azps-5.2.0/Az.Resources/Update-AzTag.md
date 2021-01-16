---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 07c6e327-05f4-4279-a5fb-d4e860c897d4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
ms.openlocfilehash: 3423331e36fd9fbd636a1ae877275badd5912324
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333895"
---
# <span data-ttu-id="bddd8-101">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="bddd8-101">Update-AzTag</span></span>

## <span data-ttu-id="bddd8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bddd8-102">SYNOPSIS</span></span>

<span data-ttu-id="bddd8-103">Aggiorna in modo selettivo il set di tag in una risorsa o un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="bddd8-103">Selectively updates the set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="bddd8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bddd8-104">SYNTAX</span></span>

```powershell
Update-AzTag
   -ResourceId <String>
   -Operation <TagPatchOperation>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]

```

## <span data-ttu-id="bddd8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bddd8-105">DESCRIPTION</span></span>

<span data-ttu-id="bddd8-106">Il cmdlet **Update-AzTag** con un **resourceId** aggiorna in modo selettivo il set di tag in una risorsa o un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="bddd8-106">The **Update-AzTag** cmdlet with a **ResourceId** selectively updates the set of tags on a resource or subscription.</span></span>
<span data-ttu-id="bddd8-107">Questa operazione consente di sostituire, unire o eliminare selettivamente i tag nella risorsa o nell'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="bddd8-107">This operation allows replacing, merging or selectively deleting tags on the specified resource or subscription.</span></span> <span data-ttu-id="bddd8-108">L'entità specificata può avere un massimo di 50 tag alla fine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="bddd8-108">The specified entity can have a maximum of 50 tags at the end of the operation.</span></span> <span data-ttu-id="bddd8-109">L'opzione ' Sostituisci ' sostituisce l'intero set di tag esistenti con un nuovo set.</span><span class="sxs-lookup"><span data-stu-id="bddd8-109">The 'replace' option replaces the entire set of existing tags with a new set.</span></span> <span data-ttu-id="bddd8-110">L'opzione "Unisci" consente di aggiungere tag con nuovi nomi e di aggiornare i valori dei tag con nomi esistenti.</span><span class="sxs-lookup"><span data-stu-id="bddd8-110">The 'merge' option allows adding tags with new names and updating the values of tags with existing names.</span></span> <span data-ttu-id="bddd8-111">L'opzione "Elimina" consente di eliminare selettivamente i tag in base a nomi o coppie nome/valore specificati.</span><span class="sxs-lookup"><span data-stu-id="bddd8-111">The 'delete' option allows selectively deleting tags based on given names or name/value pairs.</span></span>

## <span data-ttu-id="bddd8-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bddd8-112">EXAMPLES</span></span>

### <span data-ttu-id="bddd8-113">Esempio 1: Aggiorna selettivamente il set di tag in un abbonamento con l'operazione "merge"</span><span class="sxs-lookup"><span data-stu-id="bddd8-113">Example 1: Selectively updates the set of tags on a subscription with "Merge" Operation</span></span>

```powershell
PS C:\>$mergedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $mergedTags -Operation Merge

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key2     value2
             key3     value3
```

<span data-ttu-id="bddd8-114">Questo comando unisce il set di tag nell'abbonamento con {subId}.</span><span class="sxs-lookup"><span data-stu-id="bddd8-114">This command Merges the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="bddd8-115">Esempio 2: Aggiorna in modo selettivo il set di tag in un abbonamento con l'operazione "Sostituisci"</span><span class="sxs-lookup"><span data-stu-id="bddd8-115">Example 2: Selectively updates the set of tags on a subscription with "Replace" Operation</span></span>

```powershell
PS C:\>$replacedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $replacedTags -Operation Replace

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key3     value3
```

<span data-ttu-id="bddd8-116">Questo comando Repalces il set di tag nell'abbonamento con {subId}.</span><span class="sxs-lookup"><span data-stu-id="bddd8-116">This command Repalces the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="bddd8-117">Esempio 3: Aggiorna in modo selettivo il set di tag in un abbonamento con l'operazione "Delete"</span><span class="sxs-lookup"><span data-stu-id="bddd8-117">Example 3: Selectively updates the set of tags on a subscription with "Delete" Operation</span></span>

```powershell
PS C:\>$deletedTags = @{"key1"="value1"}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $deletedTags -Operation Delete

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key3     value3
```

<span data-ttu-id="bddd8-118">Questo comando Elimina il set di tag nell'abbonamento con {subId}.</span><span class="sxs-lookup"><span data-stu-id="bddd8-118">This command Deletes the set of tags on the subscription with {subId}.</span></span>

## <span data-ttu-id="bddd8-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bddd8-119">PARAMETERS</span></span>

### <span data-ttu-id="bddd8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bddd8-120">-DefaultProfile</span></span>
<span data-ttu-id="bddd8-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bddd8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bddd8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bddd8-122">-ResourceId</span></span>
<span data-ttu-id="bddd8-123">Identificatore delle risorse per l'entità Tagged.</span><span class="sxs-lookup"><span data-stu-id="bddd8-123">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="bddd8-124">Una risorsa, un gruppo di risorse o un abbonamento possono essere contrassegnati.</span><span class="sxs-lookup"><span data-stu-id="bddd8-124">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bddd8-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="bddd8-125">-Tag</span></span>
<span data-ttu-id="bddd8-126">Set di tag da usare per Update.</span><span class="sxs-lookup"><span data-stu-id="bddd8-126">The set of tags to use for update.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bddd8-127">-Operazione</span><span class="sxs-lookup"><span data-stu-id="bddd8-127">-Operation</span></span>
<span data-ttu-id="bddd8-128">Operazione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="bddd8-128">The update operation.</span></span> <span data-ttu-id="bddd8-129">Le opzioni sono merge, Sostituisci ed Elimina.</span><span class="sxs-lookup"><span data-stu-id="bddd8-129">Options are Merge, Replace and Delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Tags.Model.TagPatchOperation
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bddd8-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bddd8-130">-Confirm</span></span>
<span data-ttu-id="bddd8-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bddd8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bddd8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bddd8-132">-WhatIf</span></span>
<span data-ttu-id="bddd8-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bddd8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bddd8-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bddd8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bddd8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bddd8-135">CommonParameters</span></span>
<span data-ttu-id="bddd8-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bddd8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bddd8-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bddd8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bddd8-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bddd8-138">INPUTS</span></span>

### <span data-ttu-id="bddd8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bddd8-139">System.String</span></span>

### <span data-ttu-id="bddd8-140">Microsoft. Azure. Commands. Tags. Model. TagPatchOperation</span><span class="sxs-lookup"><span data-stu-id="bddd8-140">Microsoft.Azure.Commands.Tags.Model.TagPatchOperation</span></span>

### <span data-ttu-id="bddd8-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bddd8-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bddd8-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bddd8-142">OUTPUTS</span></span>

### <span data-ttu-id="bddd8-143">Microsoft. Azure. Commands. Tags. Model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="bddd8-143">Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="bddd8-144">Note</span><span class="sxs-lookup"><span data-stu-id="bddd8-144">NOTES</span></span>

## <span data-ttu-id="bddd8-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bddd8-145">RELATED LINKS</span></span>

[<span data-ttu-id="bddd8-146">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="bddd8-146">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="bddd8-147">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="bddd8-147">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="bddd8-148">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="bddd8-148">Remove-AzTag</span></span>](./Remove-AzTag.md)
