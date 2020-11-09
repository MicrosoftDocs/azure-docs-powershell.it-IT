---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: 13964bf668533aa5c1bc09b9c4eaaab83c6c421e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300703"
---
# <span data-ttu-id="c1766-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="c1766-101">Remove-AzGallery</span></span>

## <span data-ttu-id="c1766-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c1766-102">SYNOPSIS</span></span>
<span data-ttu-id="c1766-103">Eliminare una raccolta.</span><span class="sxs-lookup"><span data-stu-id="c1766-103">Delete a gallery.</span></span>

## <span data-ttu-id="c1766-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1766-104">SYNTAX</span></span>

### <span data-ttu-id="c1766-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c1766-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1766-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="c1766-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1766-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="c1766-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1766-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1766-108">DESCRIPTION</span></span>
<span data-ttu-id="c1766-109">Eliminare una raccolta.</span><span class="sxs-lookup"><span data-stu-id="c1766-109">Delete a gallery.</span></span>

## <span data-ttu-id="c1766-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1766-110">EXAMPLES</span></span>

### <span data-ttu-id="c1766-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c1766-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="c1766-112">Eliminare la raccolta specificata.</span><span class="sxs-lookup"><span data-stu-id="c1766-112">Delete the given gallery.</span></span>

## <span data-ttu-id="c1766-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c1766-113">PARAMETERS</span></span>

### <span data-ttu-id="c1766-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1766-114">-AsJob</span></span>
<span data-ttu-id="c1766-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c1766-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1766-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1766-116">-DefaultProfile</span></span>
<span data-ttu-id="c1766-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c1766-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1766-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c1766-118">-Force</span></span>
<span data-ttu-id="c1766-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c1766-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1766-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1766-120">-InputObject</span></span>
<span data-ttu-id="c1766-121">Oggetto raccolta PS</span><span class="sxs-lookup"><span data-stu-id="c1766-121">The PS Gallery Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery
Parameter Sets: ObjectParameter
Aliases: Gallery

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1766-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1766-122">-Name</span></span>
<span data-ttu-id="c1766-123">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="c1766-123">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1766-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1766-124">-ResourceGroupName</span></span>
<span data-ttu-id="c1766-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c1766-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1766-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1766-126">-ResourceId</span></span>
<span data-ttu-id="c1766-127">ID risorsa per la raccolta</span><span class="sxs-lookup"><span data-stu-id="c1766-127">The resource Id for the gallery</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1766-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c1766-128">-Confirm</span></span>
<span data-ttu-id="c1766-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1766-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1766-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1766-130">-WhatIf</span></span>
<span data-ttu-id="c1766-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c1766-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1766-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c1766-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1766-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1766-133">CommonParameters</span></span>
<span data-ttu-id="c1766-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1766-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1766-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1766-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1766-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c1766-136">INPUTS</span></span>

### <span data-ttu-id="c1766-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c1766-137">System.String</span></span>

### <span data-ttu-id="c1766-138">Microsoft. Azure. Commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="c1766-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="c1766-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1766-139">OUTPUTS</span></span>

### <span data-ttu-id="c1766-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="c1766-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="c1766-141">Note</span><span class="sxs-lookup"><span data-stu-id="c1766-141">NOTES</span></span>

## <span data-ttu-id="c1766-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1766-142">RELATED LINKS</span></span>
