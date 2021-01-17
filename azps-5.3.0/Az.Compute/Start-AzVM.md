---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: 32e633d1f9fea877ef81b6c6e7ef5e8bb09da81a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477639"
---
# <span data-ttu-id="c145f-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="c145f-101">Start-AzVM</span></span>

## <span data-ttu-id="c145f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c145f-102">SYNOPSIS</span></span>
<span data-ttu-id="c145f-103">Avvia una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="c145f-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="c145f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c145f-104">SYNTAX</span></span>

### <span data-ttu-id="c145f-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c145f-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c145f-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="c145f-106">IdParameterSetName</span></span>
```
Start-AzVM [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c145f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c145f-107">DESCRIPTION</span></span>
<span data-ttu-id="c145f-108">Il cmdlet **Start-AzVM** avvia una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="c145f-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="c145f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c145f-109">EXAMPLES</span></span>

### <span data-ttu-id="c145f-110">Esempio 1: avviare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="c145f-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="c145f-111">Questo comando avvia la macchina virtuale denominata VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c145f-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="c145f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c145f-112">PARAMETERS</span></span>

### <span data-ttu-id="c145f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c145f-113">-AsJob</span></span>
<span data-ttu-id="c145f-114">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="c145f-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c145f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c145f-115">-DefaultProfile</span></span>
<span data-ttu-id="c145f-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c145f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c145f-117">-ID</span><span class="sxs-lookup"><span data-stu-id="c145f-117">-Id</span></span>
<span data-ttu-id="c145f-118">ID della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c145f-118">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="c145f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c145f-119">-Name</span></span>
<span data-ttu-id="c145f-120">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c145f-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="c145f-121">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="c145f-121">-NoWait</span></span>
<span data-ttu-id="c145f-122">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="c145f-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="c145f-123">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="c145f-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="c145f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c145f-124">-ResourceGroupName</span></span>
<span data-ttu-id="c145f-125">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c145f-125">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c145f-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c145f-126">-Confirm</span></span>
<span data-ttu-id="c145f-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c145f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c145f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c145f-128">-WhatIf</span></span>
<span data-ttu-id="c145f-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c145f-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c145f-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c145f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c145f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c145f-131">CommonParameters</span></span>
<span data-ttu-id="c145f-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c145f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c145f-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c145f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c145f-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c145f-134">INPUTS</span></span>

### <span data-ttu-id="c145f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c145f-135">System.String</span></span>

## <span data-ttu-id="c145f-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c145f-136">OUTPUTS</span></span>

### <span data-ttu-id="c145f-137">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="c145f-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="c145f-138">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c145f-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c145f-139">Note</span><span class="sxs-lookup"><span data-stu-id="c145f-139">NOTES</span></span>

## <span data-ttu-id="c145f-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c145f-140">RELATED LINKS</span></span>

[<span data-ttu-id="c145f-141">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="c145f-141">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="c145f-142">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="c145f-142">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="c145f-143">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="c145f-143">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="c145f-144">Riavviare-AzVM</span><span class="sxs-lookup"><span data-stu-id="c145f-144">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="c145f-145">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="c145f-145">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="c145f-146">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="c145f-146">Update-AzVM</span></span>](./Update-AzVM.md)


