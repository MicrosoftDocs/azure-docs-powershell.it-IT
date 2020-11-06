---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/invoke-azurermvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
ms.openlocfilehash: 89d81387f8a97fe02f607ddc9d13d4645fc9688b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515488"
---
# <span data-ttu-id="bcc98-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="bcc98-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="bcc98-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bcc98-102">SYNOPSIS</span></span>
<span data-ttu-id="bcc98-103">Esegui comando nella VM.</span><span class="sxs-lookup"><span data-stu-id="bcc98-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcc98-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bcc98-104">SYNTAX</span></span>

### <span data-ttu-id="bcc98-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bcc98-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcc98-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="bcc98-106">ResourceIdParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bcc98-107">VMParameter</span><span class="sxs-lookup"><span data-stu-id="bcc98-107">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bcc98-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bcc98-108">DESCRIPTION</span></span>
<span data-ttu-id="bcc98-109">Richiamare un comando Esegui nella VM.</span><span class="sxs-lookup"><span data-stu-id="bcc98-109">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="bcc98-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bcc98-110">EXAMPLES</span></span>

### <span data-ttu-id="bcc98-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bcc98-111">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="bcc98-112">Richiamare un comando Esegui di RunPowerShellScript con l'override dello script "sample.ps1" e i parametri della VM di "VMName" nel gruppo di risorse "RgName".</span><span class="sxs-lookup"><span data-stu-id="bcc98-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="bcc98-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bcc98-113">PARAMETERS</span></span>

### <span data-ttu-id="bcc98-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bcc98-114">-AsJob</span></span>
<span data-ttu-id="bcc98-115">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="bcc98-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="bcc98-116">-CommandID</span><span class="sxs-lookup"><span data-stu-id="bcc98-116">-CommandId</span></span>
<span data-ttu-id="bcc98-117">ID comando Esegui.</span><span class="sxs-lookup"><span data-stu-id="bcc98-117">The run command id.</span></span>

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

### <span data-ttu-id="bcc98-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcc98-118">-DefaultProfile</span></span>
<span data-ttu-id="bcc98-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bcc98-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcc98-120">Parametro-</span><span class="sxs-lookup"><span data-stu-id="bcc98-120">-Parameter</span></span>
<span data-ttu-id="bcc98-121">Parametri di comando Esegui.</span><span class="sxs-lookup"><span data-stu-id="bcc98-121">The run command parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcc98-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcc98-122">-ResourceGroupName</span></span>
<span data-ttu-id="bcc98-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bcc98-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcc98-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcc98-124">-ResourceId</span></span>
<span data-ttu-id="bcc98-125">ID risorsa per la VM</span><span class="sxs-lookup"><span data-stu-id="bcc98-125">The resource id for the VM</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcc98-126">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="bcc98-126">-ScriptPath</span></span>
<span data-ttu-id="bcc98-127">Percorso dello script da eseguire.</span><span class="sxs-lookup"><span data-stu-id="bcc98-127">Path of the script to be executed.</span></span>  <span data-ttu-id="bcc98-128">Quando questo valore viene assegnato, lo script indicato eseguirà l'override dello script predefinito del comando.</span><span class="sxs-lookup"><span data-stu-id="bcc98-128">When this value is given, the given script will override the default script of the command.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcc98-129">-VM</span><span class="sxs-lookup"><span data-stu-id="bcc98-129">-VM</span></span>
<span data-ttu-id="bcc98-130">Oggetto macchina virtuale PS.</span><span class="sxs-lookup"><span data-stu-id="bcc98-130">The PS virtual Machine Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameter
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcc98-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="bcc98-131">-VMName</span></span>
<span data-ttu-id="bcc98-132">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bcc98-132">The name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcc98-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bcc98-133">-Confirm</span></span>
<span data-ttu-id="bcc98-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcc98-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcc98-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcc98-135">-WhatIf</span></span>
<span data-ttu-id="bcc98-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bcc98-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcc98-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bcc98-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcc98-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcc98-138">CommonParameters</span></span>
<span data-ttu-id="bcc98-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcc98-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcc98-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcc98-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcc98-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bcc98-141">INPUTS</span></span>

### <span data-ttu-id="bcc98-142">System. String</span><span class="sxs-lookup"><span data-stu-id="bcc98-142">System.String</span></span>

### <span data-ttu-id="bcc98-143">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="bcc98-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="bcc98-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bcc98-144">OUTPUTS</span></span>

### <span data-ttu-id="bcc98-145">Microsoft. Azure. Commands. Compute. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="bcc98-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="bcc98-146">Note</span><span class="sxs-lookup"><span data-stu-id="bcc98-146">NOTES</span></span>

## <span data-ttu-id="bcc98-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bcc98-147">RELATED LINKS</span></span>