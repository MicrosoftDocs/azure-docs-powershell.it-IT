---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvm
schema: 2.0.0
ms.openlocfilehash: 7b9e6aa5a9879e0f7abb281810d80a6900198ca1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686207"
---
# <span data-ttu-id="7f41a-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7f41a-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="7f41a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f41a-102">SYNOPSIS</span></span>
<span data-ttu-id="7f41a-103">Avvia una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="7f41a-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f41a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f41a-104">SYNTAX</span></span>

### <span data-ttu-id="7f41a-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7f41a-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f41a-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="7f41a-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f41a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f41a-107">DESCRIPTION</span></span>
<span data-ttu-id="7f41a-108">Il cmdlet **Start-AzureRmVM** avvia una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="7f41a-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="7f41a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f41a-109">EXAMPLES</span></span>

### <span data-ttu-id="7f41a-110">Esempio 1: avviare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="7f41a-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="7f41a-111">Questo comando avvia la macchina virtuale denominata VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="7f41a-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="7f41a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f41a-112">PARAMETERS</span></span>

### <span data-ttu-id="7f41a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f41a-113">-AsJob</span></span>
<span data-ttu-id="7f41a-114">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="7f41a-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7f41a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f41a-115">-DefaultProfile</span></span>
<span data-ttu-id="7f41a-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7f41a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f41a-117">-ID</span><span class="sxs-lookup"><span data-stu-id="7f41a-117">-Id</span></span>
<span data-ttu-id="7f41a-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7f41a-118">The resource group name.</span></span>

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

### <span data-ttu-id="7f41a-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f41a-119">-Name</span></span>
<span data-ttu-id="7f41a-120">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f41a-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="7f41a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f41a-121">-ResourceGroupName</span></span>
<span data-ttu-id="7f41a-122">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f41a-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7f41a-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7f41a-123">-Confirm</span></span>
<span data-ttu-id="7f41a-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f41a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f41a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f41a-125">-WhatIf</span></span>
<span data-ttu-id="7f41a-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f41a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f41a-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f41a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f41a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f41a-128">CommonParameters</span></span>
<span data-ttu-id="7f41a-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f41a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f41a-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f41a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f41a-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f41a-131">INPUTS</span></span>

### <span data-ttu-id="7f41a-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7f41a-132">None</span></span>
<span data-ttu-id="7f41a-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="7f41a-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7f41a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f41a-134">OUTPUTS</span></span>

### <span data-ttu-id="7f41a-135">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="7f41a-135">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="7f41a-136">Note</span><span class="sxs-lookup"><span data-stu-id="7f41a-136">NOTES</span></span>

## <span data-ttu-id="7f41a-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f41a-137">RELATED LINKS</span></span>

[<span data-ttu-id="7f41a-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7f41a-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="7f41a-139">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7f41a-139">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="7f41a-140">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7f41a-140">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="7f41a-141">Riavviare-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7f41a-141">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="7f41a-142">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7f41a-142">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="7f41a-143">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7f41a-143">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


