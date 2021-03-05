---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 1ab801c9eca278d5d117ddca881867371882980c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996811"
---
# <span data-ttu-id="12c75-101">Remove-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="12c75-101">Remove-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="12c75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12c75-102">SYNOPSIS</span></span>
<span data-ttu-id="12c75-103">Annullare la sottoscrizione del trigger di evento agli eventi del servizio esterno.</span><span class="sxs-lookup"><span data-stu-id="12c75-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="12c75-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12c75-104">SYNTAX</span></span>

### <span data-ttu-id="12c75-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="12c75-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-Name] <String> [-PassThru] [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="12c75-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="12c75-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12c75-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="12c75-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-PassThru] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12c75-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="12c75-108">DESCRIPTION</span></span>
<span data-ttu-id="12c75-109">Questo comando annulla la sottoscrizione del trigger di evento agli eventi del servizio esterno specificati dall'affinamento del trigger.</span><span class="sxs-lookup"><span data-stu-id="12c75-109">This command unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="12c75-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12c75-110">EXAMPLES</span></span>

### <span data-ttu-id="12c75-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="12c75-111">Example 1</span></span>
```
PS C:\> Remove-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1
```

<span data-ttu-id="12c75-112">Questo comando annulla la sottoscrizione del trigger BlobEnetTrigger1 agli eventi specificati dall'affinamento del trigger.</span><span class="sxs-lookup"><span data-stu-id="12c75-112">This command will unsubscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="12c75-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12c75-113">PARAMETERS</span></span>

### <span data-ttu-id="12c75-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="12c75-114">-DataFactoryName</span></span>
<span data-ttu-id="12c75-115">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="12c75-115">The data factory name.</span></span>

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

### <span data-ttu-id="12c75-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12c75-116">-DefaultProfile</span></span>
<span data-ttu-id="12c75-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12c75-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12c75-118">-Force</span><span class="sxs-lookup"><span data-stu-id="12c75-118">-Force</span></span>
<span data-ttu-id="12c75-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="12c75-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="12c75-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12c75-120">-InputObject</span></span>
<span data-ttu-id="12c75-121">Oggetto trigger.</span><span class="sxs-lookup"><span data-stu-id="12c75-121">The trigger object.</span></span>

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

### <span data-ttu-id="12c75-122">-Name</span><span class="sxs-lookup"><span data-stu-id="12c75-122">-Name</span></span>
<span data-ttu-id="12c75-123">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="12c75-123">The trigger name.</span></span>

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

### <span data-ttu-id="12c75-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12c75-124">-PassThru</span></span>
<span data-ttu-id="12c75-125">Se specificato, il cmdlet restituirà true se l'eliminazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="12c75-125">If specified, cmdlet will return return true on successful delete.</span></span>

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

### <span data-ttu-id="12c75-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12c75-126">-ResourceGroupName</span></span>
<span data-ttu-id="12c75-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="12c75-127">The resource group name.</span></span>

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

### <span data-ttu-id="12c75-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12c75-128">-ResourceId</span></span>
<span data-ttu-id="12c75-129">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="12c75-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="12c75-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12c75-130">-Confirm</span></span>
<span data-ttu-id="12c75-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12c75-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12c75-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12c75-132">-WhatIf</span></span>
<span data-ttu-id="12c75-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12c75-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12c75-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12c75-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12c75-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12c75-135">CommonParameters</span></span>
<span data-ttu-id="12c75-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12c75-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12c75-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12c75-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12c75-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="12c75-138">INPUTS</span></span>

### <span data-ttu-id="12c75-139">System.String</span><span class="sxs-lookup"><span data-stu-id="12c75-139">System.String</span></span>
<span data-ttu-id="12c75-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="12c75-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="12c75-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12c75-141">OUTPUTS</span></span>

### <span data-ttu-id="12c75-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="12c75-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="12c75-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="12c75-143">NOTES</span></span>

## <span data-ttu-id="12c75-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12c75-144">RELATED LINKS</span></span>

