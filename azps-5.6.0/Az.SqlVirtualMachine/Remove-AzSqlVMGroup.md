---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/remove-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
ms.openlocfilehash: d9d5ee7159f5a7f237bd9194051c99801481f1d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977997"
---
# <span data-ttu-id="dd7da-101">Remove-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="dd7da-101">Remove-AzSqlVMGroup</span></span>

## <span data-ttu-id="dd7da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd7da-102">SYNOPSIS</span></span>
<span data-ttu-id="dd7da-103">Elimina un gruppo di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="dd7da-103">Deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="dd7da-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd7da-104">SYNTAX</span></span>

### <span data-ttu-id="dd7da-105">ParamaterList (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dd7da-105">ParamaterList (Default)</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd7da-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="dd7da-106">InputObject</span></span>
```
Remove-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd7da-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd7da-107">ResourceId</span></span>
```
Remove-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd7da-108">Nome</span><span class="sxs-lookup"><span data-stu-id="dd7da-108">Name</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd7da-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dd7da-109">DESCRIPTION</span></span>
<span data-ttu-id="dd7da-110">Il Remove-AzSqlVMGroup cmdlet elimina un gruppo di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="dd7da-110">The Remove-AzSqlVMGroup cmdlet deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="dd7da-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd7da-111">EXAMPLES</span></span>

### <span data-ttu-id="dd7da-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dd7da-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
```

<span data-ttu-id="dd7da-113">Elimina il gruppo SQL di macchine virtuali Azure "test-group" nel gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="dd7da-113">Deletes the Azure SQL virtual machine group "test-group" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="dd7da-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd7da-114">PARAMETERS</span></span>

### <span data-ttu-id="dd7da-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd7da-115">-AsJob</span></span>
<span data-ttu-id="dd7da-116">Eseguire il cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="dd7da-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="dd7da-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd7da-117">-DefaultProfile</span></span>
<span data-ttu-id="dd7da-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd7da-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd7da-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd7da-119">-InputObject</span></span>
<span data-ttu-id="dd7da-120">SQL dell'oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd7da-120">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: InputObject
Aliases: SqlVMGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd7da-121">-Name</span><span class="sxs-lookup"><span data-stu-id="dd7da-121">-Name</span></span>
<span data-ttu-id="dd7da-122">SQL del gruppo di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="dd7da-122">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7da-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd7da-123">-PassThru</span></span>
<span data-ttu-id="dd7da-124">Specifica se l'output della risorsa eliminata deve essere restituito al termine dell'esecuzione del cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd7da-124">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="dd7da-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd7da-125">-ResourceGroupName</span></span>
<span data-ttu-id="dd7da-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dd7da-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7da-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd7da-127">-ResourceId</span></span>
<span data-ttu-id="dd7da-128">SQL ID risorsa gruppo di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="dd7da-128">SQL virtual machine group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd7da-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd7da-129">-Confirm</span></span>
<span data-ttu-id="dd7da-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd7da-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd7da-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd7da-131">-WhatIf</span></span>
<span data-ttu-id="dd7da-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd7da-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd7da-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd7da-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd7da-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd7da-134">CommonParameters</span></span>
<span data-ttu-id="dd7da-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd7da-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd7da-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dd7da-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd7da-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="dd7da-137">INPUTS</span></span>

### <span data-ttu-id="dd7da-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="dd7da-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="dd7da-139">System.String</span><span class="sxs-lookup"><span data-stu-id="dd7da-139">System.String</span></span>

## <span data-ttu-id="dd7da-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd7da-140">OUTPUTS</span></span>

### <span data-ttu-id="dd7da-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="dd7da-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="dd7da-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="dd7da-142">NOTES</span></span>

## <span data-ttu-id="dd7da-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd7da-143">RELATED LINKS</span></span>
