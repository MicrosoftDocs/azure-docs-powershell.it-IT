---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: e343b9e16f793a760166736edcef6658bde34723
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861630"
---
# <span data-ttu-id="b9b55-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="b9b55-101">Start-AzVM</span></span>

## <span data-ttu-id="b9b55-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b9b55-102">SYNOPSIS</span></span>
<span data-ttu-id="b9b55-103">Avvia una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="b9b55-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="b9b55-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9b55-104">SYNTAX</span></span>

### <span data-ttu-id="b9b55-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b9b55-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9b55-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b9b55-106">IdParameterSetName</span></span>
```
Start-AzVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9b55-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9b55-107">DESCRIPTION</span></span>
<span data-ttu-id="b9b55-108">Il cmdlet **Start-AzVM** avvia una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="b9b55-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="b9b55-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9b55-109">EXAMPLES</span></span>

### <span data-ttu-id="b9b55-110">Esempio 1: avviare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="b9b55-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="b9b55-111">Questo comando avvia la macchina virtuale denominata VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b9b55-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="b9b55-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9b55-112">PARAMETERS</span></span>

### <span data-ttu-id="b9b55-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9b55-113">-AsJob</span></span>
<span data-ttu-id="b9b55-114">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="b9b55-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b9b55-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9b55-115">-DefaultProfile</span></span>
<span data-ttu-id="b9b55-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9b55-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9b55-117">-ID</span><span class="sxs-lookup"><span data-stu-id="b9b55-117">-Id</span></span>
<span data-ttu-id="b9b55-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b9b55-118">The resource group name.</span></span>

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

### <span data-ttu-id="b9b55-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9b55-119">-Name</span></span>
<span data-ttu-id="b9b55-120">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b9b55-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="b9b55-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9b55-121">-ResourceGroupName</span></span>
<span data-ttu-id="b9b55-122">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b9b55-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b9b55-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b9b55-123">-Confirm</span></span>
<span data-ttu-id="b9b55-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9b55-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9b55-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9b55-125">-WhatIf</span></span>
<span data-ttu-id="b9b55-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9b55-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b9b55-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9b55-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9b55-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9b55-128">CommonParameters</span></span>
<span data-ttu-id="b9b55-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9b55-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9b55-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9b55-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9b55-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b9b55-131">INPUTS</span></span>

### <span data-ttu-id="b9b55-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b9b55-132">None</span></span>
<span data-ttu-id="b9b55-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b9b55-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b9b55-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9b55-134">OUTPUTS</span></span>

### <span data-ttu-id="b9b55-135">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="b9b55-135">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="b9b55-136">Note</span><span class="sxs-lookup"><span data-stu-id="b9b55-136">NOTES</span></span>

## <span data-ttu-id="b9b55-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9b55-137">RELATED LINKS</span></span>

[<span data-ttu-id="b9b55-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="b9b55-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="b9b55-139">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="b9b55-139">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="b9b55-140">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="b9b55-140">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="b9b55-141">Riavviare-AzVM</span><span class="sxs-lookup"><span data-stu-id="b9b55-141">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="b9b55-142">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="b9b55-142">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="b9b55-143">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="b9b55-143">Update-AzVM</span></span>](./Update-AzVM.md)


