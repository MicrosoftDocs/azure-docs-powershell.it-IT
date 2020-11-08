---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVM.md
ms.openlocfilehash: 764312c64ae9887a6ef4243cc20b04535afcf81f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189243"
---
# <span data-ttu-id="f9809-101">New-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="f9809-101">New-AzSqlVM</span></span>

## <span data-ttu-id="f9809-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f9809-102">SYNOPSIS</span></span>
<span data-ttu-id="f9809-103">Crea una nuova macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="f9809-103">Creates a new sql virtual machine.</span></span>

## <span data-ttu-id="f9809-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9809-104">SYNTAX</span></span>

### <span data-ttu-id="f9809-105">NameParamaterList (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f9809-105">NameParamaterList (Default)</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType] <String> -Location <String> [-AsJob]
 [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9809-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="f9809-106">NameInputObject</span></span>
```
New-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-SqlVM] <AzureSqlVMModel> -Location <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9809-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9809-107">DESCRIPTION</span></span>
<span data-ttu-id="f9809-108">Il cmdlet New-AzSqlVM crea una macchina virtuale di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f9809-108">The New-AzSqlVM cmdlet creates an Azure SQL virtual machine.</span></span>

## <span data-ttu-id="f9809-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9809-109">EXAMPLES</span></span>

### <span data-ttu-id="f9809-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f9809-110">Example 1</span></span>
```powershell
PS C:\> New-AzSqlVM  New-AzSqlVM -ResourceGroupName ResourceGroup01 -Name vm -LicenseType 'PAYG' -Sku Developer
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="f9809-111">Crea una nuova macchina virtuale di Azure SQL con il nome VM nel gruppo di risorse ResourceGroup01</span><span class="sxs-lookup"><span data-stu-id="f9809-111">Creates a new Azure SQL virtual machine with name vm in the resource group ResourceGroup01</span></span> 

## <span data-ttu-id="f9809-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f9809-112">PARAMETERS</span></span>

### <span data-ttu-id="f9809-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9809-113">-AsJob</span></span>
<span data-ttu-id="f9809-114">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="f9809-114">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="f9809-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9809-115">-DefaultProfile</span></span>
<span data-ttu-id="f9809-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f9809-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9809-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f9809-117">-LicenseType</span></span>
<span data-ttu-id="f9809-118">Tipo di licenza per la macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="f9809-118">SQL virtual machine license type.</span></span>

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

### <span data-ttu-id="f9809-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f9809-119">-Location</span></span>
<span data-ttu-id="f9809-120">Posizione della macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="f9809-120">SQL virtual machine location.</span></span>

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

### <span data-ttu-id="f9809-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9809-121">-Name</span></span>
<span data-ttu-id="f9809-122">Nome macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="f9809-122">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="f9809-123">-Offerta</span><span class="sxs-lookup"><span data-stu-id="f9809-123">-Offer</span></span>
<span data-ttu-id="f9809-124">Offerta macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="f9809-124">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="f9809-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9809-125">-ResourceGroupName</span></span>
<span data-ttu-id="f9809-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f9809-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="f9809-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="f9809-127">-Sku</span></span>
<span data-ttu-id="f9809-128">Tipo SQL Virtual Machine Edition.</span><span class="sxs-lookup"><span data-stu-id="f9809-128">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="f9809-129">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="f9809-129">-SqlManagementType</span></span>
<span data-ttu-id="f9809-130">Tipo di gestione della macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="f9809-130">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="f9809-131">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="f9809-131">-SqlVM</span></span>
<span data-ttu-id="f9809-132">Oggetto macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="f9809-132">SQL virtual machine object.</span></span>

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

### <span data-ttu-id="f9809-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="f9809-133">-Tag</span></span>
<span data-ttu-id="f9809-134">Tag da associare alla macchina virtuale SQL</span><span class="sxs-lookup"><span data-stu-id="f9809-134">The tags to associate with the SQL virtual machine</span></span>

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

### <span data-ttu-id="f9809-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f9809-135">-Confirm</span></span>
<span data-ttu-id="f9809-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9809-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9809-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9809-137">-WhatIf</span></span>
<span data-ttu-id="f9809-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9809-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9809-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9809-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9809-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9809-140">CommonParameters</span></span>
<span data-ttu-id="f9809-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9809-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9809-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9809-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9809-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f9809-143">INPUTS</span></span>

### <span data-ttu-id="f9809-144">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="f9809-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="f9809-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9809-145">OUTPUTS</span></span>

### <span data-ttu-id="f9809-146">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="f9809-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="f9809-147">Note</span><span class="sxs-lookup"><span data-stu-id="f9809-147">NOTES</span></span>

## <span data-ttu-id="f9809-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9809-148">RELATED LINKS</span></span>