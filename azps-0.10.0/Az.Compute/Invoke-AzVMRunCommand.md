---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
ms.openlocfilehash: 3036b26c4f3ebe6fc6f039f1754acdb3b50977f6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863673"
---
# <span data-ttu-id="8c646-101">Invoke-AzVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="8c646-101">Invoke-AzVMRunCommand</span></span>

## <span data-ttu-id="8c646-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8c646-102">SYNOPSIS</span></span>
<span data-ttu-id="8c646-103">Esegui comando nella VM.</span><span class="sxs-lookup"><span data-stu-id="8c646-103">Run command on the VM.</span></span>

## <span data-ttu-id="8c646-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c646-104">SYNTAX</span></span>

### <span data-ttu-id="8c646-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8c646-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c646-106">VMParameter</span><span class="sxs-lookup"><span data-stu-id="8c646-106">VMParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8c646-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c646-107">DESCRIPTION</span></span>
<span data-ttu-id="8c646-108">Richiamare un comando Esegui nella VM.</span><span class="sxs-lookup"><span data-stu-id="8c646-108">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="8c646-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c646-109">EXAMPLES</span></span>

### <span data-ttu-id="8c646-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8c646-110">Example 1</span></span>
```
PS C:\> Invoke-AzVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="8c646-111">Richiamare un comando Esegui di RunPowerShellScript con l'override dello script "sample.ps1" e i parametri della VM di "VMName" nel gruppo di risorse "RgName".</span><span class="sxs-lookup"><span data-stu-id="8c646-111">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="8c646-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8c646-112">PARAMETERS</span></span>

### <span data-ttu-id="8c646-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c646-113">-AsJob</span></span>
<span data-ttu-id="8c646-114">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="8c646-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8c646-115">-CommandID</span><span class="sxs-lookup"><span data-stu-id="8c646-115">-CommandId</span></span>
<span data-ttu-id="8c646-116">ID comando Esegui.</span><span class="sxs-lookup"><span data-stu-id="8c646-116">The run command id.</span></span>

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

### <span data-ttu-id="8c646-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c646-117">-DefaultProfile</span></span>
<span data-ttu-id="8c646-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8c646-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c646-119">Parametro-</span><span class="sxs-lookup"><span data-stu-id="8c646-119">-Parameter</span></span>
<span data-ttu-id="8c646-120">Parametri di comando Esegui.</span><span class="sxs-lookup"><span data-stu-id="8c646-120">The run command parameters.</span></span>

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

### <span data-ttu-id="8c646-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c646-121">-ResourceGroupName</span></span>
<span data-ttu-id="8c646-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8c646-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="8c646-123">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="8c646-123">-ScriptPath</span></span>
<span data-ttu-id="8c646-124">Percorso dello script da eseguire.</span><span class="sxs-lookup"><span data-stu-id="8c646-124">Path of the script to be executed.</span></span>  <span data-ttu-id="8c646-125">Quando questo valore viene assegnato, lo script indicato eseguirà l'override dello script predefinito del comando.</span><span class="sxs-lookup"><span data-stu-id="8c646-125">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="8c646-126">-VM</span><span class="sxs-lookup"><span data-stu-id="8c646-126">-VM</span></span>
<span data-ttu-id="8c646-127">Oggetto macchina virtuale PS.</span><span class="sxs-lookup"><span data-stu-id="8c646-127">The PS virtual Machine Object.</span></span>

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

### <span data-ttu-id="8c646-128">-VMName</span><span class="sxs-lookup"><span data-stu-id="8c646-128">-VMName</span></span>
<span data-ttu-id="8c646-129">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8c646-129">The name of the virtual machine.</span></span>

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

### <span data-ttu-id="8c646-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8c646-130">-Confirm</span></span>
<span data-ttu-id="8c646-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c646-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c646-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c646-132">-WhatIf</span></span>
<span data-ttu-id="8c646-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8c646-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c646-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8c646-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c646-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c646-135">CommonParameters</span></span>
<span data-ttu-id="8c646-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c646-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c646-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c646-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c646-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8c646-138">INPUTS</span></span>

### <span data-ttu-id="8c646-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8c646-139">System.String</span></span>
<span data-ttu-id="8c646-140">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8c646-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="8c646-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c646-141">OUTPUTS</span></span>

### <span data-ttu-id="8c646-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="8c646-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="8c646-143">Note</span><span class="sxs-lookup"><span data-stu-id="8c646-143">NOTES</span></span>

## <span data-ttu-id="8c646-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c646-144">RELATED LINKS</span></span>

