---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/invoke-azurermvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
ms.openlocfilehash: 7d3c27ad8dacb288aeb0d15235aacc48405b8a6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687934"
---
# <span data-ttu-id="8097b-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="8097b-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="8097b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8097b-102">SYNOPSIS</span></span>
<span data-ttu-id="8097b-103">Esegui comando nella VM.</span><span class="sxs-lookup"><span data-stu-id="8097b-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8097b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8097b-104">SYNTAX</span></span>

### <span data-ttu-id="8097b-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8097b-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8097b-106">VMParameter</span><span class="sxs-lookup"><span data-stu-id="8097b-106">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8097b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8097b-107">DESCRIPTION</span></span>
<span data-ttu-id="8097b-108">Richiamare un comando Esegui nella VM.</span><span class="sxs-lookup"><span data-stu-id="8097b-108">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="8097b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8097b-109">EXAMPLES</span></span>

### <span data-ttu-id="8097b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8097b-110">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="8097b-111">Richiamare un comando Esegui di RunPowerShellScript con l'override dello script "sample.ps1" e i parametri della VM di "VMName" nel gruppo di risorse "RgName".</span><span class="sxs-lookup"><span data-stu-id="8097b-111">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="8097b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8097b-112">PARAMETERS</span></span>

### <span data-ttu-id="8097b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8097b-113">-AsJob</span></span>
<span data-ttu-id="8097b-114">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="8097b-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8097b-115">-CommandID</span><span class="sxs-lookup"><span data-stu-id="8097b-115">-CommandId</span></span>
<span data-ttu-id="8097b-116">ID comando Esegui.</span><span class="sxs-lookup"><span data-stu-id="8097b-116">The run command id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8097b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8097b-117">-DefaultProfile</span></span>
<span data-ttu-id="8097b-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8097b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8097b-119">Parametro-</span><span class="sxs-lookup"><span data-stu-id="8097b-119">-Parameter</span></span>
<span data-ttu-id="8097b-120">Parametri di comando Esegui.</span><span class="sxs-lookup"><span data-stu-id="8097b-120">The run command parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8097b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8097b-121">-ResourceGroupName</span></span>
<span data-ttu-id="8097b-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8097b-122">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8097b-123">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="8097b-123">-ScriptPath</span></span>
<span data-ttu-id="8097b-124">Percorso dello script da eseguire.</span><span class="sxs-lookup"><span data-stu-id="8097b-124">Path of the script to be executed.</span></span>  <span data-ttu-id="8097b-125">Quando questo valore viene assegnato, lo script indicato eseguirà l'override dello script predefinito del comando.</span><span class="sxs-lookup"><span data-stu-id="8097b-125">When this value is given, the given script will override the default script of the command.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8097b-126">-VM</span><span class="sxs-lookup"><span data-stu-id="8097b-126">-VM</span></span>
<span data-ttu-id="8097b-127">Oggetto macchina virtuale PS.</span><span class="sxs-lookup"><span data-stu-id="8097b-127">The PS virtual Machine Object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: VMParameter
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8097b-128">-VMName</span><span class="sxs-lookup"><span data-stu-id="8097b-128">-VMName</span></span>
<span data-ttu-id="8097b-129">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8097b-129">The name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8097b-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8097b-130">-Confirm</span></span>
<span data-ttu-id="8097b-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8097b-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8097b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8097b-132">-WhatIf</span></span>
<span data-ttu-id="8097b-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8097b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8097b-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8097b-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8097b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8097b-135">CommonParameters</span></span>
<span data-ttu-id="8097b-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8097b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8097b-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8097b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8097b-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8097b-138">INPUTS</span></span>

### <span data-ttu-id="8097b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8097b-139">System.String</span></span>
<span data-ttu-id="8097b-140">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8097b-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="8097b-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8097b-141">OUTPUTS</span></span>

### <span data-ttu-id="8097b-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="8097b-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="8097b-143">Note</span><span class="sxs-lookup"><span data-stu-id="8097b-143">NOTES</span></span>

## <span data-ttu-id="8097b-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8097b-144">RELATED LINKS</span></span>
