---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/remove-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
ms.openlocfilehash: 741db1ddd4d2cce236d5a1d6787ea25179aa373f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977998"
---
# <span data-ttu-id="77df1-101">Remove-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="77df1-101">Remove-AzSqlVM</span></span>

## <span data-ttu-id="77df1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77df1-102">SYNOPSIS</span></span>
<span data-ttu-id="77df1-103">Elimina una macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="77df1-103">Deletes a sql virtual machine.</span></span>

## <span data-ttu-id="77df1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77df1-104">SYNTAX</span></span>

### <span data-ttu-id="77df1-105">Nome (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="77df1-105">Name (Default)</span></span>
```
Remove-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77df1-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="77df1-106">InputObject</span></span>
```
Remove-AzSqlVM [-InputObject] <AzureSqlVMModel> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77df1-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="77df1-107">ResourceId</span></span>
```
Remove-AzSqlVM [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77df1-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="77df1-108">DESCRIPTION</span></span>
<span data-ttu-id="77df1-109">Il Remove-AzSqlVM cmdlet elimina una macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="77df1-109">The Remove-AzSqlVM cmdlet deletes a sql virtual machine.</span></span>

## <span data-ttu-id="77df1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77df1-110">EXAMPLES</span></span>

### <span data-ttu-id="77df1-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="77df1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
```

<span data-ttu-id="77df1-112">Elimina la "macchina SQL" della macchina virtuale Azure nel gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="77df1-112">Deletes the Azure SQL virtual machine "vm" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="77df1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77df1-113">PARAMETERS</span></span>

### <span data-ttu-id="77df1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77df1-114">-AsJob</span></span>
<span data-ttu-id="77df1-115">Eseguire il cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="77df1-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="77df1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77df1-116">-DefaultProfile</span></span>
<span data-ttu-id="77df1-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="77df1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77df1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77df1-118">-InputObject</span></span>
<span data-ttu-id="77df1-119">SQL dell'oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="77df1-119">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: InputObject
Aliases: SqlVM

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77df1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="77df1-120">-Name</span></span>
<span data-ttu-id="77df1-121">SQL nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="77df1-121">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77df1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77df1-122">-PassThru</span></span>
<span data-ttu-id="77df1-123">Specifica se l'output della risorsa eliminata deve essere restituito al termine dell'esecuzione del cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77df1-123">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="77df1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77df1-124">-ResourceGroupName</span></span>
<span data-ttu-id="77df1-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="77df1-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="77df1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77df1-126">-ResourceId</span></span>
<span data-ttu-id="77df1-127">SQL ID risorsa della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="77df1-127">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77df1-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77df1-128">-Confirm</span></span>
<span data-ttu-id="77df1-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77df1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77df1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77df1-130">-WhatIf</span></span>
<span data-ttu-id="77df1-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77df1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77df1-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77df1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77df1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77df1-133">CommonParameters</span></span>
<span data-ttu-id="77df1-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77df1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77df1-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="77df1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77df1-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="77df1-136">INPUTS</span></span>

### <span data-ttu-id="77df1-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="77df1-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="77df1-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77df1-138">OUTPUTS</span></span>

### <span data-ttu-id="77df1-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="77df1-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="77df1-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="77df1-140">NOTES</span></span>

## <span data-ttu-id="77df1-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77df1-141">RELATED LINKS</span></span>
