---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
ms.openlocfilehash: ad5d387a0935150a66924cbfdd19ac40ed57079c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327359"
---
# <span data-ttu-id="93d26-101">Start-AzVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="93d26-101">Start-AzVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="93d26-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="93d26-102">SYNOPSIS</span></span>
<span data-ttu-id="93d26-103">Avvia un aggiornamento a rotazione per trasferire tutte le istanze di set di scale della macchina virtuale alla versione più recente del sistema operativo per le immagini della piattaforma disponibile.</span><span class="sxs-lookup"><span data-stu-id="93d26-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

## <span data-ttu-id="93d26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93d26-104">SYNTAX</span></span>

```
Start-AzVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93d26-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93d26-105">DESCRIPTION</span></span>
<span data-ttu-id="93d26-106">Avvia un aggiornamento a rotazione per trasferire tutte le istanze di set di scale della macchina virtuale alla versione più recente del sistema operativo per le immagini della piattaforma disponibile.</span><span class="sxs-lookup"><span data-stu-id="93d26-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="93d26-107">Le istanze già in esecuzione della versione più recente del sistema operativo disponibile non sono interessate.</span><span class="sxs-lookup"><span data-stu-id="93d26-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="93d26-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93d26-108">EXAMPLES</span></span>

### <span data-ttu-id="93d26-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="93d26-109">Example 1</span></span>
```
PS C:\> Start-AzVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="93d26-110">Questo comando avvia un aggiornamento a rotazione di tutte le istanze VM della scala VM set "VMSS001" nel gruppo di risorse "Group001".</span><span class="sxs-lookup"><span data-stu-id="93d26-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="93d26-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="93d26-111">PARAMETERS</span></span>

### <span data-ttu-id="93d26-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93d26-112">-AsJob</span></span>
<span data-ttu-id="93d26-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="93d26-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="93d26-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93d26-114">-DefaultProfile</span></span>
<span data-ttu-id="93d26-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="93d26-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93d26-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93d26-116">-ResourceGroupName</span></span>
<span data-ttu-id="93d26-117">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="93d26-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="93d26-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="93d26-118">-VMScaleSetName</span></span>
<span data-ttu-id="93d26-119">Nome del set di scale VM.</span><span class="sxs-lookup"><span data-stu-id="93d26-119">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="93d26-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="93d26-120">-Confirm</span></span>
<span data-ttu-id="93d26-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93d26-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93d26-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93d26-122">-WhatIf</span></span>
<span data-ttu-id="93d26-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93d26-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93d26-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93d26-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93d26-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93d26-125">CommonParameters</span></span>
<span data-ttu-id="93d26-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93d26-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93d26-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93d26-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93d26-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="93d26-128">INPUTS</span></span>

### <span data-ttu-id="93d26-129">System. String</span><span class="sxs-lookup"><span data-stu-id="93d26-129">System.String</span></span>

## <span data-ttu-id="93d26-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93d26-130">OUTPUTS</span></span>

### <span data-ttu-id="93d26-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="93d26-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="93d26-132">Note</span><span class="sxs-lookup"><span data-stu-id="93d26-132">NOTES</span></span>

## <span data-ttu-id="93d26-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93d26-133">RELATED LINKS</span></span>
