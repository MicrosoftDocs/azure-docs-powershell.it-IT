---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
ms.openlocfilehash: f05855c7fa677c384e9d8d0c5385d6014d80d312
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983309"
---
# <span data-ttu-id="35f45-101">Remove-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="35f45-101">Remove-AzHostGroup</span></span>

## <span data-ttu-id="35f45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35f45-102">SYNOPSIS</span></span>
<span data-ttu-id="35f45-103">Rimuove un gruppo host.</span><span class="sxs-lookup"><span data-stu-id="35f45-103">Removes a host group.</span></span>

## <span data-ttu-id="35f45-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35f45-104">SYNTAX</span></span>

### <span data-ttu-id="35f45-105">DefaultParameter (Default)</span><span class="sxs-lookup"><span data-stu-id="35f45-105">DefaultParameter (Default)</span></span>
```
Remove-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35f45-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="35f45-106">ResourceIdParameter</span></span>
```
Remove-AzHostGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35f45-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="35f45-107">ObjectParameter</span></span>
```
Remove-AzHostGroup [-InputObject] <PSHostGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35f45-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="35f45-108">DESCRIPTION</span></span>
<span data-ttu-id="35f45-109">Questo cmdlet eliminerà un gruppo host</span><span class="sxs-lookup"><span data-stu-id="35f45-109">This cmdlet will delete a Host group</span></span>

## <span data-ttu-id="35f45-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35f45-110">EXAMPLES</span></span>

### <span data-ttu-id="35f45-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="35f45-111">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName | Remove-AzHostGroup
```

<span data-ttu-id="35f45-112">Questo comando recupera e rimuove il gruppo host specificato.</span><span class="sxs-lookup"><span data-stu-id="35f45-112">This command gets and removes the given host group.</span></span>

### <span data-ttu-id="35f45-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="35f45-113">Example 2</span></span>
```
PS C:\> Remove-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName
```

<span data-ttu-id="35f45-114">Questo comando rimuove il gruppo host specificato.</span><span class="sxs-lookup"><span data-stu-id="35f45-114">This command removes the given host group.</span></span>

## <span data-ttu-id="35f45-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35f45-115">PARAMETERS</span></span>

### <span data-ttu-id="35f45-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35f45-116">-AsJob</span></span>
<span data-ttu-id="35f45-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="35f45-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35f45-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35f45-118">-DefaultProfile</span></span>
<span data-ttu-id="35f45-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35f45-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35f45-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35f45-120">-InputObject</span></span>
<span data-ttu-id="35f45-121">Oggetto locale del gruppo host.</span><span class="sxs-lookup"><span data-stu-id="35f45-121">The local object of the host group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup
Parameter Sets: ObjectParameter
Aliases: HostGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35f45-122">-Name</span><span class="sxs-lookup"><span data-stu-id="35f45-122">-Name</span></span>
<span data-ttu-id="35f45-123">Nome del gruppo host.</span><span class="sxs-lookup"><span data-stu-id="35f45-123">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35f45-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35f45-124">-ResourceGroupName</span></span>
<span data-ttu-id="35f45-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="35f45-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="35f45-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35f45-126">-ResourceId</span></span>
<span data-ttu-id="35f45-127">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="35f45-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="35f45-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35f45-128">-Confirm</span></span>
<span data-ttu-id="35f45-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35f45-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35f45-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35f45-130">-WhatIf</span></span>
<span data-ttu-id="35f45-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35f45-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35f45-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35f45-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35f45-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35f45-133">CommonParameters</span></span>
<span data-ttu-id="35f45-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35f45-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35f45-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="35f45-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35f45-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="35f45-136">INPUTS</span></span>

### <span data-ttu-id="35f45-137">System.String</span><span class="sxs-lookup"><span data-stu-id="35f45-137">System.String</span></span>

### <span data-ttu-id="35f45-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="35f45-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="35f45-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35f45-139">OUTPUTS</span></span>

### <span data-ttu-id="35f45-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="35f45-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="35f45-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="35f45-141">NOTES</span></span>

## <span data-ttu-id="35f45-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35f45-142">RELATED LINKS</span></span>
