---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/remove-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
ms.openlocfilehash: b6fb42ccafe5b70316ea29251a87b76ea65dda7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674580"
---
# <span data-ttu-id="a99b5-101">Remove-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="a99b5-101">Remove-AzDevSpacesController</span></span>

## <span data-ttu-id="a99b5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a99b5-102">SYNOPSIS</span></span>
<span data-ttu-id="a99b5-103">Eliminare un controller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="a99b5-103">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="a99b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a99b5-104">SYNTAX</span></span>

### <span data-ttu-id="a99b5-105">DevSpacesControllerNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a99b5-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a99b5-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a99b5-106">ResourceIdParameterSet</span></span>
```
Remove-AzDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a99b5-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a99b5-107">InputObjectParameterSet</span></span>
```
Remove-AzDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a99b5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a99b5-108">DESCRIPTION</span></span>
<span data-ttu-id="a99b5-109">Eliminare un controller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="a99b5-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="a99b5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a99b5-110">EXAMPLES</span></span>

### <span data-ttu-id="a99b5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a99b5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="a99b5-112">Eliminare un controller DevSpaces denominato devSpaceControllerName.</span><span class="sxs-lookup"><span data-stu-id="a99b5-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="a99b5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a99b5-113">PARAMETERS</span></span>

### <span data-ttu-id="a99b5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a99b5-114">-AsJob</span></span>
<span data-ttu-id="a99b5-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a99b5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a99b5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a99b5-116">-DefaultProfile</span></span>
<span data-ttu-id="a99b5-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a99b5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a99b5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a99b5-118">-InputObject</span></span>
<span data-ttu-id="a99b5-119">Un oggetto PSController, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="a99b5-119">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="a99b5-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a99b5-120">-Name</span></span>
<span data-ttu-id="a99b5-121">Nome del controller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="a99b5-121">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="a99b5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a99b5-122">-PassThru</span></span>
<span data-ttu-id="a99b5-123">Restituisce vero se l'eliminazione è riuscita</span><span class="sxs-lookup"><span data-stu-id="a99b5-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="a99b5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a99b5-124">-ResourceGroupName</span></span>
<span data-ttu-id="a99b5-125">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="a99b5-125">Resource group name</span></span>

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

### <span data-ttu-id="a99b5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a99b5-126">-ResourceId</span></span>
<span data-ttu-id="a99b5-127">ID risorsa DevSpaces</span><span class="sxs-lookup"><span data-stu-id="a99b5-127">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="a99b5-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a99b5-128">-Confirm</span></span>
<span data-ttu-id="a99b5-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a99b5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a99b5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a99b5-130">-WhatIf</span></span>
<span data-ttu-id="a99b5-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a99b5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a99b5-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a99b5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a99b5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a99b5-133">CommonParameters</span></span>
<span data-ttu-id="a99b5-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a99b5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a99b5-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a99b5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a99b5-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a99b5-136">INPUTS</span></span>

### <span data-ttu-id="a99b5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a99b5-137">System.String</span></span>

### <span data-ttu-id="a99b5-138">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="a99b5-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="a99b5-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a99b5-139">OUTPUTS</span></span>

### <span data-ttu-id="a99b5-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a99b5-140">System.Boolean</span></span>

## <span data-ttu-id="a99b5-141">Note</span><span class="sxs-lookup"><span data-stu-id="a99b5-141">NOTES</span></span>

## <span data-ttu-id="a99b5-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a99b5-142">RELATED LINKS</span></span>