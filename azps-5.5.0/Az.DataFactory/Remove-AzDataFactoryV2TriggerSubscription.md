---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 89fb4591af19db46aa536ebd15f3746cf6691244
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208707"
---
# <span data-ttu-id="b6377-101">Remove-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="b6377-101">Remove-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="b6377-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6377-102">SYNOPSIS</span></span>
<span data-ttu-id="b6377-103">Annullare la sottoscrizione del trigger di evento agli eventi del servizio esterno.</span><span class="sxs-lookup"><span data-stu-id="b6377-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="b6377-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6377-104">SYNTAX</span></span>

### <span data-ttu-id="b6377-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="b6377-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-Name] <String> [-PassThru] [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6377-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b6377-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6377-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b6377-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-PassThru] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6377-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b6377-108">DESCRIPTION</span></span>
<span data-ttu-id="b6377-109">Questo comando annulla la sottoscrizione del trigger di evento agli eventi del servizio esterno specificati dall'affinamento del trigger.</span><span class="sxs-lookup"><span data-stu-id="b6377-109">This command unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="b6377-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6377-110">EXAMPLES</span></span>

### <span data-ttu-id="b6377-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b6377-111">Example 1</span></span>
```
PS C:\> Remove-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1
```

<span data-ttu-id="b6377-112">Questo comando annulla la sottoscrizione del trigger BlobEnetTrigger1 agli eventi specificati dall'affinamento del trigger.</span><span class="sxs-lookup"><span data-stu-id="b6377-112">This command will unsubscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="b6377-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6377-113">PARAMETERS</span></span>

### <span data-ttu-id="b6377-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b6377-114">-DataFactoryName</span></span>
<span data-ttu-id="b6377-115">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="b6377-115">The data factory name.</span></span>

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

### <span data-ttu-id="b6377-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6377-116">-DefaultProfile</span></span>
<span data-ttu-id="b6377-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6377-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6377-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b6377-118">-Force</span></span>
<span data-ttu-id="b6377-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="b6377-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="b6377-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6377-120">-InputObject</span></span>
<span data-ttu-id="b6377-121">Oggetto trigger.</span><span class="sxs-lookup"><span data-stu-id="b6377-121">The trigger object.</span></span>

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

### <span data-ttu-id="b6377-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b6377-122">-Name</span></span>
<span data-ttu-id="b6377-123">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="b6377-123">The trigger name.</span></span>

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

### <span data-ttu-id="b6377-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6377-124">-PassThru</span></span>
<span data-ttu-id="b6377-125">Se specificato, il cmdlet restituirà true se l'eliminazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="b6377-125">If specified, cmdlet will return return true on successful delete.</span></span>

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

### <span data-ttu-id="b6377-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6377-126">-ResourceGroupName</span></span>
<span data-ttu-id="b6377-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b6377-127">The resource group name.</span></span>

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

### <span data-ttu-id="b6377-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6377-128">-ResourceId</span></span>
<span data-ttu-id="b6377-129">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="b6377-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b6377-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6377-130">-Confirm</span></span>
<span data-ttu-id="b6377-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6377-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6377-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6377-132">-WhatIf</span></span>
<span data-ttu-id="b6377-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6377-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6377-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6377-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6377-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6377-135">CommonParameters</span></span>
<span data-ttu-id="b6377-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6377-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6377-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6377-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6377-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="b6377-138">INPUTS</span></span>

### <span data-ttu-id="b6377-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b6377-139">System.String</span></span>
<span data-ttu-id="b6377-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="b6377-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="b6377-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6377-141">OUTPUTS</span></span>

### <span data-ttu-id="b6377-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="b6377-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="b6377-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="b6377-143">NOTES</span></span>

## <span data-ttu-id="b6377-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6377-144">RELATED LINKS</span></span>

