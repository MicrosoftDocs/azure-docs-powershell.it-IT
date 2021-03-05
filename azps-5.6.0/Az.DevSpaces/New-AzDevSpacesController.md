---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/powershell/module/az.devspaces/new-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
ms.openlocfilehash: 097248e06acd081582ecc34a863658b2b073ef60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004206"
---
# <span data-ttu-id="2b966-101">New-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="2b966-101">New-AzDevSpacesController</span></span>

## <span data-ttu-id="2b966-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b966-102">SYNOPSIS</span></span>
<span data-ttu-id="2b966-103">Crea un nuovo controller Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="2b966-103">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="2b966-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b966-104">SYNTAX</span></span>

```
New-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-TargetResourceGroupName] <String>
 [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b966-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2b966-105">DESCRIPTION</span></span>
<span data-ttu-id="2b966-106">Crea un nuovo controller Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="2b966-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="2b966-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b966-107">EXAMPLES</span></span>

### <span data-ttu-id="2b966-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2b966-108">Example 1</span></span>
```powershell
PS C:\> New-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="2b966-109">Creare un controller DevSpaces nel gruppo di risorse devSpaceResourceGroup con il nome devSpaceName.</span><span class="sxs-lookup"><span data-stu-id="2b966-109">Create a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="2b966-110">Usare clusterName cluster come destinazione per questo controller.</span><span class="sxs-lookup"><span data-stu-id="2b966-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="2b966-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b966-111">PARAMETERS</span></span>

### <span data-ttu-id="2b966-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b966-112">-AsJob</span></span>
<span data-ttu-id="2b966-113">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="2b966-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b966-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b966-114">-DefaultProfile</span></span>
<span data-ttu-id="2b966-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2b966-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b966-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2b966-116">-Name</span></span>
<span data-ttu-id="2b966-117">Nome controller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="2b966-117">DevSpaces Controller Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b966-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b966-118">-ResourceGroupName</span></span>
<span data-ttu-id="2b966-119">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2b966-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b966-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="2b966-120">-Tag</span></span>
<span data-ttu-id="2b966-121">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="2b966-121">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="2b966-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="2b966-122">-TargetClusterName</span></span>
<span data-ttu-id="2b966-123">Nome cluster di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2b966-123">Target Cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b966-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b966-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="2b966-125">Nome gruppo di risorse di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2b966-125">Target Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b966-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b966-126">-Confirm</span></span>
<span data-ttu-id="2b966-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b966-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b966-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b966-128">-WhatIf</span></span>
<span data-ttu-id="2b966-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b966-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b966-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b966-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b966-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b966-131">CommonParameters</span></span>
<span data-ttu-id="2b966-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b966-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b966-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b966-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b966-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="2b966-134">INPUTS</span></span>

### <span data-ttu-id="2b966-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2b966-135">None</span></span>

## <span data-ttu-id="2b966-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b966-136">OUTPUTS</span></span>

### <span data-ttu-id="2b966-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="2b966-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="2b966-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="2b966-138">NOTES</span></span>

## <span data-ttu-id="2b966-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b966-139">RELATED LINKS</span></span>
