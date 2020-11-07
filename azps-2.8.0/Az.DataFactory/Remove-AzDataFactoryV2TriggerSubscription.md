---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: c1e7fab8eb4e8afe22bdebc5930c8599c2dadceb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674943"
---
# <span data-ttu-id="8d52d-101">Remove-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="8d52d-101">Remove-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="8d52d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8d52d-102">SYNOPSIS</span></span>
<span data-ttu-id="8d52d-103">Annullare la sottoscrizione del trigger dell'evento agli eventi del servizio esterno.</span><span class="sxs-lookup"><span data-stu-id="8d52d-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="8d52d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8d52d-104">SYNTAX</span></span>

### <span data-ttu-id="8d52d-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8d52d-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-Name] <String> [-PassThru] [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d52d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8d52d-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d52d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8d52d-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-PassThru] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d52d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d52d-108">DESCRIPTION</span></span>
<span data-ttu-id="8d52d-109">Questo comando Annulla la sottoscrizione del trigger di evento agli eventi del servizio esterno specificati dal trigger definizione.</span><span class="sxs-lookup"><span data-stu-id="8d52d-109">This command unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="8d52d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8d52d-110">EXAMPLES</span></span>

### <span data-ttu-id="8d52d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8d52d-111">Example 1</span></span>
```
PS C:\> Remove-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1
```

<span data-ttu-id="8d52d-112">Questo comando consente di annullare l'abbonamento a BlobEnetTrigger1 trigger agli eventi specificati dal trigger definizione.</span><span class="sxs-lookup"><span data-stu-id="8d52d-112">This command will unsubscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="8d52d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8d52d-113">PARAMETERS</span></span>

### <span data-ttu-id="8d52d-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="8d52d-114">-DataFactoryName</span></span>
<span data-ttu-id="8d52d-115">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="8d52d-115">The data factory name.</span></span>

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

### <span data-ttu-id="8d52d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d52d-116">-DefaultProfile</span></span>
<span data-ttu-id="8d52d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8d52d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d52d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8d52d-118">-Force</span></span>
<span data-ttu-id="8d52d-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="8d52d-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="8d52d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d52d-120">-InputObject</span></span>
<span data-ttu-id="8d52d-121">Oggetto trigger.</span><span class="sxs-lookup"><span data-stu-id="8d52d-121">The trigger object.</span></span>

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

### <span data-ttu-id="8d52d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="8d52d-122">-Name</span></span>
<span data-ttu-id="8d52d-123">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="8d52d-123">The trigger name.</span></span>

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

### <span data-ttu-id="8d52d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d52d-124">-PassThru</span></span>
<span data-ttu-id="8d52d-125">Se specificato, cmdlet restituirà return true per l'eliminazione corretta.</span><span class="sxs-lookup"><span data-stu-id="8d52d-125">If specified, cmdlet will return return true on successful delete.</span></span>

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

### <span data-ttu-id="8d52d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d52d-126">-ResourceGroupName</span></span>
<span data-ttu-id="8d52d-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8d52d-127">The resource group name.</span></span>

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

### <span data-ttu-id="8d52d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d52d-128">-ResourceId</span></span>
<span data-ttu-id="8d52d-129">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="8d52d-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8d52d-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8d52d-130">-Confirm</span></span>
<span data-ttu-id="8d52d-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d52d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d52d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d52d-132">-WhatIf</span></span>
<span data-ttu-id="8d52d-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8d52d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d52d-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8d52d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d52d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d52d-135">CommonParameters</span></span>
<span data-ttu-id="8d52d-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d52d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d52d-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d52d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d52d-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8d52d-138">INPUTS</span></span>

### <span data-ttu-id="8d52d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8d52d-139">System.String</span></span>
<span data-ttu-id="8d52d-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="8d52d-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="8d52d-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8d52d-141">OUTPUTS</span></span>

### <span data-ttu-id="8d52d-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="8d52d-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="8d52d-143">Note</span><span class="sxs-lookup"><span data-stu-id="8d52d-143">NOTES</span></span>

## <span data-ttu-id="8d52d-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8d52d-144">RELATED LINKS</span></span>

