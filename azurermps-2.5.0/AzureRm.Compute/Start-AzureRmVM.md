---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvm
schema: 2.0.0
ms.openlocfilehash: 04110cb46d3f0ed0e5e09e6b12544b927cf6ae25
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866526"
---
# <span data-ttu-id="ed4a2-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ed4a2-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="ed4a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ed4a2-102">SYNOPSIS</span></span>
<span data-ttu-id="ed4a2-103">Avvia una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="ed4a2-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed4a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed4a2-104">SYNTAX</span></span>

### <span data-ttu-id="ed4a2-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ed4a2-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed4a2-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ed4a2-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed4a2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed4a2-107">DESCRIPTION</span></span>
<span data-ttu-id="ed4a2-108">Il cmdlet **Start-AzureRmVM** avvia una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="ed4a2-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="ed4a2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed4a2-109">EXAMPLES</span></span>

### <span data-ttu-id="ed4a2-110">Esempio 1: avviare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="ed4a2-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="ed4a2-111">Questo comando avvia la macchina virtuale denominata VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ed4a2-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="ed4a2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ed4a2-112">PARAMETERS</span></span>

### <span data-ttu-id="ed4a2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed4a2-113">-AsJob</span></span>
<span data-ttu-id="ed4a2-114">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="ed4a2-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ed4a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed4a2-115">-DefaultProfile</span></span>
<span data-ttu-id="ed4a2-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed4a2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed4a2-117">-ID</span><span class="sxs-lookup"><span data-stu-id="ed4a2-117">-Id</span></span>
<span data-ttu-id="ed4a2-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ed4a2-118">The resource group name.</span></span>

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

### <span data-ttu-id="ed4a2-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed4a2-119">-Name</span></span>
<span data-ttu-id="ed4a2-120">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ed4a2-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="ed4a2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed4a2-121">-ResourceGroupName</span></span>
<span data-ttu-id="ed4a2-122">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ed4a2-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ed4a2-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ed4a2-123">-Confirm</span></span>
<span data-ttu-id="ed4a2-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed4a2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed4a2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed4a2-125">-WhatIf</span></span>
<span data-ttu-id="ed4a2-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed4a2-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed4a2-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed4a2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed4a2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed4a2-128">CommonParameters</span></span>
<span data-ttu-id="ed4a2-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed4a2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed4a2-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed4a2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed4a2-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ed4a2-131">INPUTS</span></span>

### <span data-ttu-id="ed4a2-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ed4a2-132">None</span></span>
<span data-ttu-id="ed4a2-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="ed4a2-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ed4a2-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed4a2-134">OUTPUTS</span></span>

### <span data-ttu-id="ed4a2-135">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="ed4a2-135">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="ed4a2-136">Note</span><span class="sxs-lookup"><span data-stu-id="ed4a2-136">NOTES</span></span>

## <span data-ttu-id="ed4a2-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed4a2-137">RELATED LINKS</span></span>

[<span data-ttu-id="ed4a2-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ed4a2-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="ed4a2-139">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ed4a2-139">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="ed4a2-140">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ed4a2-140">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="ed4a2-141">Riavviare-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ed4a2-141">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="ed4a2-142">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ed4a2-142">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="ed4a2-143">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ed4a2-143">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


