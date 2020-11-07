---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/remove-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Remove-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Remove-AzureRmDevSpacesController.md
ms.openlocfilehash: e242ba95330ac102fbfbcecf6f28326adb29a057
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687597"
---
# <span data-ttu-id="7c8d9-101">Remove-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="7c8d9-101">Remove-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="7c8d9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c8d9-102">SYNOPSIS</span></span>
<span data-ttu-id="7c8d9-103">Eliminare un controller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="7c8d9-103">Delete a DevSpaces controller.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c8d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c8d9-104">SYNTAX</span></span>

### <span data-ttu-id="7c8d9-105">DevSpacesControllerNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7c8d9-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c8d9-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c8d9-106">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c8d9-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c8d9-107">InputObjectParameterSet</span></span>
```
Remove-AzureRmDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c8d9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c8d9-108">DESCRIPTION</span></span>
<span data-ttu-id="7c8d9-109">Eliminare un controller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="7c8d9-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="7c8d9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c8d9-110">EXAMPLES</span></span>

### <span data-ttu-id="7c8d9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7c8d9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="7c8d9-112">Eliminare un controller DevSpaces denominato devSpaceControllerName.</span><span class="sxs-lookup"><span data-stu-id="7c8d9-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="7c8d9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c8d9-113">PARAMETERS</span></span>

### <span data-ttu-id="7c8d9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c8d9-114">-AsJob</span></span>
<span data-ttu-id="7c8d9-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7c8d9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c8d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c8d9-116">-DefaultProfile</span></span>
<span data-ttu-id="7c8d9-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c8d9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c8d9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c8d9-118">-InputObject</span></span>
<span data-ttu-id="7c8d9-119">Un oggetto PSController, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="7c8d9-119">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="7c8d9-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="7c8d9-120">-Name</span></span>
<span data-ttu-id="7c8d9-121">Nome del controller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="7c8d9-121">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="7c8d9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c8d9-122">-PassThru</span></span>
<span data-ttu-id="7c8d9-123">Restituisce vero se l'eliminazione è riuscita</span><span class="sxs-lookup"><span data-stu-id="7c8d9-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="7c8d9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c8d9-124">-ResourceGroupName</span></span>
<span data-ttu-id="7c8d9-125">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="7c8d9-125">Resource group name</span></span>

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

### <span data-ttu-id="7c8d9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c8d9-126">-ResourceId</span></span>
<span data-ttu-id="7c8d9-127">ID risorsa DevSpaces</span><span class="sxs-lookup"><span data-stu-id="7c8d9-127">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="7c8d9-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7c8d9-128">-Confirm</span></span>
<span data-ttu-id="7c8d9-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c8d9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c8d9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c8d9-130">-WhatIf</span></span>
<span data-ttu-id="7c8d9-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c8d9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c8d9-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c8d9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c8d9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c8d9-133">CommonParameters</span></span>
<span data-ttu-id="7c8d9-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c8d9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c8d9-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c8d9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c8d9-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c8d9-136">INPUTS</span></span>

### <span data-ttu-id="7c8d9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7c8d9-137">System.String</span></span>

### <span data-ttu-id="7c8d9-138">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="7c8d9-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>
<span data-ttu-id="7c8d9-139">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7c8d9-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="7c8d9-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c8d9-140">OUTPUTS</span></span>

### <span data-ttu-id="7c8d9-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7c8d9-141">System.Boolean</span></span>

## <span data-ttu-id="7c8d9-142">Note</span><span class="sxs-lookup"><span data-stu-id="7c8d9-142">NOTES</span></span>

## <span data-ttu-id="7c8d9-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c8d9-143">RELATED LINKS</span></span>
