---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVM.md
ms.openlocfilehash: bfc64aeb344e9913bf72ae7b51559bb613209994
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857626"
---
# <span data-ttu-id="5e41e-101">Update-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="5e41e-101">Update-AzSqlVM</span></span>

## <span data-ttu-id="5e41e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e41e-102">SYNOPSIS</span></span>
<span data-ttu-id="5e41e-103">Aggiorna una macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="5e41e-103">Updates a sql virtual machine.</span></span>

## <span data-ttu-id="5e41e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e41e-104">SYNTAX</span></span>

### <span data-ttu-id="5e41e-105">NameParamaterList (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5e41e-105">NameParamaterList (Default)</span></span>
```
Update-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Offer <String>]
 [-Sku <String>] [-SqlManagementType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e41e-106">NameInputObject</span><span class="sxs-lookup"><span data-stu-id="5e41e-106">NameInputObject</span></span>
```
Update-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <AzureSqlVMModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e41e-107">ResourceIdParamaterList</span><span class="sxs-lookup"><span data-stu-id="5e41e-107">ResourceIdParamaterList</span></span>
```
Update-AzSqlVM [-LicenseType <String>] [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e41e-108">ResourceIdInputObject</span><span class="sxs-lookup"><span data-stu-id="5e41e-108">ResourceIdInputObject</span></span>
```
Update-AzSqlVM [-InputObject] <AzureSqlVMModel> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e41e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e41e-109">DESCRIPTION</span></span>
<span data-ttu-id="5e41e-110">Il cmdlet Update-AzSqlVM aggiorna una macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="5e41e-110">The Update-AzSqlVM cmdlet updates a sql virtual machine.</span></span>

## <span data-ttu-id="5e41e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e41e-111">EXAMPLES</span></span>

### <span data-ttu-id="5e41e-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5e41e-112">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $vm = Update-AzSqlVM -InputObject $vm -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="5e41e-113">Aggiorna i tag di una macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="5e41e-113">Updates the tags of a sql virtual machine.</span></span>

## <span data-ttu-id="5e41e-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e41e-114">PARAMETERS</span></span>

### <span data-ttu-id="5e41e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e41e-115">-AsJob</span></span>
<span data-ttu-id="5e41e-116">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="5e41e-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="5e41e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e41e-117">-DefaultProfile</span></span>
<span data-ttu-id="5e41e-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5e41e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e41e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e41e-119">-InputObject</span></span>
<span data-ttu-id="5e41e-120">Oggetto macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="5e41e-120">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: NameInputObject, ResourceIdInputObject
Aliases: SqlVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e41e-121">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5e41e-121">-LicenseType</span></span>
<span data-ttu-id="5e41e-122">Tipo di licenza per la macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="5e41e-122">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e41e-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e41e-123">-Name</span></span>
<span data-ttu-id="5e41e-124">Nome macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="5e41e-124">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, NameInputObject
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e41e-125">-Offerta</span><span class="sxs-lookup"><span data-stu-id="5e41e-125">-Offer</span></span>
<span data-ttu-id="5e41e-126">Offerta macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="5e41e-126">SQL virtual machine offer.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e41e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e41e-127">-ResourceGroupName</span></span>
<span data-ttu-id="5e41e-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5e41e-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, NameInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e41e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e41e-129">-ResourceId</span></span>
<span data-ttu-id="5e41e-130">ID risorsa macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="5e41e-130">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParamaterList, ResourceIdInputObject
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e41e-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="5e41e-131">-Sku</span></span>
<span data-ttu-id="5e41e-132">Tipo SQL Virtual Machine Edition.</span><span class="sxs-lookup"><span data-stu-id="5e41e-132">SQL virtual machine edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e41e-133">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="5e41e-133">-SqlManagementType</span></span>
<span data-ttu-id="5e41e-134">Tipo di gestione della macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="5e41e-134">SQL virtual machine management type.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e41e-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="5e41e-135">-Tag</span></span>
<span data-ttu-id="5e41e-136">Tag da associare alla macchina virtuale SQL</span><span class="sxs-lookup"><span data-stu-id="5e41e-136">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: NameParamaterList, ResourceIdParamaterList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e41e-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5e41e-137">-Confirm</span></span>
<span data-ttu-id="5e41e-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e41e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e41e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e41e-139">-WhatIf</span></span>
<span data-ttu-id="5e41e-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e41e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e41e-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e41e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e41e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e41e-142">CommonParameters</span></span>
<span data-ttu-id="5e41e-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e41e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e41e-144">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e41e-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e41e-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e41e-145">INPUTS</span></span>

### <span data-ttu-id="5e41e-146">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="5e41e-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="5e41e-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e41e-147">OUTPUTS</span></span>

### <span data-ttu-id="5e41e-148">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="5e41e-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="5e41e-149">Note</span><span class="sxs-lookup"><span data-stu-id="5e41e-149">NOTES</span></span>

## <span data-ttu-id="5e41e-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e41e-150">RELATED LINKS</span></span>
