---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvm
schema: 2.0.0
ms.openlocfilehash: 6cf37c453d47278958ccd84eaf817e6dc118b16b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686116"
---
# <span data-ttu-id="7782c-101">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7782c-101">Stop-AzureRmVM</span></span>

## <span data-ttu-id="7782c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7782c-102">SYNOPSIS</span></span>
<span data-ttu-id="7782c-103">Interrompe una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="7782c-103">Stops an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7782c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7782c-104">SYNTAX</span></span>

### <span data-ttu-id="7782c-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7782c-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7782c-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="7782c-106">IdParameterSetName</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7782c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7782c-107">DESCRIPTION</span></span>
<span data-ttu-id="7782c-108">Il cmdlet **Stop-AzureRmVM** arresta una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="7782c-108">The **Stop-AzureRmVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="7782c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7782c-109">EXAMPLES</span></span>

### <span data-ttu-id="7782c-110">Esempio 1: arrestare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="7782c-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="7782c-111">Questo comando Arresta la macchina virtuale denominata VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="7782c-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="7782c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7782c-112">PARAMETERS</span></span>

### <span data-ttu-id="7782c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7782c-113">-AsJob</span></span>
<span data-ttu-id="7782c-114">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="7782c-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7782c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7782c-115">-DefaultProfile</span></span>
<span data-ttu-id="7782c-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7782c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7782c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7782c-117">-Force</span></span>
<span data-ttu-id="7782c-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7782c-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7782c-119">-ID</span><span class="sxs-lookup"><span data-stu-id="7782c-119">-Id</span></span>
<span data-ttu-id="7782c-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7782c-120">The resource group name.</span></span>

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

### <span data-ttu-id="7782c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="7782c-121">-Name</span></span>
<span data-ttu-id="7782c-122">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7782c-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="7782c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7782c-123">-ResourceGroupName</span></span>
<span data-ttu-id="7782c-124">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7782c-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7782c-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="7782c-125">-StayProvisioned</span></span>
<span data-ttu-id="7782c-126">Il cmdlet arresta tutte le macchine virtuali all'interno di VMSS, ma non le rilascia.</span><span class="sxs-lookup"><span data-stu-id="7782c-126">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="7782c-127">L'account viene addebitato per le macchine virtuali interrotte.</span><span class="sxs-lookup"><span data-stu-id="7782c-127">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="7782c-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7782c-128">-Confirm</span></span>
<span data-ttu-id="7782c-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7782c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7782c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7782c-130">-WhatIf</span></span>
<span data-ttu-id="7782c-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7782c-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7782c-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7782c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7782c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7782c-133">CommonParameters</span></span>
<span data-ttu-id="7782c-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7782c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7782c-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7782c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7782c-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7782c-136">INPUTS</span></span>

### <span data-ttu-id="7782c-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7782c-137">None</span></span>
<span data-ttu-id="7782c-138">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="7782c-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7782c-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7782c-139">OUTPUTS</span></span>

### <span data-ttu-id="7782c-140">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="7782c-140">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="7782c-141">Note</span><span class="sxs-lookup"><span data-stu-id="7782c-141">NOTES</span></span>

## <span data-ttu-id="7782c-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7782c-142">RELATED LINKS</span></span>

[<span data-ttu-id="7782c-143">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7782c-143">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="7782c-144">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7782c-144">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="7782c-145">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7782c-145">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="7782c-146">Riavviare-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7782c-146">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="7782c-147">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7782c-147">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="7782c-148">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7782c-148">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


