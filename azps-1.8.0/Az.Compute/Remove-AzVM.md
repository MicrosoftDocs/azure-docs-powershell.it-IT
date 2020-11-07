---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 5a7f03cbd4fdac75743fed491697ac2bb4ff6dac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852010"
---
# <span data-ttu-id="1250f-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="1250f-101">Remove-AzVM</span></span>

## <span data-ttu-id="1250f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1250f-102">SYNOPSIS</span></span>
<span data-ttu-id="1250f-103">Rimuove una macchina virtuale da Azure.</span><span class="sxs-lookup"><span data-stu-id="1250f-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="1250f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1250f-104">SYNTAX</span></span>

### <span data-ttu-id="1250f-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1250f-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1250f-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="1250f-106">IdParameterSetName</span></span>
```
Remove-AzVM [[-Name] <String>] [-Force] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1250f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1250f-107">DESCRIPTION</span></span>
<span data-ttu-id="1250f-108">Il cmdlet **Remove-AzVM** rimuove una macchina virtuale da Azure.</span><span class="sxs-lookup"><span data-stu-id="1250f-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="1250f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1250f-109">EXAMPLES</span></span>

### <span data-ttu-id="1250f-110">Esempio 1: rimuovere una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="1250f-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="1250f-111">Questo comando rimuove la macchina virtuale denominata VirtualMachine07 nel gruppo di risorse ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1250f-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="1250f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1250f-112">PARAMETERS</span></span>

### <span data-ttu-id="1250f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1250f-113">-AsJob</span></span>
<span data-ttu-id="1250f-114">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="1250f-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="1250f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1250f-115">-DefaultProfile</span></span>
<span data-ttu-id="1250f-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1250f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1250f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1250f-117">-Force</span></span>
<span data-ttu-id="1250f-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1250f-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1250f-119">-ID</span><span class="sxs-lookup"><span data-stu-id="1250f-119">-Id</span></span>
<span data-ttu-id="1250f-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1250f-120">The resource group name.</span></span>

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

### <span data-ttu-id="1250f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1250f-121">-Name</span></span>
<span data-ttu-id="1250f-122">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="1250f-122">The resource name.</span></span>

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

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: ResourceName, VMName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1250f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1250f-123">-ResourceGroupName</span></span>
<span data-ttu-id="1250f-124">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1250f-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1250f-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1250f-125">-Confirm</span></span>
<span data-ttu-id="1250f-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1250f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1250f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1250f-127">-WhatIf</span></span>
<span data-ttu-id="1250f-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1250f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1250f-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1250f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1250f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1250f-130">CommonParameters</span></span>
<span data-ttu-id="1250f-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1250f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1250f-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1250f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1250f-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1250f-133">INPUTS</span></span>

### <span data-ttu-id="1250f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1250f-134">System.String</span></span>

## <span data-ttu-id="1250f-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1250f-135">OUTPUTS</span></span>

### <span data-ttu-id="1250f-136">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="1250f-136">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="1250f-137">Note</span><span class="sxs-lookup"><span data-stu-id="1250f-137">NOTES</span></span>

## <span data-ttu-id="1250f-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1250f-138">RELATED LINKS</span></span>

[<span data-ttu-id="1250f-139">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="1250f-139">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="1250f-140">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="1250f-140">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="1250f-141">Riavviare-AzVM</span><span class="sxs-lookup"><span data-stu-id="1250f-141">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="1250f-142">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="1250f-142">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="1250f-143">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="1250f-143">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="1250f-144">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="1250f-144">Update-AzVM</span></span>](./Update-AzVM.md)


