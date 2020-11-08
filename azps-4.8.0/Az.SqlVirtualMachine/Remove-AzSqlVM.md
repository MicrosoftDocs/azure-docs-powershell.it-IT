---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzSqlVM.md
ms.openlocfilehash: 4478ec96cd7354a404a736ddd0f305cba5675b26
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188758"
---
# <span data-ttu-id="d3815-101">Remove-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="d3815-101">Remove-AzSqlVM</span></span>

## <span data-ttu-id="d3815-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3815-102">SYNOPSIS</span></span>
<span data-ttu-id="d3815-103">Elimina una macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="d3815-103">Deletes a sql virtual machine.</span></span>

## <span data-ttu-id="d3815-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3815-104">SYNTAX</span></span>

### <span data-ttu-id="d3815-105">Nome (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d3815-105">Name (Default)</span></span>
```
Remove-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3815-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d3815-106">InputObject</span></span>
```
Remove-AzSqlVM [-InputObject] <AzureSqlVMModel> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3815-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3815-107">ResourceId</span></span>
```
Remove-AzSqlVM [-ResourceId] <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3815-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3815-108">DESCRIPTION</span></span>
<span data-ttu-id="d3815-109">Il cmdlet Remove-AzSqlVM Elimina una macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="d3815-109">The Remove-AzSqlVM cmdlet deletes a sql virtual machine.</span></span>

## <span data-ttu-id="d3815-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3815-110">EXAMPLES</span></span>

### <span data-ttu-id="d3815-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d3815-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
```

<span data-ttu-id="d3815-112">Elimina la macchina virtuale di Azure SQL "VM" nel gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="d3815-112">Deletes the Azure SQL virtual machine "vm" in the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="d3815-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3815-113">PARAMETERS</span></span>

### <span data-ttu-id="d3815-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3815-114">-AsJob</span></span>
<span data-ttu-id="d3815-115">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="d3815-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="d3815-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3815-116">-DefaultProfile</span></span>
<span data-ttu-id="d3815-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3815-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3815-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3815-118">-InputObject</span></span>
<span data-ttu-id="d3815-119">Oggetto macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="d3815-119">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="d3815-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3815-120">-Name</span></span>
<span data-ttu-id="d3815-121">Nome macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="d3815-121">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="d3815-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3815-122">-PassThru</span></span>
<span data-ttu-id="d3815-123">Specifica se restituire la risorsa eliminata alla fine dell'esecuzione del cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3815-123">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="d3815-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3815-124">-ResourceGroupName</span></span>
<span data-ttu-id="d3815-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d3815-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="d3815-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3815-126">-ResourceId</span></span>
<span data-ttu-id="d3815-127">ID risorsa macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="d3815-127">SQL virtual machine resource id.</span></span>

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

### <span data-ttu-id="d3815-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d3815-128">-Confirm</span></span>
<span data-ttu-id="d3815-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3815-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3815-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3815-130">-WhatIf</span></span>
<span data-ttu-id="d3815-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3815-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3815-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3815-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3815-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3815-133">CommonParameters</span></span>
<span data-ttu-id="d3815-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3815-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3815-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3815-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3815-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3815-136">INPUTS</span></span>

### <span data-ttu-id="d3815-137">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="d3815-137">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="d3815-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3815-138">OUTPUTS</span></span>

### <span data-ttu-id="d3815-139">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="d3815-139">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="d3815-140">Note</span><span class="sxs-lookup"><span data-stu-id="d3815-140">NOTES</span></span>

## <span data-ttu-id="d3815-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3815-141">RELATED LINKS</span></span>
