---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: C06D4AD3-9CB1-4FEB-B02F-74022F264260
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/disable-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Disable-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Disable-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: c754b7e30fdec3a179beefdf48292a781ec083db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514115"
---
# <span data-ttu-id="b5ade-101">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b5ade-101">Disable-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="b5ade-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b5ade-102">SYNOPSIS</span></span>
<span data-ttu-id="b5ade-103">Disabilita una raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="b5ade-103">Disables a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5ade-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5ade-104">SYNTAX</span></span>

```
Disable-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5ade-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5ade-105">DESCRIPTION</span></span>
<span data-ttu-id="b5ade-106">Il cmdlet **Disable-AzureRmSchedulerJobCollection Disabilita** una raccolta processi in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="b5ade-106">The **Disable-AzureRmSchedulerJobCollection** cmdlet disables a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="b5ade-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5ade-107">EXAMPLES</span></span>

## <span data-ttu-id="b5ade-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b5ade-108">PARAMETERS</span></span>

### <span data-ttu-id="b5ade-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5ade-109">-DefaultProfile</span></span>
<span data-ttu-id="b5ade-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b5ade-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5ade-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="b5ade-111">-JobCollectionName</span></span>
<span data-ttu-id="b5ade-112">Specifica il nome di una raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="b5ade-112">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="b5ade-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5ade-113">-PassThru</span></span>
<span data-ttu-id="b5ade-114">Indica che questo cmdlet restituisce il valore Success per Success.</span><span class="sxs-lookup"><span data-stu-id="b5ade-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="b5ade-115">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="b5ade-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b5ade-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5ade-116">-ResourceGroupName</span></span>
<span data-ttu-id="b5ade-117">Specifica il gruppo di risorse della raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="b5ade-117">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="b5ade-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b5ade-118">-Confirm</span></span>
<span data-ttu-id="b5ade-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5ade-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5ade-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5ade-120">-WhatIf</span></span>
<span data-ttu-id="b5ade-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5ade-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5ade-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5ade-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5ade-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5ade-123">CommonParameters</span></span>
<span data-ttu-id="b5ade-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5ade-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5ade-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5ade-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5ade-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b5ade-126">INPUTS</span></span>

### <span data-ttu-id="b5ade-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b5ade-127">None</span></span>
<span data-ttu-id="b5ade-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b5ade-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b5ade-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5ade-129">OUTPUTS</span></span>

## <span data-ttu-id="b5ade-130">Note</span><span class="sxs-lookup"><span data-stu-id="b5ade-130">NOTES</span></span>

## <span data-ttu-id="b5ade-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5ade-131">RELATED LINKS</span></span>

[<span data-ttu-id="b5ade-132">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b5ade-132">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="b5ade-133">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b5ade-133">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="b5ade-134">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b5ade-134">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="b5ade-135">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b5ade-135">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="b5ade-136">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b5ade-136">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


