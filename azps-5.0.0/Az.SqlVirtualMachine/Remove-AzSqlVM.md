---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
ms.openlocfilehash: 4478ec96cd7354a404a736ddd0f305cba5675b26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193601"
---
# <span data-ttu-id="30f0f-101">Remove-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="30f0f-101">Remove-AzSqlVM</span></span>

## <span data-ttu-id="30f0f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30f0f-102">SYNOPSIS</span></span>
<span data-ttu-id="30f0f-103">Elimina una macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="30f0f-103">Deletes a sql virtual machine.</span></span>

## <span data-ttu-id="30f0f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30f0f-104">SYNTAX</span></span>

### <span data-ttu-id="30f0f-105">Nome (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="30f0f-105">Name (Default)</span></span>
```
Remove-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30f0f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="30f0f-106">InputObject</span></span>
```
Remove-AzSqlVM [-InputObject] <AzureSqlVMModel> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30f0f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="30f0f-107">ResourceId</span></span>
```
Remove-AzSqlVM [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30f0f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30f0f-108">DESCRIPTION</span></span>
<span data-ttu-id="30f0f-109">Il cmdlet Remove-AzSqlVM Elimina una macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="30f0f-109">The Remove-AzSqlVM cmdlet deletes a sql virtual machine.</span></span>

## <span data-ttu-id="30f0f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30f0f-110">EXAMPLES</span></span>

### <span data-ttu-id="30f0f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="30f0f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
```

<span data-ttu-id="30f0f-112">Elimina la macchina virtuale di Azure SQL "VM" nel gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="30f0f-112">Deletes the Azure SQL virtual machine "vm" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="30f0f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30f0f-113">PARAMETERS</span></span>

### <span data-ttu-id="30f0f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30f0f-114">-AsJob</span></span>
<span data-ttu-id="30f0f-115">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="30f0f-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="30f0f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30f0f-116">-DefaultProfile</span></span>
<span data-ttu-id="30f0f-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="30f0f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30f0f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30f0f-118">-InputObject</span></span>
<span data-ttu-id="30f0f-119">Oggetto macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="30f0f-119">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="30f0f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="30f0f-120">-Name</span></span>
<span data-ttu-id="30f0f-121">Nome macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="30f0f-121">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="30f0f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30f0f-122">-PassThru</span></span>
<span data-ttu-id="30f0f-123">Specifica se restituire la risorsa eliminata alla fine dell'esecuzione del cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30f0f-123">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="30f0f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30f0f-124">-ResourceGroupName</span></span>
<span data-ttu-id="30f0f-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="30f0f-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="30f0f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30f0f-126">-ResourceId</span></span>
<span data-ttu-id="30f0f-127">ID risorsa macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="30f0f-127">SQL virtual machine resource id.</span></span>

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

### <span data-ttu-id="30f0f-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="30f0f-128">-Confirm</span></span>
<span data-ttu-id="30f0f-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30f0f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30f0f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30f0f-130">-WhatIf</span></span>
<span data-ttu-id="30f0f-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30f0f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30f0f-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30f0f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30f0f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30f0f-133">CommonParameters</span></span>
<span data-ttu-id="30f0f-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30f0f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30f0f-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30f0f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30f0f-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30f0f-136">INPUTS</span></span>

### <span data-ttu-id="30f0f-137">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="30f0f-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="30f0f-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30f0f-138">OUTPUTS</span></span>

### <span data-ttu-id="30f0f-139">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="30f0f-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="30f0f-140">Note</span><span class="sxs-lookup"><span data-stu-id="30f0f-140">NOTES</span></span>

## <span data-ttu-id="30f0f-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30f0f-141">RELATED LINKS</span></span>
