---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvm
schema: 2.0.0
ms.openlocfilehash: 4bf5ec5ccdbe79f5557cb2f400fbcc0b9baf5e5a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867138"
---
# <span data-ttu-id="274d7-101">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="274d7-101">Stop-AzureRmVM</span></span>

## <span data-ttu-id="274d7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="274d7-102">SYNOPSIS</span></span>
<span data-ttu-id="274d7-103">Interrompe una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="274d7-103">Stops an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="274d7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="274d7-104">SYNTAX</span></span>

### <span data-ttu-id="274d7-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="274d7-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="274d7-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="274d7-106">IdParameterSetName</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="274d7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="274d7-107">DESCRIPTION</span></span>
<span data-ttu-id="274d7-108">Il cmdlet **Stop-AzureRmVM** arresta una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="274d7-108">The **Stop-AzureRmVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="274d7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="274d7-109">EXAMPLES</span></span>

### <span data-ttu-id="274d7-110">Esempio 1: arrestare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="274d7-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="274d7-111">Questo comando Arresta la macchina virtuale denominata VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="274d7-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="274d7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="274d7-112">PARAMETERS</span></span>

### <span data-ttu-id="274d7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="274d7-113">-AsJob</span></span>
<span data-ttu-id="274d7-114">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="274d7-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="274d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="274d7-115">-DefaultProfile</span></span>
<span data-ttu-id="274d7-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="274d7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="274d7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="274d7-117">-Force</span></span>
<span data-ttu-id="274d7-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="274d7-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="274d7-119">-ID</span><span class="sxs-lookup"><span data-stu-id="274d7-119">-Id</span></span>
<span data-ttu-id="274d7-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="274d7-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="274d7-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="274d7-121">-Name</span></span>
<span data-ttu-id="274d7-122">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="274d7-122">The virtual machine name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="274d7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="274d7-123">-ResourceGroupName</span></span>
<span data-ttu-id="274d7-124">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="274d7-124">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="274d7-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="274d7-125">-StayProvisioned</span></span>
<span data-ttu-id="274d7-126">Il cmdlet arresta tutte le macchine virtuali all'interno di VMSS, ma non le rilascia.</span><span class="sxs-lookup"><span data-stu-id="274d7-126">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="274d7-127">L'account viene addebitato per le macchine virtuali interrotte.</span><span class="sxs-lookup"><span data-stu-id="274d7-127">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="274d7-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="274d7-128">-Confirm</span></span>
<span data-ttu-id="274d7-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="274d7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="274d7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="274d7-130">-WhatIf</span></span>
<span data-ttu-id="274d7-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="274d7-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="274d7-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="274d7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="274d7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="274d7-133">CommonParameters</span></span>
<span data-ttu-id="274d7-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="274d7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="274d7-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="274d7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="274d7-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="274d7-136">INPUTS</span></span>

### <span data-ttu-id="274d7-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="274d7-137">None</span></span>
<span data-ttu-id="274d7-138">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="274d7-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="274d7-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="274d7-139">OUTPUTS</span></span>

### <span data-ttu-id="274d7-140">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="274d7-140">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="274d7-141">Note</span><span class="sxs-lookup"><span data-stu-id="274d7-141">NOTES</span></span>

## <span data-ttu-id="274d7-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="274d7-142">RELATED LINKS</span></span>

[<span data-ttu-id="274d7-143">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="274d7-143">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="274d7-144">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="274d7-144">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="274d7-145">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="274d7-145">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="274d7-146">Riavviare-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="274d7-146">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="274d7-147">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="274d7-147">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="274d7-148">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="274d7-148">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


