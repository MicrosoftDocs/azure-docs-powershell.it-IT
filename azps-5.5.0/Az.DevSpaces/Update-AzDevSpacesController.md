---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: 9de9f5e5870aed99a9ef7203bfea4797e78e5f8c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204210"
---
# <span data-ttu-id="2ef09-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="2ef09-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="2ef09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ef09-102">SYNOPSIS</span></span>
<span data-ttu-id="2ef09-103">Aggiorna il controller DevSpaces per aggiungere tag.</span><span class="sxs-lookup"><span data-stu-id="2ef09-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="2ef09-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ef09-104">SYNTAX</span></span>

### <span data-ttu-id="2ef09-105">DevSpacesControllerNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2ef09-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ef09-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ef09-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ef09-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ef09-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ef09-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2ef09-108">DESCRIPTION</span></span>
<span data-ttu-id="2ef09-109">Aggiorna il controller DevSpaces per aggiungere tag.</span><span class="sxs-lookup"><span data-stu-id="2ef09-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="2ef09-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ef09-110">EXAMPLES</span></span>

### <span data-ttu-id="2ef09-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2ef09-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="2ef09-112">Aggiungere tag a un controller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="2ef09-112">Tag a DevSpaces controller.</span></span>

## <span data-ttu-id="2ef09-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ef09-113">PARAMETERS</span></span>

### <span data-ttu-id="2ef09-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ef09-114">-DefaultProfile</span></span>
<span data-ttu-id="2ef09-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2ef09-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ef09-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ef09-116">-InputObject</span></span>
<span data-ttu-id="2ef09-117">Un oggetto PSController, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="2ef09-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="2ef09-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2ef09-118">-Name</span></span>
<span data-ttu-id="2ef09-119">Nome del controller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="2ef09-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="2ef09-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ef09-120">-ResourceGroupName</span></span>
<span data-ttu-id="2ef09-121">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="2ef09-121">Resource group name</span></span>

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

### <span data-ttu-id="2ef09-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ef09-122">-ResourceId</span></span>
<span data-ttu-id="2ef09-123">ID risorsa DevSpaces</span><span class="sxs-lookup"><span data-stu-id="2ef09-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="2ef09-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="2ef09-124">-Tag</span></span>
<span data-ttu-id="2ef09-125">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="2ef09-125">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ef09-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ef09-126">-Confirm</span></span>
<span data-ttu-id="2ef09-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ef09-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ef09-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ef09-128">-WhatIf</span></span>
<span data-ttu-id="2ef09-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ef09-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ef09-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ef09-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ef09-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ef09-131">CommonParameters</span></span>
<span data-ttu-id="2ef09-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ef09-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ef09-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ef09-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ef09-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="2ef09-134">INPUTS</span></span>

### <span data-ttu-id="2ef09-135">System.String</span><span class="sxs-lookup"><span data-stu-id="2ef09-135">System.String</span></span>

### <span data-ttu-id="2ef09-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="2ef09-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="2ef09-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ef09-137">OUTPUTS</span></span>

### <span data-ttu-id="2ef09-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="2ef09-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="2ef09-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="2ef09-139">NOTES</span></span>

## <span data-ttu-id="2ef09-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ef09-140">RELATED LINKS</span></span>
