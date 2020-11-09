---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 6e38f98f9dd3ebfaa2ad4747016556aecd9998e9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298638"
---
# <span data-ttu-id="84d4d-101">Add-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="84d4d-101">Add-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="84d4d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84d4d-102">SYNOPSIS</span></span>
<span data-ttu-id="84d4d-103">Sottoscrivere il trigger dell'evento per gli eventi del servizio esterno.</span><span class="sxs-lookup"><span data-stu-id="84d4d-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="84d4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84d4d-104">SYNTAX</span></span>

### <span data-ttu-id="84d4d-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="84d4d-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84d4d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="84d4d-106">ByInputObject</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84d4d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="84d4d-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84d4d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84d4d-108">DESCRIPTION</span></span>
<span data-ttu-id="84d4d-109">Questo comando sottoscrive il trigger dell'evento agli eventi del servizio esterno specificati dal trigger definizione.</span><span class="sxs-lookup"><span data-stu-id="84d4d-109">This command subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="84d4d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84d4d-110">EXAMPLES</span></span>

### <span data-ttu-id="84d4d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="84d4d-111">Example 1</span></span>
```
PS C:\> Add-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Provisioning
```

<span data-ttu-id="84d4d-112">Questo comando sottoscriverà il trigger BlobEnetTrigger1 agli eventi specificati dal trigger definizione.</span><span class="sxs-lookup"><span data-stu-id="84d4d-112">This command will subscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="84d4d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84d4d-113">PARAMETERS</span></span>

### <span data-ttu-id="84d4d-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="84d4d-114">-DataFactoryName</span></span>
<span data-ttu-id="84d4d-115">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="84d4d-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84d4d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84d4d-116">-DefaultProfile</span></span>
<span data-ttu-id="84d4d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84d4d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84d4d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84d4d-118">-InputObject</span></span>
<span data-ttu-id="84d4d-119">Oggetto trigger.</span><span class="sxs-lookup"><span data-stu-id="84d4d-119">The trigger object.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84d4d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="84d4d-120">-Name</span></span>
<span data-ttu-id="84d4d-121">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="84d4d-121">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84d4d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84d4d-122">-ResourceGroupName</span></span>
<span data-ttu-id="84d4d-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="84d4d-123">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84d4d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84d4d-124">-ResourceId</span></span>
<span data-ttu-id="84d4d-125">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="84d4d-125">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84d4d-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="84d4d-126">-Confirm</span></span>
<span data-ttu-id="84d4d-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84d4d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84d4d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84d4d-128">-WhatIf</span></span>
<span data-ttu-id="84d4d-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84d4d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84d4d-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84d4d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84d4d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84d4d-131">CommonParameters</span></span>
<span data-ttu-id="84d4d-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84d4d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84d4d-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84d4d-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84d4d-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84d4d-134">INPUTS</span></span>

### <span data-ttu-id="84d4d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="84d4d-135">System.String</span></span>
<span data-ttu-id="84d4d-136">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="84d4d-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="84d4d-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84d4d-137">OUTPUTS</span></span>

### <span data-ttu-id="84d4d-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="84d4d-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="84d4d-139">Note</span><span class="sxs-lookup"><span data-stu-id="84d4d-139">NOTES</span></span>

## <span data-ttu-id="84d4d-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84d4d-140">RELATED LINKS</span></span>

