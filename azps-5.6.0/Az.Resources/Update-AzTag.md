---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 07c6e327-05f4-4279-a5fb-d4e860c897d4
online version: https://docs.microsoft.com/powershell/module/az.resources/update-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
ms.openlocfilehash: acf97f282e50d9c6f468e400cb2a5c598fe06659
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997133"
---
# <span data-ttu-id="7cd85-101">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="7cd85-101">Update-AzTag</span></span>

## <span data-ttu-id="7cd85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cd85-102">SYNOPSIS</span></span>

<span data-ttu-id="7cd85-103">Aggiornare in modo selettivo il set di tag per una risorsa o un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7cd85-103">Selectively updates the set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="7cd85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7cd85-104">SYNTAX</span></span>

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

## <span data-ttu-id="7cd85-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7cd85-105">DESCRIPTION</span></span>

<span data-ttu-id="7cd85-106">Il cmdlet **Update-AzTag** con **un valore ResourceId** aggiorna in modo selettivo il set di tag per una risorsa o un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7cd85-106">The **Update-AzTag** cmdlet with a **ResourceId** selectively updates the set of tags on a resource or subscription.</span></span>
<span data-ttu-id="7cd85-107">Questa operazione consente di sostituire, unire o eliminare in modo selettivo i tag nella risorsa o nella sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="7cd85-107">This operation allows replacing, merging or selectively deleting tags on the specified resource or subscription.</span></span> <span data-ttu-id="7cd85-108">L'entità specificata può avere un massimo di 50 tag alla fine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="7cd85-108">The specified entity can have a maximum of 50 tags at the end of the operation.</span></span> <span data-ttu-id="7cd85-109">L'opzione "sostituisci" sostituisce l'intero set di tag esistenti con un nuovo set.</span><span class="sxs-lookup"><span data-stu-id="7cd85-109">The 'replace' option replaces the entire set of existing tags with a new set.</span></span> <span data-ttu-id="7cd85-110">L'opzione 'unisci' consente di aggiungere tag con nuovi nomi e aggiornare i valori dei tag con nomi esistenti.</span><span class="sxs-lookup"><span data-stu-id="7cd85-110">The 'merge' option allows adding tags with new names and updating the values of tags with existing names.</span></span> <span data-ttu-id="7cd85-111">L'opzione "elimina" consente di eliminare in modo selettivo i tag in base a nomi o coppie nome/valore specificate.</span><span class="sxs-lookup"><span data-stu-id="7cd85-111">The 'delete' option allows selectively deleting tags based on given names or name/value pairs.</span></span>

## <span data-ttu-id="7cd85-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7cd85-112">EXAMPLES</span></span>

### <span data-ttu-id="7cd85-113">Esempio 1: Aggiornare in modo selettivo il set di tag in un abbonamento con l'operazione "Merge"</span><span class="sxs-lookup"><span data-stu-id="7cd85-113">Example 1: Selectively updates the set of tags on a subscription with "Merge" Operation</span></span>

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

<span data-ttu-id="7cd85-114">Questo comando unisce il set di tag dell'abbonamento con {subId}.</span><span class="sxs-lookup"><span data-stu-id="7cd85-114">This command Merges the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="7cd85-115">Esempio 2: Aggiornare in modo selettivo il set di tag in un abbonamento con l'operazione "Sostituisci"</span><span class="sxs-lookup"><span data-stu-id="7cd85-115">Example 2: Selectively updates the set of tags on a subscription with "Replace" Operation</span></span>

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

<span data-ttu-id="7cd85-116">Questo comando riordina il set di tag nell'abbonamento con {subId}.</span><span class="sxs-lookup"><span data-stu-id="7cd85-116">This command Repalces the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="7cd85-117">Esempio 3: Aggiornare in modo selettivo il set di tag in un abbonamento con l'operazione "Elimina"</span><span class="sxs-lookup"><span data-stu-id="7cd85-117">Example 3: Selectively updates the set of tags on a subscription with "Delete" Operation</span></span>

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

<span data-ttu-id="7cd85-118">Questo comando elimina il set di tag nell'abbonamento con {subId}.</span><span class="sxs-lookup"><span data-stu-id="7cd85-118">This command Deletes the set of tags on the subscription with {subId}.</span></span>

## <span data-ttu-id="7cd85-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cd85-119">PARAMETERS</span></span>

### <span data-ttu-id="7cd85-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cd85-120">-DefaultProfile</span></span>
<span data-ttu-id="7cd85-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7cd85-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cd85-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cd85-122">-ResourceId</span></span>
<span data-ttu-id="7cd85-123">Identificatore di risorsa per l'entità con tag.</span><span class="sxs-lookup"><span data-stu-id="7cd85-123">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="7cd85-124">Una risorsa, un gruppo di risorse o una sottoscrizione può essere contrassegnata.</span><span class="sxs-lookup"><span data-stu-id="7cd85-124">A resource, a resource group or a subscription may be tagged.</span></span>

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

### <span data-ttu-id="7cd85-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="7cd85-125">-Tag</span></span>
<span data-ttu-id="7cd85-126">Insieme di tag da usare per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="7cd85-126">The set of tags to use for update.</span></span>

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

### <span data-ttu-id="7cd85-127">-Operazione</span><span class="sxs-lookup"><span data-stu-id="7cd85-127">-Operation</span></span>
<span data-ttu-id="7cd85-128">Operazione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="7cd85-128">The update operation.</span></span> <span data-ttu-id="7cd85-129">Le opzioni sono Unisci, Sostituisci ed Elimina.</span><span class="sxs-lookup"><span data-stu-id="7cd85-129">Options are Merge, Replace and Delete.</span></span>

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

### <span data-ttu-id="7cd85-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cd85-130">-Confirm</span></span>
<span data-ttu-id="7cd85-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cd85-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cd85-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cd85-132">-WhatIf</span></span>
<span data-ttu-id="7cd85-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7cd85-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cd85-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7cd85-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cd85-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cd85-135">CommonParameters</span></span>
<span data-ttu-id="7cd85-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cd85-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cd85-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7cd85-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cd85-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="7cd85-138">INPUTS</span></span>

### <span data-ttu-id="7cd85-139">System.String</span><span class="sxs-lookup"><span data-stu-id="7cd85-139">System.String</span></span>

### <span data-ttu-id="7cd85-140">Microsoft.Azure.Commands.Tags.Model.TagPatchOperation</span><span class="sxs-lookup"><span data-stu-id="7cd85-140">Microsoft.Azure.Commands.Tags.Model.TagPatchOperation</span></span>

### <span data-ttu-id="7cd85-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7cd85-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7cd85-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7cd85-142">OUTPUTS</span></span>

### <span data-ttu-id="7cd85-143">Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="7cd85-143">Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="7cd85-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="7cd85-144">NOTES</span></span>

## <span data-ttu-id="7cd85-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7cd85-145">RELATED LINKS</span></span>

[<span data-ttu-id="7cd85-146">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="7cd85-146">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="7cd85-147">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="7cd85-147">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="7cd85-148">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="7cd85-148">Remove-AzTag</span></span>](./Remove-AzTag.md)
