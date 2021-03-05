---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 87830eb9cb4321bf9af1476d3fa5a0db41796351
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987810"
---
# <span data-ttu-id="825ab-101">Remove-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="825ab-101">Remove-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="825ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="825ab-102">SYNOPSIS</span></span>
<span data-ttu-id="825ab-103">Eliminare l'associazione di una regola di raccolta dati.</span><span class="sxs-lookup"><span data-stu-id="825ab-103">Delete a data collection rule association.</span></span>

## <span data-ttu-id="825ab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="825ab-104">SYNTAX</span></span>

### <span data-ttu-id="825ab-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="825ab-105">ByName (Default)</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -TargetResourceId <string> 
      -AssociationName <string> 
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="825ab-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="825ab-106">ByInputObject</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -InputObject <PSDataCollectionRuleAssociationProxyOnlyResource>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="825ab-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="825ab-107">ByResourceId</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -AssociationId <string>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

## <span data-ttu-id="825ab-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="825ab-108">DESCRIPTION</span></span>
<span data-ttu-id="825ab-109">Il cmdlet **Remove-AzDataCollectionRuleAssociation** elimina un'associazione di regole di raccolta dati (DCRA).</span><span class="sxs-lookup"><span data-stu-id="825ab-109">The **Remove-AzDataCollectionRuleAssociation** cmdlet delete a data collection rule association (DCRA).</span></span>

<span data-ttu-id="825ab-110">Per applicare un DCR a una macchina virtuale, creare un'associazione per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="825ab-110">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="825ab-111">Una macchina virtuale può avere un'associazione a più controller di dominio e a una DCR possono essere associate più macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="825ab-111">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="825ab-112">In questo modo è possibile definire un set di controller di dominio, che corrispondono a uno specifico requisito, e applicarli solo alle macchine virtuali a cui sono applicabili.</span><span class="sxs-lookup"><span data-stu-id="825ab-112">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="825ab-113">Ecco "Configurare la [raccolta di dati per l'agente di Monitoraggio](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) di Azure" usando l'articolo DCRA.</span><span class="sxs-lookup"><span data-stu-id="825ab-113">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="825ab-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="825ab-114">EXAMPLES</span></span>

### <span data-ttu-id="825ab-115">Esempio 1: Eliminare l'associazione della regola di raccolta dati con i parametri nome e ID risorsa di destinazione (macchina virtuale associata)</span><span class="sxs-lookup"><span data-stu-id="825ab-115">Example 1: Delete data collection rule association with name and target resource ID (associated virtual machine) parameters</span></span>
```
PS C:\>Remove-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id -AssociationName $assocName
```

### <span data-ttu-id="825ab-116">Esempio 2: Eliminare una regola di raccolta dati con l'oggetto di input</span><span class="sxs-lookup"><span data-stu-id="825ab-116">Example 2: Delete data collection rule with Input Object</span></span>
```
PS C:\>$dcrAssoc | Remove-AzDataCollectionRule
```

### <span data-ttu-id="825ab-117">Esempio 3: Eliminare una regola di raccolta dati con la proprietà ID risorsa di associazione</span><span class="sxs-lookup"><span data-stu-id="825ab-117">Example 3: Delete data collection rule with the association resource ID property</span></span>
```
PS C:\>Remove-AzDataCollectionRule -AssociationId $dcrAssoc.Id
```

## <span data-ttu-id="825ab-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="825ab-118">PARAMETERS</span></span>

### <span data-ttu-id="825ab-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="825ab-119">-DefaultProfile</span></span>
<span data-ttu-id="825ab-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="825ab-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="825ab-121">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="825ab-121">-TargetResourceId</span></span>
<span data-ttu-id="825ab-122">ID risorsa associato.</span><span class="sxs-lookup"><span data-stu-id="825ab-122">The associated resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="825ab-123">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="825ab-123">-AssociationName</span></span>
<span data-ttu-id="825ab-124">Nome della risorsa di associazione.</span><span class="sxs-lookup"><span data-stu-id="825ab-124">The name of the association resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName (Default)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="825ab-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="825ab-125">-InputObject</span></span>
<span data-ttu-id="825ab-126">Oggetto PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="825ab-126">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="825ab-127">-AssociationId</span><span class="sxs-lookup"><span data-stu-id="825ab-127">-AssociationId</span></span>
<span data-ttu-id="825ab-128">L'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="825ab-128">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="825ab-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="825ab-129">-Confirm</span></span>
<span data-ttu-id="825ab-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="825ab-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="825ab-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="825ab-131">-WhatIf</span></span>
<span data-ttu-id="825ab-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="825ab-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="825ab-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="825ab-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="825ab-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="825ab-134">CommonParameters</span></span>
<span data-ttu-id="825ab-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="825ab-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="825ab-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="825ab-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="825ab-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="825ab-137">INPUTS</span></span>

### <span data-ttu-id="825ab-138">System.String</span><span class="sxs-lookup"><span data-stu-id="825ab-138">System.String</span></span>
###<span data-ttu-id="825ab-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="825ab-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="825ab-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="825ab-140">OUTPUTS</span></span>

### <span data-ttu-id="825ab-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="825ab-141">System.Boolean</span></span>

## <span data-ttu-id="825ab-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="825ab-142">NOTES</span></span>

## <span data-ttu-id="825ab-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="825ab-143">RELATED LINKS</span></span>

<span data-ttu-id="825ab-144">[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="825ab-144">[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)</span></span>
