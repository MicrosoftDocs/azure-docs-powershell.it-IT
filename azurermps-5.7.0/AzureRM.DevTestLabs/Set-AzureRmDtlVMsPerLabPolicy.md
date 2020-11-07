---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: D2A7ECF6-E2B1-4BD5-BEA6-C9EC0C7377BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerLabPolicy.md
ms.openlocfilehash: 8e6e50fd22330073d647353232c549579aa382a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686525"
---
# <span data-ttu-id="a6c55-101">Set-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="a6c55-101">Set-AzureRmDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="a6c55-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a6c55-102">SYNOPSIS</span></span>
<span data-ttu-id="a6c55-103">Imposta i criteri delle macchine virtuali per Lab di un Lab in DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="a6c55-103">Sets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6c55-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6c55-104">SYNTAX</span></span>

### <span data-ttu-id="a6c55-105">Enable (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a6c55-105">Enable (Default)</span></span>
```
Set-AzureRmDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6c55-106">Disabilitare</span><span class="sxs-lookup"><span data-stu-id="a6c55-106">Disable</span></span>
```
Set-AzureRmDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6c55-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6c55-107">DESCRIPTION</span></span>
<span data-ttu-id="a6c55-108">Il cmdlet **set-AzureRmDtlVMsPerLabPolicy** imposta le macchine virtuali per i criteri Lab di un Lab, che imposta il numero totale di macchine virtuali consentite in un Lab.</span><span class="sxs-lookup"><span data-stu-id="a6c55-108">The **Set-AzureRmDtlVMsPerLabPolicy** cmdlet sets the virtual machines per lab policy of a lab, which sets the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="a6c55-109">Il cmdlet usa il gruppo di risorse specificato e il nome del Lab per impostare i criteri.</span><span class="sxs-lookup"><span data-stu-id="a6c55-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="a6c55-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6c55-110">EXAMPLES</span></span>

## <span data-ttu-id="a6c55-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a6c55-111">PARAMETERS</span></span>

### <span data-ttu-id="a6c55-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6c55-112">-DefaultProfile</span></span>
<span data-ttu-id="a6c55-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a6c55-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6c55-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="a6c55-114">-Disable</span></span>
<span data-ttu-id="a6c55-115">Indica che questo cmdlet Disabilita i criteri del Lab.</span><span class="sxs-lookup"><span data-stu-id="a6c55-115">Indicates that this cmdlet disables the policy of the lab.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disable
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c55-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="a6c55-116">-Enable</span></span>
<span data-ttu-id="a6c55-117">Indica che questo cmdlet Abilita i criteri del Lab.</span><span class="sxs-lookup"><span data-stu-id="a6c55-117">Indicates that this cmdlet enables the policy of the lab.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Enable
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c55-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="a6c55-118">-LabName</span></span>
<span data-ttu-id="a6c55-119">Specifica il nome del Lab per il quale questo cmdlet imposta le macchine virtuali per ogni criterio Lab.</span><span class="sxs-lookup"><span data-stu-id="a6c55-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per lab policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6c55-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="a6c55-120">-MaxVMs</span></span>
<span data-ttu-id="a6c55-121">Specifica il numero massimo di macchine virtuali che possono essere create in Lab.</span><span class="sxs-lookup"><span data-stu-id="a6c55-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c55-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6c55-122">-ResourceGroupName</span></span>
<span data-ttu-id="a6c55-123">Specifica il nome del gruppo di risorse a cui appartiene il Lab.</span><span class="sxs-lookup"><span data-stu-id="a6c55-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="a6c55-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a6c55-124">-Confirm</span></span>
<span data-ttu-id="a6c55-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6c55-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c55-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6c55-126">-WhatIf</span></span>
<span data-ttu-id="a6c55-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6c55-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6c55-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6c55-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c55-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6c55-129">CommonParameters</span></span>
<span data-ttu-id="a6c55-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6c55-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6c55-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6c55-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6c55-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a6c55-132">INPUTS</span></span>

### <span data-ttu-id="a6c55-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a6c55-133">None</span></span>
<span data-ttu-id="a6c55-134">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a6c55-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a6c55-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6c55-135">OUTPUTS</span></span>

### <span data-ttu-id="a6c55-136">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="a6c55-136">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="a6c55-137">Questo cmdlet restituisce il criterio che specifica il numero massimo di macchine virtuali che possono essere create in laboratorio.</span><span class="sxs-lookup"><span data-stu-id="a6c55-137">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created in the lab.</span></span>

## <span data-ttu-id="a6c55-138">Note</span><span class="sxs-lookup"><span data-stu-id="a6c55-138">NOTES</span></span>

## <span data-ttu-id="a6c55-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6c55-139">RELATED LINKS</span></span>

[<span data-ttu-id="a6c55-140">Get-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="a6c55-140">Get-AzureRmDtlVMsPerLabPolicy</span></span>](./Get-AzureRmDtlVMsPerLabPolicy.md)


