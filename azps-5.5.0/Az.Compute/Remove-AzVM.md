---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 6e733bfecea9a054bbab3794ca61778894c613fe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199207"
---
# <span data-ttu-id="78a89-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="78a89-101">Remove-AzVM</span></span>

## <span data-ttu-id="78a89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78a89-102">SYNOPSIS</span></span>
<span data-ttu-id="78a89-103">Rimuove una macchina virtuale da Azure.</span><span class="sxs-lookup"><span data-stu-id="78a89-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="78a89-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="78a89-104">SYNTAX</span></span>

### <span data-ttu-id="78a89-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="78a89-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78a89-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="78a89-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Force] [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78a89-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="78a89-107">DESCRIPTION</span></span>
<span data-ttu-id="78a89-108">Il cmdlet **Remove-AzVM** rimuove una macchina virtuale da Azure.</span><span class="sxs-lookup"><span data-stu-id="78a89-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="78a89-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="78a89-109">EXAMPLES</span></span>

### <span data-ttu-id="78a89-110">Esempio 1: Rimuovere una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="78a89-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="78a89-111">Questo comando rimuove la macchina virtuale denominata VirtualMachine07 nel gruppo di risorse ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="78a89-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="78a89-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78a89-112">PARAMETERS</span></span>

### <span data-ttu-id="78a89-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78a89-113">-AsJob</span></span>
<span data-ttu-id="78a89-114">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="78a89-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="78a89-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78a89-115">-DefaultProfile</span></span>
<span data-ttu-id="78a89-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="78a89-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78a89-117">-Force</span><span class="sxs-lookup"><span data-stu-id="78a89-117">-Force</span></span>
<span data-ttu-id="78a89-118">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="78a89-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a89-119">-Id</span><span class="sxs-lookup"><span data-stu-id="78a89-119">-Id</span></span>
<span data-ttu-id="78a89-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="78a89-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78a89-121">-Name</span><span class="sxs-lookup"><span data-stu-id="78a89-121">-Name</span></span>
<span data-ttu-id="78a89-122">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="78a89-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78a89-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="78a89-123">-NoWait</span></span>
<span data-ttu-id="78a89-124">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="78a89-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="78a89-125">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="78a89-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="78a89-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78a89-126">-ResourceGroupName</span></span>
<span data-ttu-id="78a89-127">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="78a89-127">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78a89-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78a89-128">-Confirm</span></span>
<span data-ttu-id="78a89-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78a89-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a89-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78a89-130">-WhatIf</span></span>
<span data-ttu-id="78a89-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78a89-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78a89-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78a89-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a89-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78a89-133">CommonParameters</span></span>
<span data-ttu-id="78a89-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78a89-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78a89-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="78a89-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78a89-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="78a89-136">INPUTS</span></span>

### <span data-ttu-id="78a89-137">System.String</span><span class="sxs-lookup"><span data-stu-id="78a89-137">System.String</span></span>

## <span data-ttu-id="78a89-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="78a89-138">OUTPUTS</span></span>

### <span data-ttu-id="78a89-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="78a89-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="78a89-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="78a89-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="78a89-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="78a89-141">NOTES</span></span>

## <span data-ttu-id="78a89-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="78a89-142">RELATED LINKS</span></span>

[<span data-ttu-id="78a89-143">Get-AZVM</span><span class="sxs-lookup"><span data-stu-id="78a89-143">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="78a89-144">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="78a89-144">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="78a89-145">Restart-AZVM</span><span class="sxs-lookup"><span data-stu-id="78a89-145">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="78a89-146">Start-AZVM</span><span class="sxs-lookup"><span data-stu-id="78a89-146">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="78a89-147">Stop-AZVM</span><span class="sxs-lookup"><span data-stu-id="78a89-147">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="78a89-148">Update-AZVM</span><span class="sxs-lookup"><span data-stu-id="78a89-148">Update-AzVM</span></span>](./Update-AzVM.md)


