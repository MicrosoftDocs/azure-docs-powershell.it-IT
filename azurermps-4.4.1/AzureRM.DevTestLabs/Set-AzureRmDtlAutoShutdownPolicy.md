---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 8AAD9309-5763-4903-AF6A-1E50310146C0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoShutdownPolicy.md
ms.openlocfilehash: d812d66911c31297a2aaf4a32fd73562bc4ae9b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520102"
---
# <span data-ttu-id="5f224-101">Set-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="5f224-101">Set-AzureRmDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="5f224-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5f224-102">SYNOPSIS</span></span>
<span data-ttu-id="5f224-103">Imposta il criterio di arresto automatico di un Lab DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="5f224-103">Sets the auto shutdown policy of a lab DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f224-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f224-104">SYNTAX</span></span>

### <span data-ttu-id="5f224-105">Enable (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5f224-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5f224-106">Disabilitare</span><span class="sxs-lookup"><span data-stu-id="5f224-106">Disable</span></span>
```
Set-AzureRmDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f224-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f224-107">DESCRIPTION</span></span>
<span data-ttu-id="5f224-108">Il cmdlet **set-AzureRmDtlAutoShutdownPolicy** imposta i criteri di arresto automatico di un Lab, che arresta automaticamente tutte le macchine virtuali nel Lab in un determinato momento della giornata.</span><span class="sxs-lookup"><span data-stu-id="5f224-108">The **Set-AzureRmDtlAutoShutdownPolicy** cmdlet sets the auto shutdown policy of a lab, which automatically shuts down all the virtual machines in the lab at a specified time of the day.</span></span>
<span data-ttu-id="5f224-109">Il cmdlet usa il gruppo di risorse specificato e il nome del Lab per impostare i criteri.</span><span class="sxs-lookup"><span data-stu-id="5f224-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="5f224-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f224-110">EXAMPLES</span></span>

## <span data-ttu-id="5f224-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5f224-111">PARAMETERS</span></span>

### <span data-ttu-id="5f224-112">-Disable</span><span class="sxs-lookup"><span data-stu-id="5f224-112">-Disable</span></span>
<span data-ttu-id="5f224-113">Indica che il cmdlet disabilita il criterio in Lab.</span><span class="sxs-lookup"><span data-stu-id="5f224-113">Indicates that the cmdlet disables the policy in the lab.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f224-114">-Enable</span><span class="sxs-lookup"><span data-stu-id="5f224-114">-Enable</span></span>
<span data-ttu-id="5f224-115">Indica che il cmdlet Abilita i criteri in Lab.</span><span class="sxs-lookup"><span data-stu-id="5f224-115">Indicates that the cmdlet enables the policy in the lab.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f224-116">-LabName</span><span class="sxs-lookup"><span data-stu-id="5f224-116">-LabName</span></span>
<span data-ttu-id="5f224-117">Specifica il nome del Lab per il quale questo cmdlet imposta il criterio di arresto automatico.</span><span class="sxs-lookup"><span data-stu-id="5f224-117">Specifies the name of the lab for which this cmdlet sets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="5f224-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f224-118">-ResourceGroupName</span></span>
<span data-ttu-id="5f224-119">Specifica il nome del gruppo di risorse a cui appartiene il Lab.</span><span class="sxs-lookup"><span data-stu-id="5f224-119">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f224-120">-Ora</span><span class="sxs-lookup"><span data-stu-id="5f224-120">-Time</span></span>
<span data-ttu-id="5f224-121">Specifica il tempo, come oggetto **DateTime** , per il momento in cui le macchine virtuali in laboratorio devono essere arrestate.</span><span class="sxs-lookup"><span data-stu-id="5f224-121">Specifies the time, as a **DateTime** object, for when the virtual machines in the lab must shut down.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f224-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5f224-122">-Confirm</span></span>
<span data-ttu-id="5f224-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f224-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f224-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f224-124">-WhatIf</span></span>
<span data-ttu-id="5f224-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5f224-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f224-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5f224-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f224-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f224-127">-DefaultProfile</span></span>
<span data-ttu-id="5f224-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5f224-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f224-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f224-129">CommonParameters</span></span>
<span data-ttu-id="5f224-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f224-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f224-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f224-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f224-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5f224-132">INPUTS</span></span>

## <span data-ttu-id="5f224-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f224-133">OUTPUTS</span></span>

### <span data-ttu-id="5f224-134">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="5f224-134">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="5f224-135">Questo cmdlet restituisce la programmazione che specifica quando deve essere chiusa la macchina virtuale in laboratorio.</span><span class="sxs-lookup"><span data-stu-id="5f224-135">This cmdlet returns the schedule which specifies when the virtual machines in the lab must shut down.</span></span>

## <span data-ttu-id="5f224-136">Note</span><span class="sxs-lookup"><span data-stu-id="5f224-136">NOTES</span></span>

## <span data-ttu-id="5f224-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f224-137">RELATED LINKS</span></span>

[<span data-ttu-id="5f224-138">Get-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="5f224-138">Get-AzureRmDtlAutoShutdownPolicy</span></span>](./Get-AzureRmDtlAutoShutdownPolicy.md)


