---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvmssrollingosupgrade
schema: 2.0.0
ms.openlocfilehash: 7f1cd0680d42ab83ec797b675e4505515a90548e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867133"
---
# <span data-ttu-id="3aaf3-101">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="3aaf3-101">Start-AzureRmVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="3aaf3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3aaf3-102">SYNOPSIS</span></span>
<span data-ttu-id="3aaf3-103">Avvia un aggiornamento a rotazione per trasferire tutte le istanze di set di scale della macchina virtuale alla versione più recente del sistema operativo per le immagini della piattaforma disponibile.</span><span class="sxs-lookup"><span data-stu-id="3aaf3-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3aaf3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3aaf3-104">SYNTAX</span></span>

```
Start-AzureRmVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3aaf3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3aaf3-105">DESCRIPTION</span></span>
<span data-ttu-id="3aaf3-106">Avvia un aggiornamento a rotazione per trasferire tutte le istanze di set di scale della macchina virtuale alla versione più recente del sistema operativo per le immagini della piattaforma disponibile.</span><span class="sxs-lookup"><span data-stu-id="3aaf3-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="3aaf3-107">Le istanze già in esecuzione della versione più recente del sistema operativo disponibile non sono interessate.</span><span class="sxs-lookup"><span data-stu-id="3aaf3-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="3aaf3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3aaf3-108">EXAMPLES</span></span>

### <span data-ttu-id="3aaf3-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3aaf3-109">Example 1</span></span>
```
PS C:\> Start-AzureRmVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="3aaf3-110">Questo comando avvia un aggiornamento a rotazione di tutte le istanze VM della scala VM set "VMSS001" nel gruppo di risorse "Group001".</span><span class="sxs-lookup"><span data-stu-id="3aaf3-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="3aaf3-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3aaf3-111">PARAMETERS</span></span>

### <span data-ttu-id="3aaf3-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3aaf3-112">-AsJob</span></span>
<span data-ttu-id="3aaf3-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3aaf3-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3aaf3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aaf3-114">-DefaultProfile</span></span>
<span data-ttu-id="3aaf3-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3aaf3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3aaf3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3aaf3-116">-ResourceGroupName</span></span>
<span data-ttu-id="3aaf3-117">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3aaf3-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="3aaf3-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3aaf3-118">-VMScaleSetName</span></span>
<span data-ttu-id="3aaf3-119">Nome del set di scale VM.</span><span class="sxs-lookup"><span data-stu-id="3aaf3-119">The name of the VM scale set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aaf3-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3aaf3-120">-Confirm</span></span>
<span data-ttu-id="3aaf3-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3aaf3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3aaf3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3aaf3-122">-WhatIf</span></span>
<span data-ttu-id="3aaf3-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3aaf3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3aaf3-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3aaf3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3aaf3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aaf3-125">CommonParameters</span></span>
<span data-ttu-id="3aaf3-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3aaf3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aaf3-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3aaf3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aaf3-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3aaf3-128">INPUTS</span></span>

### <span data-ttu-id="3aaf3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3aaf3-129">System.String</span></span>

## <span data-ttu-id="3aaf3-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3aaf3-130">OUTPUTS</span></span>

### <span data-ttu-id="3aaf3-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="3aaf3-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="3aaf3-132">Note</span><span class="sxs-lookup"><span data-stu-id="3aaf3-132">NOTES</span></span>

## <span data-ttu-id="3aaf3-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3aaf3-133">RELATED LINKS</span></span>

