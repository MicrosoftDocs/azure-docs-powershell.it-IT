---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/new-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
ms.openlocfilehash: a99a26060492efbe40bc4a16633ca6a207e093b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209698"
---
# <span data-ttu-id="eeaf4-101">New-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="eeaf4-101">New-AzDevSpacesController</span></span>

## <span data-ttu-id="eeaf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eeaf4-102">SYNOPSIS</span></span>
<span data-ttu-id="eeaf4-103">Crea un nuovo controller Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="eeaf4-103">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="eeaf4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eeaf4-104">SYNTAX</span></span>

```
New-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-TargetResourceGroupName] <String>
 [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eeaf4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="eeaf4-105">DESCRIPTION</span></span>
<span data-ttu-id="eeaf4-106">Crea un nuovo controller Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="eeaf4-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="eeaf4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eeaf4-107">EXAMPLES</span></span>

### <span data-ttu-id="eeaf4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="eeaf4-108">Example 1</span></span>
```powershell
PS C:\> New-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="eeaf4-109">Creare un controller DevSpaces nel gruppo di risorse devSpaceResourceGroup con il nome devSpaceName.</span><span class="sxs-lookup"><span data-stu-id="eeaf4-109">Create a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="eeaf4-110">Usare clusterName cluster come destinazione per questo controller.</span><span class="sxs-lookup"><span data-stu-id="eeaf4-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="eeaf4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eeaf4-111">PARAMETERS</span></span>

### <span data-ttu-id="eeaf4-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eeaf4-112">-AsJob</span></span>
<span data-ttu-id="eeaf4-113">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="eeaf4-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eeaf4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeaf4-114">-DefaultProfile</span></span>
<span data-ttu-id="eeaf4-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eeaf4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eeaf4-116">-Name</span><span class="sxs-lookup"><span data-stu-id="eeaf4-116">-Name</span></span>
<span data-ttu-id="eeaf4-117">Nome controller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="eeaf4-117">DevSpaces Controller Name.</span></span>

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

### <span data-ttu-id="eeaf4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeaf4-118">-ResourceGroupName</span></span>
<span data-ttu-id="eeaf4-119">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="eeaf4-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="eeaf4-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="eeaf4-120">-Tag</span></span>
<span data-ttu-id="eeaf4-121">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="eeaf4-121">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="eeaf4-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="eeaf4-122">-TargetClusterName</span></span>
<span data-ttu-id="eeaf4-123">Nome cluster di destinazione.</span><span class="sxs-lookup"><span data-stu-id="eeaf4-123">Target Cluster Name.</span></span>

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

### <span data-ttu-id="eeaf4-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeaf4-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="eeaf4-125">Nome gruppo di risorse di destinazione.</span><span class="sxs-lookup"><span data-stu-id="eeaf4-125">Target Resource Group Name.</span></span>

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

### <span data-ttu-id="eeaf4-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eeaf4-126">-Confirm</span></span>
<span data-ttu-id="eeaf4-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeaf4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeaf4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeaf4-128">-WhatIf</span></span>
<span data-ttu-id="eeaf4-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eeaf4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eeaf4-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eeaf4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeaf4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeaf4-131">CommonParameters</span></span>
<span data-ttu-id="eeaf4-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeaf4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeaf4-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeaf4-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeaf4-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="eeaf4-134">INPUTS</span></span>

### <span data-ttu-id="eeaf4-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="eeaf4-135">None</span></span>

## <span data-ttu-id="eeaf4-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eeaf4-136">OUTPUTS</span></span>

### <span data-ttu-id="eeaf4-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="eeaf4-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="eeaf4-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="eeaf4-138">NOTES</span></span>

## <span data-ttu-id="eeaf4-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eeaf4-139">RELATED LINKS</span></span>
