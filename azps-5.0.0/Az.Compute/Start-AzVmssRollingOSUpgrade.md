---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
ms.openlocfilehash: ad5d387a0935150a66924cbfdd19ac40ed57079c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200235"
---
# <span data-ttu-id="a56b6-101">Start-AzVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="a56b6-101">Start-AzVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="a56b6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a56b6-102">SYNOPSIS</span></span>
<span data-ttu-id="a56b6-103">Avvia un aggiornamento a rotazione per trasferire tutte le istanze di set di scale della macchina virtuale alla versione più recente del sistema operativo per le immagini della piattaforma disponibile.</span><span class="sxs-lookup"><span data-stu-id="a56b6-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

## <span data-ttu-id="a56b6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a56b6-104">SYNTAX</span></span>

```
Start-AzVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a56b6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a56b6-105">DESCRIPTION</span></span>
<span data-ttu-id="a56b6-106">Avvia un aggiornamento a rotazione per trasferire tutte le istanze di set di scale della macchina virtuale alla versione più recente del sistema operativo per le immagini della piattaforma disponibile.</span><span class="sxs-lookup"><span data-stu-id="a56b6-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="a56b6-107">Le istanze già in esecuzione della versione più recente del sistema operativo disponibile non sono interessate.</span><span class="sxs-lookup"><span data-stu-id="a56b6-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="a56b6-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a56b6-108">EXAMPLES</span></span>

### <span data-ttu-id="a56b6-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a56b6-109">Example 1</span></span>
```
PS C:\> Start-AzVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="a56b6-110">Questo comando avvia un aggiornamento a rotazione di tutte le istanze VM della scala VM set "VMSS001" nel gruppo di risorse "Group001".</span><span class="sxs-lookup"><span data-stu-id="a56b6-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="a56b6-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a56b6-111">PARAMETERS</span></span>

### <span data-ttu-id="a56b6-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a56b6-112">-AsJob</span></span>
<span data-ttu-id="a56b6-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a56b6-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a56b6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a56b6-114">-DefaultProfile</span></span>
<span data-ttu-id="a56b6-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a56b6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a56b6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a56b6-116">-ResourceGroupName</span></span>
<span data-ttu-id="a56b6-117">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a56b6-117">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a56b6-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a56b6-118">-VMScaleSetName</span></span>
<span data-ttu-id="a56b6-119">Nome del set di scale VM.</span><span class="sxs-lookup"><span data-stu-id="a56b6-119">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a56b6-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a56b6-120">-Confirm</span></span>
<span data-ttu-id="a56b6-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a56b6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a56b6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a56b6-122">-WhatIf</span></span>
<span data-ttu-id="a56b6-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a56b6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a56b6-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a56b6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a56b6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a56b6-125">CommonParameters</span></span>
<span data-ttu-id="a56b6-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a56b6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a56b6-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a56b6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a56b6-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a56b6-128">INPUTS</span></span>

### <span data-ttu-id="a56b6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a56b6-129">System.String</span></span>

## <span data-ttu-id="a56b6-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a56b6-130">OUTPUTS</span></span>

### <span data-ttu-id="a56b6-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a56b6-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a56b6-132">Note</span><span class="sxs-lookup"><span data-stu-id="a56b6-132">NOTES</span></span>

## <span data-ttu-id="a56b6-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a56b6-133">RELATED LINKS</span></span>