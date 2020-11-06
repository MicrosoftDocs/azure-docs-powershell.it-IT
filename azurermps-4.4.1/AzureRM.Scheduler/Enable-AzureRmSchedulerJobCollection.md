---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: BA79EDC8-BE89-4836-92EF-748D6F518886
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Enable-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Enable-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 16b86028dafa2f9fa35422b4346cd11496194bfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516060"
---
# <span data-ttu-id="34e65-101">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="34e65-101">Enable-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="34e65-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34e65-102">SYNOPSIS</span></span>
<span data-ttu-id="34e65-103">Abilita una raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="34e65-103">Enables a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34e65-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34e65-104">SYNTAX</span></span>

```
Enable-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34e65-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34e65-105">DESCRIPTION</span></span>
<span data-ttu-id="34e65-106">Il cmdlet **Enable-AzureRmSchedulerJobCollection** Abilita una raccolta processi in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="34e65-106">The **Enable-AzureRmSchedulerJobCollection** cmdlet enables a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="34e65-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34e65-107">EXAMPLES</span></span>

## <span data-ttu-id="34e65-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34e65-108">PARAMETERS</span></span>

### <span data-ttu-id="34e65-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="34e65-109">-JobCollectionName</span></span>
<span data-ttu-id="34e65-110">Specifica il nome di una raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="34e65-110">Specifies the name of a job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34e65-111">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34e65-111">-PassThru</span></span>
<span data-ttu-id="34e65-112">Indica che questo cmdlet restituisce il valore Success per Success.</span><span class="sxs-lookup"><span data-stu-id="34e65-112">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="34e65-113">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="34e65-113">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="34e65-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34e65-114">-ResourceGroupName</span></span>
<span data-ttu-id="34e65-115">Specifica il gruppo di risorse della raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="34e65-115">Specifies the resource group of the job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34e65-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="34e65-116">-Confirm</span></span>
<span data-ttu-id="34e65-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34e65-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34e65-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34e65-118">-WhatIf</span></span>
<span data-ttu-id="34e65-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34e65-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34e65-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34e65-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34e65-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34e65-121">-DefaultProfile</span></span>
<span data-ttu-id="34e65-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34e65-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34e65-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34e65-123">CommonParameters</span></span>
<span data-ttu-id="34e65-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34e65-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34e65-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34e65-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34e65-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34e65-126">INPUTS</span></span>

## <span data-ttu-id="34e65-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34e65-127">OUTPUTS</span></span>

## <span data-ttu-id="34e65-128">Note</span><span class="sxs-lookup"><span data-stu-id="34e65-128">NOTES</span></span>

## <span data-ttu-id="34e65-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34e65-129">RELATED LINKS</span></span>

[<span data-ttu-id="34e65-130">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="34e65-130">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="34e65-131">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="34e65-131">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="34e65-132">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="34e65-132">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="34e65-133">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="34e65-133">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="34e65-134">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="34e65-134">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


