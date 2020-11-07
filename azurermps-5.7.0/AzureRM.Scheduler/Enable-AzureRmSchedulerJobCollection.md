---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: BA79EDC8-BE89-4836-92EF-748D6F518886
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/enable-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Enable-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Enable-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 832b7659da0b71d804ddc1a8f19703b85fc8500b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687459"
---
# <span data-ttu-id="0ca73-101">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0ca73-101">Enable-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="0ca73-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0ca73-102">SYNOPSIS</span></span>
<span data-ttu-id="0ca73-103">Abilita una raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="0ca73-103">Enables a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ca73-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ca73-104">SYNTAX</span></span>

```
Enable-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ca73-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ca73-105">DESCRIPTION</span></span>
<span data-ttu-id="0ca73-106">Il cmdlet **Enable-AzureRmSchedulerJobCollection** Abilita una raccolta processi in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="0ca73-106">The **Enable-AzureRmSchedulerJobCollection** cmdlet enables a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="0ca73-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ca73-107">EXAMPLES</span></span>

## <span data-ttu-id="0ca73-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0ca73-108">PARAMETERS</span></span>

### <span data-ttu-id="0ca73-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ca73-109">-DefaultProfile</span></span>
<span data-ttu-id="0ca73-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0ca73-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ca73-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="0ca73-111">-JobCollectionName</span></span>
<span data-ttu-id="0ca73-112">Specifica il nome di una raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="0ca73-112">Specifies the name of a job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ca73-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ca73-113">-PassThru</span></span>
<span data-ttu-id="0ca73-114">Indica che questo cmdlet restituisce il valore Success per Success.</span><span class="sxs-lookup"><span data-stu-id="0ca73-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="0ca73-115">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="0ca73-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0ca73-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ca73-116">-ResourceGroupName</span></span>
<span data-ttu-id="0ca73-117">Specifica il gruppo di risorse della raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="0ca73-117">Specifies the resource group of the job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ca73-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0ca73-118">-Confirm</span></span>
<span data-ttu-id="0ca73-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ca73-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ca73-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ca73-120">-WhatIf</span></span>
<span data-ttu-id="0ca73-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ca73-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ca73-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ca73-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ca73-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ca73-123">CommonParameters</span></span>
<span data-ttu-id="0ca73-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ca73-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ca73-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ca73-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ca73-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0ca73-126">INPUTS</span></span>

### <span data-ttu-id="0ca73-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0ca73-127">None</span></span>
<span data-ttu-id="0ca73-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="0ca73-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0ca73-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ca73-129">OUTPUTS</span></span>

## <span data-ttu-id="0ca73-130">Note</span><span class="sxs-lookup"><span data-stu-id="0ca73-130">NOTES</span></span>

## <span data-ttu-id="0ca73-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ca73-131">RELATED LINKS</span></span>

[<span data-ttu-id="0ca73-132">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0ca73-132">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="0ca73-133">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0ca73-133">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="0ca73-134">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0ca73-134">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="0ca73-135">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0ca73-135">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="0ca73-136">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0ca73-136">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


