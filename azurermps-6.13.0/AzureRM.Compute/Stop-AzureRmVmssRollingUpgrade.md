---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Stop-AzureRmVmssRollingUpgrade.md
ms.openlocfilehash: 92a3a98ba5e6743b5d52ad619501fd6ed56c10c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511800"
---
# <span data-ttu-id="c0084-101">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="c0084-101">Stop-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="c0084-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c0084-102">SYNOPSIS</span></span>
<span data-ttu-id="c0084-103">Annulla l'aggiornamento a rotazione della scala della macchina virtuale corrente.</span><span class="sxs-lookup"><span data-stu-id="c0084-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0084-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0084-104">SYNTAX</span></span>

### <span data-ttu-id="c0084-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c0084-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0084-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="c0084-106">FriendMethod</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0084-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0084-107">DESCRIPTION</span></span>
<span data-ttu-id="c0084-108">Annulla l'aggiornamento a rotazione della scala della macchina virtuale corrente.</span><span class="sxs-lookup"><span data-stu-id="c0084-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="c0084-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0084-109">EXAMPLES</span></span>

### <span data-ttu-id="c0084-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c0084-110">Example 1</span></span>
```
PS C:\> Stop-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="c0084-111">Questo comando Annulla l'aggiornamento in corso del rollforward della scala VM imposta "VMSS001" nel gruppo di risorse "Group001".</span><span class="sxs-lookup"><span data-stu-id="c0084-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="c0084-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c0084-112">PARAMETERS</span></span>

### <span data-ttu-id="c0084-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0084-113">-AsJob</span></span>
<span data-ttu-id="c0084-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c0084-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0084-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0084-115">-DefaultProfile</span></span>
<span data-ttu-id="c0084-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c0084-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0084-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c0084-117">-Force</span></span>
<span data-ttu-id="c0084-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c0084-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c0084-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0084-119">-ResourceGroupName</span></span>
<span data-ttu-id="c0084-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c0084-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0084-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c0084-121">-VMScaleSetName</span></span>
<span data-ttu-id="c0084-122">Nome del set di scale VM.</span><span class="sxs-lookup"><span data-stu-id="c0084-122">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0084-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c0084-123">-Confirm</span></span>
<span data-ttu-id="c0084-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0084-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0084-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0084-125">-WhatIf</span></span>
<span data-ttu-id="c0084-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0084-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0084-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0084-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0084-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0084-128">CommonParameters</span></span>
<span data-ttu-id="c0084-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0084-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0084-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0084-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0084-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c0084-131">INPUTS</span></span>

### <span data-ttu-id="c0084-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c0084-132">System.String</span></span>

## <span data-ttu-id="c0084-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0084-133">OUTPUTS</span></span>

### <span data-ttu-id="c0084-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="c0084-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="c0084-135">Note</span><span class="sxs-lookup"><span data-stu-id="c0084-135">NOTES</span></span>

## <span data-ttu-id="c0084-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0084-136">RELATED LINKS</span></span>
