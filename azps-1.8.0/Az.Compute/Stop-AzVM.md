---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: 393f2a75217b95b6c1c5366326735ac0f78ac294
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836620"
---
# <span data-ttu-id="052d1-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="052d1-101">Stop-AzVM</span></span>

## <span data-ttu-id="052d1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="052d1-102">SYNOPSIS</span></span>
<span data-ttu-id="052d1-103">Interrompe una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="052d1-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="052d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="052d1-104">SYNTAX</span></span>

### <span data-ttu-id="052d1-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="052d1-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="052d1-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="052d1-106">IdParameterSetName</span></span>
```
Stop-AzVM [[-Name] <String>] [-Force] [-StayProvisioned] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="052d1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="052d1-107">DESCRIPTION</span></span>
<span data-ttu-id="052d1-108">Il cmdlet **Stop-AzVM** arresta una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="052d1-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="052d1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="052d1-109">EXAMPLES</span></span>

### <span data-ttu-id="052d1-110">Esempio 1: arrestare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="052d1-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="052d1-111">Questo comando Arresta la macchina virtuale denominata VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="052d1-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="052d1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="052d1-112">PARAMETERS</span></span>

### <span data-ttu-id="052d1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="052d1-113">-AsJob</span></span>
<span data-ttu-id="052d1-114">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="052d1-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="052d1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="052d1-115">-DefaultProfile</span></span>
<span data-ttu-id="052d1-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="052d1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="052d1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="052d1-117">-Force</span></span>
<span data-ttu-id="052d1-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="052d1-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="052d1-119">-ID</span><span class="sxs-lookup"><span data-stu-id="052d1-119">-Id</span></span>
<span data-ttu-id="052d1-120">ID della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="052d1-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="052d1-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="052d1-121">-Name</span></span>
<span data-ttu-id="052d1-122">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="052d1-122">The virtual machine name.</span></span>

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

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="052d1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="052d1-123">-ResourceGroupName</span></span>
<span data-ttu-id="052d1-124">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="052d1-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="052d1-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="052d1-125">-StayProvisioned</span></span>
<span data-ttu-id="052d1-126">Il cmdlet arresta tutte le macchine virtuali all'interno di VMSS, ma non le rilascia.</span><span class="sxs-lookup"><span data-stu-id="052d1-126">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="052d1-127">L'account viene addebitato per le macchine virtuali interrotte.</span><span class="sxs-lookup"><span data-stu-id="052d1-127">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="052d1-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="052d1-128">-Confirm</span></span>
<span data-ttu-id="052d1-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="052d1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="052d1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="052d1-130">-WhatIf</span></span>
<span data-ttu-id="052d1-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="052d1-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="052d1-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="052d1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="052d1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="052d1-133">CommonParameters</span></span>
<span data-ttu-id="052d1-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="052d1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="052d1-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="052d1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="052d1-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="052d1-136">INPUTS</span></span>

### <span data-ttu-id="052d1-137">System. String</span><span class="sxs-lookup"><span data-stu-id="052d1-137">System.String</span></span>

## <span data-ttu-id="052d1-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="052d1-138">OUTPUTS</span></span>

### <span data-ttu-id="052d1-139">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="052d1-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="052d1-140">Note</span><span class="sxs-lookup"><span data-stu-id="052d1-140">NOTES</span></span>

## <span data-ttu-id="052d1-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="052d1-141">RELATED LINKS</span></span>

[<span data-ttu-id="052d1-142">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="052d1-142">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="052d1-143">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="052d1-143">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="052d1-144">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="052d1-144">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="052d1-145">Riavviare-AzVM</span><span class="sxs-lookup"><span data-stu-id="052d1-145">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="052d1-146">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="052d1-146">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="052d1-147">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="052d1-147">Update-AzVM</span></span>](./Update-AzVM.md)


