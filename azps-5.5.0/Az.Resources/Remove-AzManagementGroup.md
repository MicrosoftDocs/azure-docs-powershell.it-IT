---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: ce2ccd21d7adecdf9602d29837295ad2ca65c952
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201871"
---
# <span data-ttu-id="9e333-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9e333-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="9e333-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e333-102">SYNOPSIS</span></span>
<span data-ttu-id="9e333-103">Rimuove un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="9e333-103">Removes a Management Group</span></span>

## <span data-ttu-id="9e333-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e333-104">SYNTAX</span></span>

### <span data-ttu-id="9e333-105">GroupOperations (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9e333-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e333-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="9e333-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e333-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9e333-107">DESCRIPTION</span></span>
<span data-ttu-id="9e333-108">Il cmdlet **Remove-AzManagementGroup** elimina un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="9e333-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="9e333-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e333-109">EXAMPLES</span></span>

### <span data-ttu-id="9e333-110">Esempio 1: Rimuovere un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="9e333-110">Example 1: Remove a Management Group</span></span>
```powershell
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="9e333-111">Esempio 2: Rimuovere un gruppo di gestione con l'oggetto PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9e333-111">Example 2: Remove a Management Group by piping PSManagementGroup Object</span></span>
```powershell
PS C:\> Get-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="9e333-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e333-112">PARAMETERS</span></span>

### <span data-ttu-id="9e333-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e333-113">-DefaultProfile</span></span>
<span data-ttu-id="9e333-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e333-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e333-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="9e333-115">-GroupName</span></span>
<span data-ttu-id="9e333-116">ID gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="9e333-116">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e333-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e333-117">-InputObject</span></span>
<span data-ttu-id="9e333-118">Oggetto di input dalla chiamata Get</span><span class="sxs-lookup"><span data-stu-id="9e333-118">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e333-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e333-119">-PassThru</span></span>
<span data-ttu-id="9e333-120">Ritorno `true` sull'esecuzione completata</span><span class="sxs-lookup"><span data-stu-id="9e333-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="9e333-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e333-121">-Confirm</span></span>
<span data-ttu-id="9e333-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e333-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e333-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e333-123">-WhatIf</span></span>
<span data-ttu-id="9e333-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e333-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e333-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e333-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e333-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e333-126">CommonParameters</span></span>
<span data-ttu-id="9e333-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e333-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e333-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9e333-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e333-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="9e333-129">INPUTS</span></span>

### <span data-ttu-id="9e333-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9e333-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="9e333-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e333-131">OUTPUTS</span></span>

### <span data-ttu-id="9e333-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9e333-132">System.Boolean</span></span>

## <span data-ttu-id="9e333-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="9e333-133">NOTES</span></span>

## <span data-ttu-id="9e333-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e333-134">RELATED LINKS</span></span>
