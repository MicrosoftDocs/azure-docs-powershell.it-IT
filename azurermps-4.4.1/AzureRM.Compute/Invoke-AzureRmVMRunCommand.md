---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
ms.openlocfilehash: 2402591c6c388dbe7c1c6b24a1beb2b298012d4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521978"
---
# <span data-ttu-id="589da-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="589da-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="589da-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="589da-102">SYNOPSIS</span></span>
<span data-ttu-id="589da-103">Esegui comando nella VM.</span><span class="sxs-lookup"><span data-stu-id="589da-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="589da-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="589da-104">SYNTAX</span></span>

### <span data-ttu-id="589da-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="589da-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="589da-106">VMParameter</span><span class="sxs-lookup"><span data-stu-id="589da-106">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="589da-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="589da-107">DESCRIPTION</span></span>
<span data-ttu-id="589da-108">Richiamare un comando Esegui nella VM.</span><span class="sxs-lookup"><span data-stu-id="589da-108">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="589da-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="589da-109">EXAMPLES</span></span>

### <span data-ttu-id="589da-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="589da-110">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="589da-111">Richiamare un comando Esegui di RunPowerShellScript con l'override dello script "sample.ps1" e i parametri della VM di "VMName" nel gruppo di risorse "RgName".</span><span class="sxs-lookup"><span data-stu-id="589da-111">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="589da-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="589da-112">PARAMETERS</span></span>

### <span data-ttu-id="589da-113">-CommandID</span><span class="sxs-lookup"><span data-stu-id="589da-113">-CommandId</span></span>
<span data-ttu-id="589da-114">ID comando Esegui.</span><span class="sxs-lookup"><span data-stu-id="589da-114">The run command id.</span></span>

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

### <span data-ttu-id="589da-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="589da-115">-DefaultProfile</span></span>
<span data-ttu-id="589da-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="589da-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="589da-117">Parametro-</span><span class="sxs-lookup"><span data-stu-id="589da-117">-Parameter</span></span>
<span data-ttu-id="589da-118">Parametri di comando Esegui.</span><span class="sxs-lookup"><span data-stu-id="589da-118">The run command parameters.</span></span>

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

### <span data-ttu-id="589da-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="589da-119">-ResourceGroupName</span></span>
<span data-ttu-id="589da-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="589da-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="589da-121">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="589da-121">-ScriptPath</span></span>
<span data-ttu-id="589da-122">Percorso dello script da eseguire.</span><span class="sxs-lookup"><span data-stu-id="589da-122">Path of the script to be executed.</span></span>  <span data-ttu-id="589da-123">Quando questo valore viene assegnato, lo script indicato eseguirà l'override dello script predefinito del comando.</span><span class="sxs-lookup"><span data-stu-id="589da-123">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="589da-124">-VM</span><span class="sxs-lookup"><span data-stu-id="589da-124">-VM</span></span>
<span data-ttu-id="589da-125">Oggetto macchina virtuale PS.</span><span class="sxs-lookup"><span data-stu-id="589da-125">The PS virtual Machine Object.</span></span>

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

### <span data-ttu-id="589da-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="589da-126">-VMName</span></span>
<span data-ttu-id="589da-127">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="589da-127">The name of the virtual machine.</span></span>

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

### <span data-ttu-id="589da-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="589da-128">-Confirm</span></span>
<span data-ttu-id="589da-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="589da-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="589da-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="589da-130">-WhatIf</span></span>
<span data-ttu-id="589da-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="589da-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="589da-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="589da-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="589da-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="589da-133">CommonParameters</span></span>
<span data-ttu-id="589da-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="589da-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="589da-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="589da-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="589da-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="589da-136">INPUTS</span></span>

### <span data-ttu-id="589da-137">System. String</span><span class="sxs-lookup"><span data-stu-id="589da-137">System.String</span></span>
<span data-ttu-id="589da-138">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="589da-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="589da-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="589da-139">OUTPUTS</span></span>

### <span data-ttu-id="589da-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="589da-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="589da-141">Note</span><span class="sxs-lookup"><span data-stu-id="589da-141">NOTES</span></span>

## <span data-ttu-id="589da-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="589da-142">RELATED LINKS</span></span>

