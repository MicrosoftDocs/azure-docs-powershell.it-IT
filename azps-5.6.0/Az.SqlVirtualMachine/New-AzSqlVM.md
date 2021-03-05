---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/new-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
ms.openlocfilehash: f7afae369258a30a156ff0439407fb4e4e4ef732
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008317"
---
# <span data-ttu-id="7e248-101">New-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="7e248-101">New-AzSqlVM</span></span>

## <span data-ttu-id="7e248-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e248-102">SYNOPSIS</span></span>
<span data-ttu-id="7e248-103">Crea una nuova macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="7e248-103">Creates a new sql virtual machine.</span></span>

## <span data-ttu-id="7e248-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e248-104">SYNTAX</span></span>

### <span data-ttu-id="7e248-105">NameParamaterList (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7e248-105">NameParamaterList (Default)</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType] <String> -Location <String> [-AsJob]
 [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e248-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="7e248-106">NameInputObject</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-SqlVM] <AzureSqlVMModel> -Location <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e248-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7e248-107">DESCRIPTION</span></span>
<span data-ttu-id="7e248-108">Il cmdlet New-AzSqlVM crea una macchina virtuale SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="7e248-108">The New-AzSqlVM cmdlet creates an Azure SQL virtual machine.</span></span>

## <span data-ttu-id="7e248-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e248-109">EXAMPLES</span></span>

### <span data-ttu-id="7e248-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7e248-110">Example 1</span></span>
```powershell
PS C:\> New-AzSqlVM  New-AzSqlVM -ResourceGroupName ResourceGroup01 -Name vm -LicenseType 'PAYG' -Sku Developer
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="7e248-111">Crea una nuova macchina virtuale Azure SQL con nome vm nel gruppo di risorse ResourceGroup01</span><span class="sxs-lookup"><span data-stu-id="7e248-111">Creates a new Azure SQL virtual machine with name vm in the resource group ResourceGroup01</span></span> 

## <span data-ttu-id="7e248-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e248-112">PARAMETERS</span></span>

### <span data-ttu-id="7e248-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e248-113">-AsJob</span></span>
<span data-ttu-id="7e248-114">Eseguire il cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="7e248-114">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="7e248-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e248-115">-DefaultProfile</span></span>
<span data-ttu-id="7e248-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e248-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e248-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7e248-117">-LicenseType</span></span>
<span data-ttu-id="7e248-118">SQL di licenza della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e248-118">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e248-119">-Location</span><span class="sxs-lookup"><span data-stu-id="7e248-119">-Location</span></span>
<span data-ttu-id="7e248-120">SQL posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e248-120">SQL virtual machine location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e248-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7e248-121">-Name</span></span>
<span data-ttu-id="7e248-122">SQL nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e248-122">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e248-123">-Offerta</span><span class="sxs-lookup"><span data-stu-id="7e248-123">-Offer</span></span>
<span data-ttu-id="7e248-124">SQL di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="7e248-124">SQL virtual machine offer.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e248-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e248-125">-ResourceGroupName</span></span>
<span data-ttu-id="7e248-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7e248-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="7e248-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="7e248-127">-Sku</span></span>
<span data-ttu-id="7e248-128">SQL di edizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e248-128">SQL virtual machine edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e248-129">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="7e248-129">-SqlManagementType</span></span>
<span data-ttu-id="7e248-130">SQL di gestione delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="7e248-130">SQL virtual machine management type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e248-131">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="7e248-131">-SqlVM</span></span>
<span data-ttu-id="7e248-132">SQL dell'oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e248-132">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: NameInputObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e248-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="7e248-133">-Tag</span></span>
<span data-ttu-id="7e248-134">I tag da associare alla macchina SQL virtuale</span><span class="sxs-lookup"><span data-stu-id="7e248-134">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: NameParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e248-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e248-135">-Confirm</span></span>
<span data-ttu-id="7e248-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e248-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e248-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e248-137">-WhatIf</span></span>
<span data-ttu-id="7e248-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e248-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e248-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e248-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e248-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e248-140">CommonParameters</span></span>
<span data-ttu-id="7e248-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e248-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e248-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7e248-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e248-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="7e248-143">INPUTS</span></span>

### <span data-ttu-id="7e248-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="7e248-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="7e248-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e248-145">OUTPUTS</span></span>

### <span data-ttu-id="7e248-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="7e248-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="7e248-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="7e248-147">NOTES</span></span>

## <span data-ttu-id="7e248-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e248-148">RELATED LINKS</span></span>
