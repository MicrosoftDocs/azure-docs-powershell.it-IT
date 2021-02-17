---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/remove-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
ms.openlocfilehash: ae183daeeb2e4bbc18f141c20a79be74118245c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209690"
---
# <span data-ttu-id="03b81-101">Remove-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="03b81-101">Remove-AzDevSpacesController</span></span>

## <span data-ttu-id="03b81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03b81-102">SYNOPSIS</span></span>
<span data-ttu-id="03b81-103">Eliminare un controller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="03b81-103">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="03b81-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03b81-104">SYNTAX</span></span>

### <span data-ttu-id="03b81-105">DevSpacesControllerNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="03b81-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03b81-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="03b81-106">ResourceIdParameterSet</span></span>
```
Remove-AzDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03b81-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03b81-107">InputObjectParameterSet</span></span>
```
Remove-AzDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03b81-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="03b81-108">DESCRIPTION</span></span>
<span data-ttu-id="03b81-109">Eliminare un controller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="03b81-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="03b81-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03b81-110">EXAMPLES</span></span>

### <span data-ttu-id="03b81-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="03b81-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="03b81-112">Eliminare un controller DevSpaces denominato devSpaceControllerName.</span><span class="sxs-lookup"><span data-stu-id="03b81-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="03b81-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03b81-113">PARAMETERS</span></span>

### <span data-ttu-id="03b81-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03b81-114">-AsJob</span></span>
<span data-ttu-id="03b81-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="03b81-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03b81-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03b81-116">-DefaultProfile</span></span>
<span data-ttu-id="03b81-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="03b81-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03b81-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03b81-118">-InputObject</span></span>
<span data-ttu-id="03b81-119">Un oggetto PSController, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="03b81-119">A PSController object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DevSpaces.Models.PSController
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03b81-120">-Name</span><span class="sxs-lookup"><span data-stu-id="03b81-120">-Name</span></span>
<span data-ttu-id="03b81-121">Nome del controller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="03b81-121">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b81-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03b81-122">-PassThru</span></span>
<span data-ttu-id="03b81-123">restituisce true se delete ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="03b81-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="03b81-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03b81-124">-ResourceGroupName</span></span>
<span data-ttu-id="03b81-125">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="03b81-125">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b81-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03b81-126">-ResourceId</span></span>
<span data-ttu-id="03b81-127">ID risorsa DevSpaces</span><span class="sxs-lookup"><span data-stu-id="03b81-127">The DevSpaces resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03b81-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03b81-128">-Confirm</span></span>
<span data-ttu-id="03b81-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03b81-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03b81-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03b81-130">-WhatIf</span></span>
<span data-ttu-id="03b81-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03b81-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03b81-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03b81-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03b81-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03b81-133">CommonParameters</span></span>
<span data-ttu-id="03b81-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03b81-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03b81-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03b81-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03b81-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="03b81-136">INPUTS</span></span>

### <span data-ttu-id="03b81-137">System.String</span><span class="sxs-lookup"><span data-stu-id="03b81-137">System.String</span></span>

### <span data-ttu-id="03b81-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="03b81-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="03b81-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03b81-139">OUTPUTS</span></span>

### <span data-ttu-id="03b81-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="03b81-140">System.Boolean</span></span>

## <span data-ttu-id="03b81-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="03b81-141">NOTES</span></span>

## <span data-ttu-id="03b81-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03b81-142">RELATED LINKS</span></span>
