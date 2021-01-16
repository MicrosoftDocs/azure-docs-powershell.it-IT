---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/new-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
ms.openlocfilehash: a99a26060492efbe40bc4a16633ca6a207e093b4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475342"
---
# <span data-ttu-id="6aac7-101">New-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="6aac7-101">New-AzDevSpacesController</span></span>

## <span data-ttu-id="6aac7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6aac7-102">SYNOPSIS</span></span>
<span data-ttu-id="6aac7-103">Creare un nuovo controller di Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="6aac7-103">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="6aac7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6aac7-104">SYNTAX</span></span>

```
New-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-TargetResourceGroupName] <String>
 [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6aac7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6aac7-105">DESCRIPTION</span></span>
<span data-ttu-id="6aac7-106">Creare un nuovo controller di Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="6aac7-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="6aac7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6aac7-107">EXAMPLES</span></span>

### <span data-ttu-id="6aac7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6aac7-108">Example 1</span></span>
```powershell
PS C:\> New-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="6aac7-109">Creare un controller DevSpaces in ResourceGroup devSpaceResourceGroup con un nome devSpaceName.</span><span class="sxs-lookup"><span data-stu-id="6aac7-109">Create a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="6aac7-110">USA clustername cluster come destinazione per questo controller.</span><span class="sxs-lookup"><span data-stu-id="6aac7-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="6aac7-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6aac7-111">PARAMETERS</span></span>

### <span data-ttu-id="6aac7-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6aac7-112">-AsJob</span></span>
<span data-ttu-id="6aac7-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6aac7-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6aac7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aac7-114">-DefaultProfile</span></span>
<span data-ttu-id="6aac7-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6aac7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6aac7-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="6aac7-116">-Name</span></span>
<span data-ttu-id="6aac7-117">Nome del controller DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="6aac7-117">DevSpaces Controller Name.</span></span>

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

### <span data-ttu-id="6aac7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aac7-118">-ResourceGroupName</span></span>
<span data-ttu-id="6aac7-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6aac7-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="6aac7-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="6aac7-120">-Tag</span></span>
<span data-ttu-id="6aac7-121">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="6aac7-121">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="6aac7-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="6aac7-122">-TargetClusterName</span></span>
<span data-ttu-id="6aac7-123">Nome del cluster di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6aac7-123">Target Cluster Name.</span></span>

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

### <span data-ttu-id="6aac7-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aac7-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="6aac7-125">Nome del gruppo di risorse di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6aac7-125">Target Resource Group Name.</span></span>

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

### <span data-ttu-id="6aac7-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6aac7-126">-Confirm</span></span>
<span data-ttu-id="6aac7-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6aac7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6aac7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6aac7-128">-WhatIf</span></span>
<span data-ttu-id="6aac7-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6aac7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6aac7-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6aac7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6aac7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aac7-131">CommonParameters</span></span>
<span data-ttu-id="6aac7-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aac7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aac7-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aac7-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aac7-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6aac7-134">INPUTS</span></span>

### <span data-ttu-id="6aac7-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6aac7-135">None</span></span>

## <span data-ttu-id="6aac7-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6aac7-136">OUTPUTS</span></span>

### <span data-ttu-id="6aac7-137">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="6aac7-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="6aac7-138">Note</span><span class="sxs-lookup"><span data-stu-id="6aac7-138">NOTES</span></span>

## <span data-ttu-id="6aac7-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6aac7-139">RELATED LINKS</span></span>
