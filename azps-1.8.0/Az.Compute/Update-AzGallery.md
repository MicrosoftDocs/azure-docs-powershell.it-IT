---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGallery.md
ms.openlocfilehash: 1f6773aafbb717387d2d1a984db03e4d2739194f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684667"
---
# <span data-ttu-id="a9c64-101">Update-AzGallery</span><span class="sxs-lookup"><span data-stu-id="a9c64-101">Update-AzGallery</span></span>

## <span data-ttu-id="a9c64-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a9c64-102">SYNOPSIS</span></span>
<span data-ttu-id="a9c64-103">Aggiornare una raccolta.</span><span class="sxs-lookup"><span data-stu-id="a9c64-103">Update a gallery.</span></span>

## <span data-ttu-id="a9c64-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9c64-104">SYNTAX</span></span>

### <span data-ttu-id="a9c64-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a9c64-105">DefaultParameter (Default)</span></span>
```
Update-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Description <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9c64-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="a9c64-106">ResourceIdParameter</span></span>
```
Update-AzGallery [-ResourceId] <String> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9c64-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="a9c64-107">ObjectParameter</span></span>
```
Update-AzGallery [-InputObject] <PSGallery> [-AsJob] [-Description <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9c64-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9c64-108">DESCRIPTION</span></span>
<span data-ttu-id="a9c64-109">Aggiornare una raccolta.</span><span class="sxs-lookup"><span data-stu-id="a9c64-109">Update a gallery.</span></span>

## <span data-ttu-id="a9c64-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9c64-110">EXAMPLES</span></span>

### <span data-ttu-id="a9c64-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a9c64-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGallery -ResourceGroupName $rgname -Name $galleryName -Description $galleryDescription
```

<span data-ttu-id="a9c64-112">Aggiornare una raccolta.</span><span class="sxs-lookup"><span data-stu-id="a9c64-112">Update a gallery.</span></span>

## <span data-ttu-id="a9c64-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a9c64-113">PARAMETERS</span></span>

### <span data-ttu-id="a9c64-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9c64-114">-AsJob</span></span>
<span data-ttu-id="a9c64-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a9c64-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a9c64-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9c64-116">-DefaultProfile</span></span>
<span data-ttu-id="a9c64-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a9c64-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9c64-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9c64-118">-Description</span></span>
<span data-ttu-id="a9c64-119">Descrizione della risorsa della raccolta.</span><span class="sxs-lookup"><span data-stu-id="a9c64-119">The description of the gallery resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9c64-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9c64-120">-InputObject</span></span>
<span data-ttu-id="a9c64-121">Oggetto raccolta PS.</span><span class="sxs-lookup"><span data-stu-id="a9c64-121">The PS Gallery Object.</span></span>

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

### <span data-ttu-id="a9c64-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a9c64-122">-Name</span></span>
<span data-ttu-id="a9c64-123">Nome della raccolta.</span><span class="sxs-lookup"><span data-stu-id="a9c64-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="a9c64-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9c64-124">-ResourceGroupName</span></span>
<span data-ttu-id="a9c64-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a9c64-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="a9c64-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9c64-126">-ResourceId</span></span>
<span data-ttu-id="a9c64-127">ID risorsa per la raccolta</span><span class="sxs-lookup"><span data-stu-id="a9c64-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="a9c64-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="a9c64-128">-Tag</span></span>
<span data-ttu-id="a9c64-129">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="a9c64-129">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9c64-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a9c64-130">-Confirm</span></span>
<span data-ttu-id="a9c64-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9c64-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9c64-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9c64-132">-WhatIf</span></span>
<span data-ttu-id="a9c64-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9c64-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9c64-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9c64-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9c64-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9c64-135">CommonParameters</span></span>
<span data-ttu-id="a9c64-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9c64-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9c64-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9c64-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9c64-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a9c64-138">INPUTS</span></span>

### <span data-ttu-id="a9c64-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a9c64-139">System.String</span></span>

### <span data-ttu-id="a9c64-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="a9c64-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

### <span data-ttu-id="a9c64-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a9c64-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a9c64-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9c64-142">OUTPUTS</span></span>

### <span data-ttu-id="a9c64-143">Microsoft. Azure. Commands. Compute. Automation. Models. PSGallery</span><span class="sxs-lookup"><span data-stu-id="a9c64-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="a9c64-144">Note</span><span class="sxs-lookup"><span data-stu-id="a9c64-144">NOTES</span></span>

## <span data-ttu-id="a9c64-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9c64-145">RELATED LINKS</span></span>
