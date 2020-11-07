---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVMGroup.md
ms.openlocfilehash: fec35992f96940dc69cdb6d1777d43ca151688bc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864883"
---
# <span data-ttu-id="fe2b1-101">Remove-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="fe2b1-101">Remove-AzSqlVMGroup</span></span>

## <span data-ttu-id="fe2b1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fe2b1-102">SYNOPSIS</span></span>
<span data-ttu-id="fe2b1-103">Elimina un gruppo di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="fe2b1-103">Deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="fe2b1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe2b1-104">SYNTAX</span></span>

### <span data-ttu-id="fe2b1-105">Paramaterico (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fe2b1-105">ParamaterList (Default)</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe2b1-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fe2b1-106">InputObject</span></span>
```
Remove-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe2b1-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe2b1-107">ResourceId</span></span>
```
Remove-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe2b1-108">Nome</span><span class="sxs-lookup"><span data-stu-id="fe2b1-108">Name</span></span>
```
Remove-AzSqlVMGroup [-AsJob] [-PassThru] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe2b1-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe2b1-109">DESCRIPTION</span></span>
<span data-ttu-id="fe2b1-110">Il cmdlet Remove-AzSqlVMGroup Elimina un gruppo di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="fe2b1-110">The Remove-AzSqlVMGroup cmdlet deletes a sql virtual machine group.</span></span>

## <span data-ttu-id="fe2b1-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe2b1-111">EXAMPLES</span></span>

### <span data-ttu-id="fe2b1-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fe2b1-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
```

<span data-ttu-id="fe2b1-113">Elimina il gruppo "test-Group" di Azure SQL Virtual Machine nel gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="fe2b1-113">Deletes the Azure SQL virtual machine group "test-group" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="fe2b1-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fe2b1-114">PARAMETERS</span></span>

### <span data-ttu-id="fe2b1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe2b1-115">-AsJob</span></span>
<span data-ttu-id="fe2b1-116">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="fe2b1-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="fe2b1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe2b1-117">-DefaultProfile</span></span>
<span data-ttu-id="fe2b1-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fe2b1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe2b1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe2b1-119">-InputObject</span></span>
<span data-ttu-id="fe2b1-120">Oggetto macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="fe2b1-120">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="fe2b1-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe2b1-121">-Name</span></span>
<span data-ttu-id="fe2b1-122">Nome del gruppo di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="fe2b1-122">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="fe2b1-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe2b1-123">-PassThru</span></span>
<span data-ttu-id="fe2b1-124">Specifica se restituire la risorsa eliminata alla fine dell'esecuzione del cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe2b1-124">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="fe2b1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe2b1-125">-ResourceGroupName</span></span>
<span data-ttu-id="fe2b1-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fe2b1-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="fe2b1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe2b1-127">-ResourceId</span></span>
<span data-ttu-id="fe2b1-128">ID risorsa di gruppo della macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="fe2b1-128">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="fe2b1-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fe2b1-129">-Confirm</span></span>
<span data-ttu-id="fe2b1-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe2b1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe2b1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe2b1-131">-WhatIf</span></span>
<span data-ttu-id="fe2b1-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe2b1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe2b1-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe2b1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe2b1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe2b1-134">CommonParameters</span></span>
<span data-ttu-id="fe2b1-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe2b1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe2b1-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe2b1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe2b1-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fe2b1-137">INPUTS</span></span>

### <span data-ttu-id="fe2b1-138">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="fe2b1-138">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="fe2b1-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fe2b1-139">System.String</span></span>

## <span data-ttu-id="fe2b1-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe2b1-140">OUTPUTS</span></span>

### <span data-ttu-id="fe2b1-141">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="fe2b1-141">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="fe2b1-142">Note</span><span class="sxs-lookup"><span data-stu-id="fe2b1-142">NOTES</span></span>

## <span data-ttu-id="fe2b1-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe2b1-143">RELATED LINKS</span></span>
