---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: e1c5fad70147300bb08fdafb94fb81079a02ea00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512611"
---
# <span data-ttu-id="d23de-101">Set-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="d23de-101">Set-AzureRmDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="d23de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d23de-102">SYNOPSIS</span></span>
<span data-ttu-id="d23de-103">Imposta i criteri di dimensioni della macchina virtuale consentiti di un Lab in DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="d23de-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d23de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d23de-104">SYNTAX</span></span>

### <span data-ttu-id="d23de-105">Enable (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d23de-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d23de-106">Disabilitare</span><span class="sxs-lookup"><span data-stu-id="d23de-106">Disable</span></span>
```
Set-AzureRmDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d23de-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d23de-107">DESCRIPTION</span></span>
<span data-ttu-id="d23de-108">Il cmdlet **set-AzureRmDtlAllowedVMSizesPolicy** imposta i criteri per le dimensioni della macchina virtuale consentiti, che specifica un elenco delle dimensioni della macchina virtuale consentite in un Lab.</span><span class="sxs-lookup"><span data-stu-id="d23de-108">The **Set-AzureRmDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="d23de-109">Il cmdlet usa il gruppo di risorse specificato e il nome del Lab per impostare i criteri.</span><span class="sxs-lookup"><span data-stu-id="d23de-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="d23de-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d23de-110">EXAMPLES</span></span>

## <span data-ttu-id="d23de-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d23de-111">PARAMETERS</span></span>

### <span data-ttu-id="d23de-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d23de-112">-DefaultProfile</span></span>
<span data-ttu-id="d23de-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d23de-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d23de-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="d23de-114">-Disable</span></span>
<span data-ttu-id="d23de-115">Indica che questo cmdlet disabilita il criterio.</span><span class="sxs-lookup"><span data-stu-id="d23de-115">Indicates that this cmdlet disables the policy.</span></span>

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

### <span data-ttu-id="d23de-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="d23de-116">-Enable</span></span>
<span data-ttu-id="d23de-117">Indica che questo cmdlet Abilita i criteri.</span><span class="sxs-lookup"><span data-stu-id="d23de-117">Indicates that this cmdlet enables the policy.</span></span>

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

### <span data-ttu-id="d23de-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="d23de-118">-LabName</span></span>
<span data-ttu-id="d23de-119">Specifica il nome del Lab per il quale questo cmdlet imposta i criteri di dimensioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d23de-119">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

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

### <span data-ttu-id="d23de-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d23de-120">-ResourceGroupName</span></span>
<span data-ttu-id="d23de-121">Specifica il nome del gruppo di risorse a cui appartiene il Lab.</span><span class="sxs-lookup"><span data-stu-id="d23de-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="d23de-122">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="d23de-122">-VmSizes</span></span>
<span data-ttu-id="d23de-123">Specifica come matrice di stringhe l'elenco delle dimensioni della macchina virtuale consentite in Lab.</span><span class="sxs-lookup"><span data-stu-id="d23de-123">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d23de-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d23de-124">-Confirm</span></span>
<span data-ttu-id="d23de-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d23de-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d23de-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d23de-126">-WhatIf</span></span>
<span data-ttu-id="d23de-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d23de-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d23de-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d23de-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d23de-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d23de-129">CommonParameters</span></span>
<span data-ttu-id="d23de-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d23de-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d23de-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d23de-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d23de-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d23de-132">INPUTS</span></span>

### <span data-ttu-id="d23de-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d23de-133">None</span></span>
<span data-ttu-id="d23de-134">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d23de-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d23de-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d23de-135">OUTPUTS</span></span>

### <span data-ttu-id="d23de-136">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="d23de-136">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="d23de-137">Questo cmdlet restituisce i criteri che specificano l'elenco delle dimensioni della macchina virtuale consentite in Lab.</span><span class="sxs-lookup"><span data-stu-id="d23de-137">This cmdlet returns the policy that specifies the list of virtual machine sizes allowed in the lab.</span></span>

## <span data-ttu-id="d23de-138">Note</span><span class="sxs-lookup"><span data-stu-id="d23de-138">NOTES</span></span>

## <span data-ttu-id="d23de-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d23de-139">RELATED LINKS</span></span>

[<span data-ttu-id="d23de-140">Get-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="d23de-140">Get-AzureRmDtlAllowedVMSizesPolicy</span></span>](./Get-AzureRmDtlAllowedVMSizesPolicy.md)


