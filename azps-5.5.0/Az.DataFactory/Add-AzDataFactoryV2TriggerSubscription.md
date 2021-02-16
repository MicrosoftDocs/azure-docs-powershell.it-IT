---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 6e38f98f9dd3ebfaa2ad4747016556aecd9998e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204475"
---
# <span data-ttu-id="5022c-101">Add-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="5022c-101">Add-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="5022c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5022c-102">SYNOPSIS</span></span>
<span data-ttu-id="5022c-103">Sottoscrivere il trigger di evento per eventi di servizi esterni.</span><span class="sxs-lookup"><span data-stu-id="5022c-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="5022c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5022c-104">SYNTAX</span></span>

### <span data-ttu-id="5022c-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="5022c-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5022c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5022c-106">ByInputObject</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5022c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5022c-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5022c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5022c-108">DESCRIPTION</span></span>
<span data-ttu-id="5022c-109">Questo comando sottoscrive il trigger di evento per gli eventi del servizio esterno specificati dall'affinamento del trigger.</span><span class="sxs-lookup"><span data-stu-id="5022c-109">This command subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="5022c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5022c-110">EXAMPLES</span></span>

### <span data-ttu-id="5022c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5022c-111">Example 1</span></span>
```
PS C:\> Add-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Provisioning
```

<span data-ttu-id="5022c-112">Questo comando sottoscrive il trigger BlobEnetTrigger1 per gli eventi specificati dall'affinamento del trigger.</span><span class="sxs-lookup"><span data-stu-id="5022c-112">This command will subscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="5022c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5022c-113">PARAMETERS</span></span>

### <span data-ttu-id="5022c-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5022c-114">-DataFactoryName</span></span>
<span data-ttu-id="5022c-115">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="5022c-115">The data factory name.</span></span>

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

### <span data-ttu-id="5022c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5022c-116">-DefaultProfile</span></span>
<span data-ttu-id="5022c-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5022c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5022c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5022c-118">-InputObject</span></span>
<span data-ttu-id="5022c-119">Oggetto trigger.</span><span class="sxs-lookup"><span data-stu-id="5022c-119">The trigger object.</span></span>

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

### <span data-ttu-id="5022c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5022c-120">-Name</span></span>
<span data-ttu-id="5022c-121">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="5022c-121">The trigger name.</span></span>

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

### <span data-ttu-id="5022c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5022c-122">-ResourceGroupName</span></span>
<span data-ttu-id="5022c-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5022c-123">The resource group name.</span></span>

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

### <span data-ttu-id="5022c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5022c-124">-ResourceId</span></span>
<span data-ttu-id="5022c-125">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="5022c-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5022c-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5022c-126">-Confirm</span></span>
<span data-ttu-id="5022c-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5022c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5022c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5022c-128">-WhatIf</span></span>
<span data-ttu-id="5022c-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5022c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5022c-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5022c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5022c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5022c-131">CommonParameters</span></span>
<span data-ttu-id="5022c-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5022c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5022c-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5022c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5022c-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="5022c-134">INPUTS</span></span>

### <span data-ttu-id="5022c-135">System.String</span><span class="sxs-lookup"><span data-stu-id="5022c-135">System.String</span></span>
<span data-ttu-id="5022c-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="5022c-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="5022c-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5022c-137">OUTPUTS</span></span>

### <span data-ttu-id="5022c-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="5022c-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="5022c-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="5022c-139">NOTES</span></span>

## <span data-ttu-id="5022c-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5022c-140">RELATED LINKS</span></span>

