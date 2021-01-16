---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
ms.openlocfilehash: d147fcd53b27031949bf51a33a59a9db86687d57
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334423"
---
# <span data-ttu-id="f0bc1-101">Remove-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="f0bc1-101">Remove-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="f0bc1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f0bc1-102">SYNOPSIS</span></span>
<span data-ttu-id="f0bc1-103">Elimina un listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="f0bc1-103">Deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="f0bc1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0bc1-104">SYNTAX</span></span>

### <span data-ttu-id="f0bc1-105">Nome (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f0bc1-105">Name (Default)</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0bc1-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f0bc1-106">InputObject</span></span>
```
Remove-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0bc1-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0bc1-107">ResourceId</span></span>
```
Remove-AzAvailabilityGroupListener [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0bc1-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="f0bc1-108">SqlVmGroupObject</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0bc1-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0bc1-109">DESCRIPTION</span></span>
<span data-ttu-id="f0bc1-110">Il cmdlet Remove-AzAvailabilityGroupListener Elimina un listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="f0bc1-110">The Remove-AzAvailabilityGroupListener cmdlet deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="f0bc1-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0bc1-111">EXAMPLES</span></span>

### <span data-ttu-id="f0bc1-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f0bc1-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="f0bc1-113">Nome ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="f0bc1-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="f0bc1-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="f0bc1-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="f0bc1-115">Elimina il listener del gruppo di disponibilità AgListener01 nel gruppo di disponibilità AvailabilityGroup01.</span><span class="sxs-lookup"><span data-stu-id="f0bc1-115">Deletes the Availability Group Listener AgListener01 in the Availability Group AvailabilityGroup01.</span></span>

## <span data-ttu-id="f0bc1-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f0bc1-116">PARAMETERS</span></span>

### <span data-ttu-id="f0bc1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0bc1-117">-AsJob</span></span>
<span data-ttu-id="f0bc1-118">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="f0bc1-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="f0bc1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0bc1-119">-DefaultProfile</span></span>
<span data-ttu-id="f0bc1-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f0bc1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0bc1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0bc1-121">-InputObject</span></span>
<span data-ttu-id="f0bc1-122">Oggetto listener gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="f0bc1-122">Availability Group Listener object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0bc1-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="f0bc1-123">-Name</span></span>
<span data-ttu-id="f0bc1-124">Nome del listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="f0bc1-124">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, SqlVmGroupObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0bc1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0bc1-125">-PassThru</span></span>
<span data-ttu-id="f0bc1-126">Specifica se restituire la risorsa eliminata alla fine dell'esecuzione del cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0bc1-126">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="f0bc1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0bc1-127">-ResourceGroupName</span></span>
<span data-ttu-id="f0bc1-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f0bc1-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="f0bc1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0bc1-129">-ResourceId</span></span>
<span data-ttu-id="f0bc1-130">ID risorsa listener del gruppo di disponibilità</span><span class="sxs-lookup"><span data-stu-id="f0bc1-130">Availability Group Listener Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0bc1-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="f0bc1-131">-SqlVMGroupName</span></span>
<span data-ttu-id="f0bc1-132">Nome del gruppo di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="f0bc1-132">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0bc1-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="f0bc1-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="f0bc1-134">Oggetto gruppo di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="f0bc1-134">SQL virtual machine Group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: SqlVmGroupObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0bc1-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f0bc1-135">-Confirm</span></span>
<span data-ttu-id="f0bc1-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0bc1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0bc1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0bc1-137">-WhatIf</span></span>
<span data-ttu-id="f0bc1-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0bc1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0bc1-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0bc1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0bc1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0bc1-140">CommonParameters</span></span>
<span data-ttu-id="f0bc1-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0bc1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0bc1-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0bc1-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0bc1-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f0bc1-143">INPUTS</span></span>

### <span data-ttu-id="f0bc1-144">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="f0bc1-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="f0bc1-145">System. String</span><span class="sxs-lookup"><span data-stu-id="f0bc1-145">System.String</span></span>

### <span data-ttu-id="f0bc1-146">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="f0bc1-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="f0bc1-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0bc1-147">OUTPUTS</span></span>

### <span data-ttu-id="f0bc1-148">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="f0bc1-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="f0bc1-149">Note</span><span class="sxs-lookup"><span data-stu-id="f0bc1-149">NOTES</span></span>

## <span data-ttu-id="f0bc1-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0bc1-150">RELATED LINKS</span></span>
