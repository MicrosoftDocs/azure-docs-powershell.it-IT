---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/invoke-azurermvmruncommand
schema: 2.0.0
ms.openlocfilehash: 12b9b3870b5239746a8524bad9aad0f44161acd1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866565"
---
# <span data-ttu-id="ee904-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="ee904-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="ee904-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee904-102">SYNOPSIS</span></span>
<span data-ttu-id="ee904-103">Esegui comando nella VM.</span><span class="sxs-lookup"><span data-stu-id="ee904-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee904-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee904-104">SYNTAX</span></span>

### <span data-ttu-id="ee904-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ee904-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee904-106">VMParameter</span><span class="sxs-lookup"><span data-stu-id="ee904-106">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ee904-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee904-107">DESCRIPTION</span></span>
<span data-ttu-id="ee904-108">Richiamare un comando Esegui nella VM.</span><span class="sxs-lookup"><span data-stu-id="ee904-108">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="ee904-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee904-109">EXAMPLES</span></span>

### <span data-ttu-id="ee904-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ee904-110">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="ee904-111">Richiamare un comando Esegui di RunPowerShellScript con l'override dello script "sample.ps1" e i parametri della VM di "VMName" nel gruppo di risorse "RgName".</span><span class="sxs-lookup"><span data-stu-id="ee904-111">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="ee904-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee904-112">PARAMETERS</span></span>

### <span data-ttu-id="ee904-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee904-113">-AsJob</span></span>
<span data-ttu-id="ee904-114">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="ee904-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ee904-115">-CommandID</span><span class="sxs-lookup"><span data-stu-id="ee904-115">-CommandId</span></span>
<span data-ttu-id="ee904-116">ID comando Esegui.</span><span class="sxs-lookup"><span data-stu-id="ee904-116">The run command id.</span></span>

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

### <span data-ttu-id="ee904-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee904-117">-DefaultProfile</span></span>
<span data-ttu-id="ee904-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ee904-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee904-119">Parametro-</span><span class="sxs-lookup"><span data-stu-id="ee904-119">-Parameter</span></span>
<span data-ttu-id="ee904-120">Parametri di comando Esegui.</span><span class="sxs-lookup"><span data-stu-id="ee904-120">The run command parameters.</span></span>

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

### <span data-ttu-id="ee904-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee904-121">-ResourceGroupName</span></span>
<span data-ttu-id="ee904-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ee904-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="ee904-123">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="ee904-123">-ScriptPath</span></span>
<span data-ttu-id="ee904-124">Percorso dello script da eseguire.</span><span class="sxs-lookup"><span data-stu-id="ee904-124">Path of the script to be executed.</span></span>  <span data-ttu-id="ee904-125">Quando questo valore viene assegnato, lo script indicato eseguirà l'override dello script predefinito del comando.</span><span class="sxs-lookup"><span data-stu-id="ee904-125">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="ee904-126">-VM</span><span class="sxs-lookup"><span data-stu-id="ee904-126">-VM</span></span>
<span data-ttu-id="ee904-127">Oggetto macchina virtuale PS.</span><span class="sxs-lookup"><span data-stu-id="ee904-127">The PS virtual Machine Object.</span></span>

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

### <span data-ttu-id="ee904-128">-VMName</span><span class="sxs-lookup"><span data-stu-id="ee904-128">-VMName</span></span>
<span data-ttu-id="ee904-129">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ee904-129">The name of the virtual machine.</span></span>

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

### <span data-ttu-id="ee904-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ee904-130">-Confirm</span></span>
<span data-ttu-id="ee904-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee904-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee904-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee904-132">-WhatIf</span></span>
<span data-ttu-id="ee904-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee904-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee904-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee904-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee904-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee904-135">CommonParameters</span></span>
<span data-ttu-id="ee904-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee904-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee904-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee904-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee904-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee904-138">INPUTS</span></span>

### <span data-ttu-id="ee904-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ee904-139">System.String</span></span>
<span data-ttu-id="ee904-140">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ee904-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ee904-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee904-141">OUTPUTS</span></span>

### <span data-ttu-id="ee904-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="ee904-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="ee904-143">Note</span><span class="sxs-lookup"><span data-stu-id="ee904-143">NOTES</span></span>

## <span data-ttu-id="ee904-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee904-144">RELATED LINKS</span></span>

