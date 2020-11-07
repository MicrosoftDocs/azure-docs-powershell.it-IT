---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVM.md
ms.openlocfilehash: 9ee07fc931e0760332456a83538621ded608049b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687343"
---
# <span data-ttu-id="5807f-101">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5807f-101">Stop-AzureRmVM</span></span>

## <span data-ttu-id="5807f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5807f-102">SYNOPSIS</span></span>
<span data-ttu-id="5807f-103">Interrompe una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="5807f-103">Stops an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5807f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5807f-104">SYNTAX</span></span>

### <span data-ttu-id="5807f-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5807f-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5807f-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="5807f-106">IdParameterSetName</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5807f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5807f-107">DESCRIPTION</span></span>
<span data-ttu-id="5807f-108">Il cmdlet **Stop-AzureRmVM** arresta una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="5807f-108">The **Stop-AzureRmVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="5807f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5807f-109">EXAMPLES</span></span>

### <span data-ttu-id="5807f-110">Esempio 1: arrestare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="5807f-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="5807f-111">Questo comando Arresta la macchina virtuale denominata VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="5807f-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="5807f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5807f-112">PARAMETERS</span></span>

### <span data-ttu-id="5807f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5807f-113">-AsJob</span></span>
<span data-ttu-id="5807f-114">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="5807f-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5807f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5807f-115">-DefaultProfile</span></span>
<span data-ttu-id="5807f-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5807f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5807f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5807f-117">-Force</span></span>
<span data-ttu-id="5807f-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="5807f-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5807f-119">-ID</span><span class="sxs-lookup"><span data-stu-id="5807f-119">-Id</span></span>
<span data-ttu-id="5807f-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5807f-120">The resource group name.</span></span>

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

### <span data-ttu-id="5807f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="5807f-121">-Name</span></span>
<span data-ttu-id="5807f-122">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5807f-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5807f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5807f-123">-ResourceGroupName</span></span>
<span data-ttu-id="5807f-124">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5807f-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5807f-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="5807f-125">-StayProvisioned</span></span>
<span data-ttu-id="5807f-126">Il cmdlet arresta tutte le macchine virtuali all'interno di VMSS, ma non le rilascia.</span><span class="sxs-lookup"><span data-stu-id="5807f-126">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="5807f-127">L'account viene addebitato per le macchine virtuali interrotte.</span><span class="sxs-lookup"><span data-stu-id="5807f-127">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="5807f-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5807f-128">-Confirm</span></span>
<span data-ttu-id="5807f-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5807f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5807f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5807f-130">-WhatIf</span></span>
<span data-ttu-id="5807f-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5807f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5807f-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5807f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5807f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5807f-133">CommonParameters</span></span>
<span data-ttu-id="5807f-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5807f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5807f-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5807f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5807f-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5807f-136">INPUTS</span></span>

### <span data-ttu-id="5807f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5807f-137">System.String</span></span>

## <span data-ttu-id="5807f-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5807f-138">OUTPUTS</span></span>

### <span data-ttu-id="5807f-139">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="5807f-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="5807f-140">Note</span><span class="sxs-lookup"><span data-stu-id="5807f-140">NOTES</span></span>

## <span data-ttu-id="5807f-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5807f-141">RELATED LINKS</span></span>

[<span data-ttu-id="5807f-142">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5807f-142">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="5807f-143">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5807f-143">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="5807f-144">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5807f-144">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="5807f-145">Riavviare-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5807f-145">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="5807f-146">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5807f-146">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="5807f-147">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5807f-147">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


