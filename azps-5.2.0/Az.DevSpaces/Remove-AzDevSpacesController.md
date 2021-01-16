---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/remove-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
ms.openlocfilehash: ae183daeeb2e4bbc18f141c20a79be74118245c0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328896"
---
# <span data-ttu-id="efc18-101">Remove-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="efc18-101">Remove-AzDevSpacesController</span></span>

## <span data-ttu-id="efc18-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="efc18-102">SYNOPSIS</span></span>
<span data-ttu-id="efc18-103">Eliminare un controller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="efc18-103">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="efc18-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="efc18-104">SYNTAX</span></span>

### <span data-ttu-id="efc18-105">DevSpacesControllerNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="efc18-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efc18-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="efc18-106">ResourceIdParameterSet</span></span>
```
Remove-AzDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efc18-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="efc18-107">InputObjectParameterSet</span></span>
```
Remove-AzDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efc18-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="efc18-108">DESCRIPTION</span></span>
<span data-ttu-id="efc18-109">Eliminare un controller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="efc18-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="efc18-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="efc18-110">EXAMPLES</span></span>

### <span data-ttu-id="efc18-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="efc18-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="efc18-112">Eliminare un controller DevSpaces denominato devSpaceControllerName.</span><span class="sxs-lookup"><span data-stu-id="efc18-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="efc18-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="efc18-113">PARAMETERS</span></span>

### <span data-ttu-id="efc18-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="efc18-114">-AsJob</span></span>
<span data-ttu-id="efc18-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="efc18-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="efc18-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efc18-116">-DefaultProfile</span></span>
<span data-ttu-id="efc18-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="efc18-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efc18-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efc18-118">-InputObject</span></span>
<span data-ttu-id="efc18-119">Un oggetto PSController, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="efc18-119">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="efc18-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="efc18-120">-Name</span></span>
<span data-ttu-id="efc18-121">Nome del controller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="efc18-121">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="efc18-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="efc18-122">-PassThru</span></span>
<span data-ttu-id="efc18-123">Restituisce vero se l'eliminazione è riuscita</span><span class="sxs-lookup"><span data-stu-id="efc18-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="efc18-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efc18-124">-ResourceGroupName</span></span>
<span data-ttu-id="efc18-125">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="efc18-125">Resource group name</span></span>

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

### <span data-ttu-id="efc18-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="efc18-126">-ResourceId</span></span>
<span data-ttu-id="efc18-127">ID risorsa DevSpaces</span><span class="sxs-lookup"><span data-stu-id="efc18-127">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="efc18-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="efc18-128">-Confirm</span></span>
<span data-ttu-id="efc18-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efc18-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efc18-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efc18-130">-WhatIf</span></span>
<span data-ttu-id="efc18-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="efc18-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efc18-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="efc18-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efc18-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc18-133">CommonParameters</span></span>
<span data-ttu-id="efc18-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efc18-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc18-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efc18-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc18-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="efc18-136">INPUTS</span></span>

### <span data-ttu-id="efc18-137">System. String</span><span class="sxs-lookup"><span data-stu-id="efc18-137">System.String</span></span>

### <span data-ttu-id="efc18-138">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="efc18-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="efc18-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="efc18-139">OUTPUTS</span></span>

### <span data-ttu-id="efc18-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="efc18-140">System.Boolean</span></span>

## <span data-ttu-id="efc18-141">Note</span><span class="sxs-lookup"><span data-stu-id="efc18-141">NOTES</span></span>

## <span data-ttu-id="efc18-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="efc18-142">RELATED LINKS</span></span>
