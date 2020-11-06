---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: 459ae0e3d18056c6579d4fd6248548155e1471cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514347"
---
# <span data-ttu-id="8c20a-101">Set-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="8c20a-101">Set-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="8c20a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8c20a-102">SYNOPSIS</span></span>
<span data-ttu-id="8c20a-103">Imposta i criteri per gli utenti delle macchine virtuali di un Lab in DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="8c20a-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c20a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c20a-104">SYNTAX</span></span>

### <span data-ttu-id="8c20a-105">Enable (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8c20a-105">Enable (Default)</span></span>
```
Set-AzureRmDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c20a-106">Disabilitare</span><span class="sxs-lookup"><span data-stu-id="8c20a-106">Disable</span></span>
```
Set-AzureRmDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c20a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c20a-107">DESCRIPTION</span></span>
<span data-ttu-id="8c20a-108">Il cmdlet **set-AzureRmDtlVMsPerUserPolicy** imposta i criteri per gli utenti delle macchine virtuali di un Lab, che imposta il numero massimo di macchine virtuali consentite per ogni utente.</span><span class="sxs-lookup"><span data-stu-id="8c20a-108">The **Set-AzureRmDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="8c20a-109">Il cmdlet usa il gruppo di risorse specificato e il nome del Lab per impostare i criteri.</span><span class="sxs-lookup"><span data-stu-id="8c20a-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="8c20a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c20a-110">EXAMPLES</span></span>

## <span data-ttu-id="8c20a-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8c20a-111">PARAMETERS</span></span>

### <span data-ttu-id="8c20a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c20a-112">-DefaultProfile</span></span>
<span data-ttu-id="8c20a-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8c20a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c20a-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="8c20a-114">-Disable</span></span>
<span data-ttu-id="8c20a-115">Indica che questo cmdlet disabilita il criterio per il Lab.</span><span class="sxs-lookup"><span data-stu-id="8c20a-115">Indicates that this cmdlet disables the policy for the lab.</span></span>

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

### <span data-ttu-id="8c20a-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="8c20a-116">-Enable</span></span>
<span data-ttu-id="8c20a-117">Indica che questo cmdlet Abilita i criteri per Lab.</span><span class="sxs-lookup"><span data-stu-id="8c20a-117">Indicates that this cmdlet enables the policy for the lab.</span></span>

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

### <span data-ttu-id="8c20a-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="8c20a-118">-LabName</span></span>
<span data-ttu-id="8c20a-119">Specifica il nome del Lab per il quale questo cmdlet imposta le macchine virtuali per ogni criterio utente.</span><span class="sxs-lookup"><span data-stu-id="8c20a-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

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

### <span data-ttu-id="8c20a-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="8c20a-120">-MaxVMs</span></span>
<span data-ttu-id="8c20a-121">Specifica il numero massimo di macchine virtuali che possono essere create in Lab.</span><span class="sxs-lookup"><span data-stu-id="8c20a-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="8c20a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c20a-122">-ResourceGroupName</span></span>
<span data-ttu-id="8c20a-123">Specifica il nome del gruppo di risorse a cui appartiene il Lab.</span><span class="sxs-lookup"><span data-stu-id="8c20a-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="8c20a-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8c20a-124">-Confirm</span></span>
<span data-ttu-id="8c20a-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c20a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c20a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c20a-126">-WhatIf</span></span>
<span data-ttu-id="8c20a-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8c20a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c20a-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8c20a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c20a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c20a-129">CommonParameters</span></span>
<span data-ttu-id="8c20a-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c20a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c20a-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c20a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c20a-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8c20a-132">INPUTS</span></span>

### <span data-ttu-id="8c20a-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8c20a-133">None</span></span>
<span data-ttu-id="8c20a-134">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="8c20a-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8c20a-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c20a-135">OUTPUTS</span></span>

### <span data-ttu-id="8c20a-136">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="8c20a-136">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="8c20a-137">Questo cmdlet restituisce il criterio che specifica il numero massimo di macchine virtuali che possono essere create da un utente in laboratorio.</span><span class="sxs-lookup"><span data-stu-id="8c20a-137">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created by a user in the lab.</span></span>

## <span data-ttu-id="8c20a-138">Note</span><span class="sxs-lookup"><span data-stu-id="8c20a-138">NOTES</span></span>

## <span data-ttu-id="8c20a-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c20a-139">RELATED LINKS</span></span>

[<span data-ttu-id="8c20a-140">Get-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="8c20a-140">Get-AzureRmDtlVMsPerUserPolicy</span></span>](./Get-AzureRmDtlVMsPerUserPolicy.md)


