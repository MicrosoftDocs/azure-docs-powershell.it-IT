---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: 32e633d1f9fea877ef81b6c6e7ef5e8bb09da81a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200655"
---
# <span data-ttu-id="2cc7e-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="2cc7e-101">Start-AzVM</span></span>

## <span data-ttu-id="2cc7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cc7e-102">SYNOPSIS</span></span>
<span data-ttu-id="2cc7e-103">Avvia una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="2cc7e-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="2cc7e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2cc7e-104">SYNTAX</span></span>

### <span data-ttu-id="2cc7e-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2cc7e-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cc7e-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2cc7e-106">IdParameterSetName</span></span>
```
Start-AzVM [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2cc7e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2cc7e-107">DESCRIPTION</span></span>
<span data-ttu-id="2cc7e-108">Il **cmdlet Start-AzVM avvia** una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="2cc7e-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="2cc7e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2cc7e-109">EXAMPLES</span></span>

### <span data-ttu-id="2cc7e-110">Esempio 1: Avviare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="2cc7e-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="2cc7e-111">Questo comando avvia la macchina virtuale denominata VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2cc7e-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="2cc7e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cc7e-112">PARAMETERS</span></span>

### <span data-ttu-id="2cc7e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2cc7e-113">-AsJob</span></span>
<span data-ttu-id="2cc7e-114">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="2cc7e-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2cc7e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cc7e-115">-DefaultProfile</span></span>
<span data-ttu-id="2cc7e-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2cc7e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cc7e-117">-Id</span><span class="sxs-lookup"><span data-stu-id="2cc7e-117">-Id</span></span>
<span data-ttu-id="2cc7e-118">ID della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2cc7e-118">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="2cc7e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2cc7e-119">-Name</span></span>
<span data-ttu-id="2cc7e-120">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2cc7e-120">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cc7e-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2cc7e-121">-NoWait</span></span>
<span data-ttu-id="2cc7e-122">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2cc7e-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="2cc7e-123">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="2cc7e-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="2cc7e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cc7e-124">-ResourceGroupName</span></span>
<span data-ttu-id="2cc7e-125">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2cc7e-125">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="2cc7e-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2cc7e-126">-Confirm</span></span>
<span data-ttu-id="2cc7e-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cc7e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cc7e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cc7e-128">-WhatIf</span></span>
<span data-ttu-id="2cc7e-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2cc7e-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2cc7e-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2cc7e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cc7e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cc7e-131">CommonParameters</span></span>
<span data-ttu-id="2cc7e-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cc7e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cc7e-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2cc7e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cc7e-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="2cc7e-134">INPUTS</span></span>

### <span data-ttu-id="2cc7e-135">System.String</span><span class="sxs-lookup"><span data-stu-id="2cc7e-135">System.String</span></span>

## <span data-ttu-id="2cc7e-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2cc7e-136">OUTPUTS</span></span>

### <span data-ttu-id="2cc7e-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="2cc7e-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="2cc7e-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2cc7e-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2cc7e-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="2cc7e-139">NOTES</span></span>

## <span data-ttu-id="2cc7e-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2cc7e-140">RELATED LINKS</span></span>

[<span data-ttu-id="2cc7e-141">Get-AZVM</span><span class="sxs-lookup"><span data-stu-id="2cc7e-141">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="2cc7e-142">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="2cc7e-142">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="2cc7e-143">Remove-AZVM</span><span class="sxs-lookup"><span data-stu-id="2cc7e-143">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="2cc7e-144">Restart-AZVM</span><span class="sxs-lookup"><span data-stu-id="2cc7e-144">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="2cc7e-145">Stop-AZVM</span><span class="sxs-lookup"><span data-stu-id="2cc7e-145">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="2cc7e-146">Update-AZVM</span><span class="sxs-lookup"><span data-stu-id="2cc7e-146">Update-AzVM</span></span>](./Update-AzVM.md)


