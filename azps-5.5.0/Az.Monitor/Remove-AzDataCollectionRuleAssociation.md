---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 798bb97b9e84121894341dd807bbaa9b3658a039
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203408"
---
# <span data-ttu-id="96a85-101">Remove-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="96a85-101">Remove-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="96a85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96a85-102">SYNOPSIS</span></span>
<span data-ttu-id="96a85-103">Eliminare l'associazione di una regola di raccolta dati.</span><span class="sxs-lookup"><span data-stu-id="96a85-103">Delete a data collection rule association.</span></span>

## <span data-ttu-id="96a85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96a85-104">SYNTAX</span></span>

### <span data-ttu-id="96a85-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="96a85-105">ByName (Default)</span></span>
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

### <span data-ttu-id="96a85-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="96a85-106">ByInputObject</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -InputObject <PSDataCollectionRuleAssociationProxyOnlyResource>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="96a85-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="96a85-107">ByResourceId</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -AssociationId <string>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

## <span data-ttu-id="96a85-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="96a85-108">DESCRIPTION</span></span>
<span data-ttu-id="96a85-109">Il cmdlet **Remove-AzDataCollectionRuleAssociation** elimina un'associazione di regole di raccolta dati (DCRA).</span><span class="sxs-lookup"><span data-stu-id="96a85-109">The **Remove-AzDataCollectionRuleAssociation** cmdlet delete a data collection rule association (DCRA).</span></span>

<span data-ttu-id="96a85-110">Per applicare un DCR a una macchina virtuale, creare un'associazione per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="96a85-110">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="96a85-111">Una macchina virtuale può avere un'associazione a più controller di dominio e a una DCR possono essere associate più macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="96a85-111">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="96a85-112">In questo modo è possibile definire un set di controller di dominio, che corrispondono a uno specifico requisito, e applicarli solo alle macchine virtuali a cui sono applicabili.</span><span class="sxs-lookup"><span data-stu-id="96a85-112">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="96a85-113">Ecco l'articolo ["Configurare la raccolta di dati per l'agente di Monitoraggio di Azure"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) usando l'articolo DCRA.</span><span class="sxs-lookup"><span data-stu-id="96a85-113">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="96a85-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96a85-114">EXAMPLES</span></span>

### <span data-ttu-id="96a85-115">Esempio 1: Eliminare l'associazione della regola di raccolta dati con i parametri nome e ID risorsa di destinazione (macchina virtuale associata)</span><span class="sxs-lookup"><span data-stu-id="96a85-115">Example 1: Delete data collection rule association with name and target resource ID (associated virtual machine) parameters</span></span>
```
PS C:\>Remove-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id -AssociationName $assocName
```

### <span data-ttu-id="96a85-116">Esempio 2: Eliminare una regola di raccolta dati con un oggetto di input</span><span class="sxs-lookup"><span data-stu-id="96a85-116">Example 2: Delete data collection rule with Input Object</span></span>
```
PS C:\>$dcrAssoc | Remove-AzDataCollectionRule
```

### <span data-ttu-id="96a85-117">Esempio 3: Eliminare una regola di raccolta dati con la proprietà ID risorsa di associazione</span><span class="sxs-lookup"><span data-stu-id="96a85-117">Example 3: Delete data collection rule with the association resource ID property</span></span>
```
PS C:\>Remove-AzDataCollectionRule -AssociationId $dcrAssoc.Id
```

## <span data-ttu-id="96a85-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96a85-118">PARAMETERS</span></span>

### <span data-ttu-id="96a85-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96a85-119">-DefaultProfile</span></span>
<span data-ttu-id="96a85-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="96a85-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96a85-121">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="96a85-121">-TargetResourceId</span></span>
<span data-ttu-id="96a85-122">ID risorsa associato.</span><span class="sxs-lookup"><span data-stu-id="96a85-122">The associated resource ID.</span></span>

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

### <span data-ttu-id="96a85-123">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="96a85-123">-AssociationName</span></span>
<span data-ttu-id="96a85-124">Nome della risorsa di associazione.</span><span class="sxs-lookup"><span data-stu-id="96a85-124">The name of the association resource.</span></span>

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

### <span data-ttu-id="96a85-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96a85-125">-InputObject</span></span>
<span data-ttu-id="96a85-126">Oggetto PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="96a85-126">PSDataCollectionRuleResource Object</span></span>

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

### <span data-ttu-id="96a85-127">-AssociationId</span><span class="sxs-lookup"><span data-stu-id="96a85-127">-AssociationId</span></span>
<span data-ttu-id="96a85-128">L'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="96a85-128">The resource identifier.</span></span>

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

### <span data-ttu-id="96a85-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96a85-129">-Confirm</span></span>
<span data-ttu-id="96a85-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96a85-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96a85-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96a85-131">-WhatIf</span></span>
<span data-ttu-id="96a85-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="96a85-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96a85-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="96a85-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96a85-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96a85-134">CommonParameters</span></span>
<span data-ttu-id="96a85-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96a85-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96a85-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="96a85-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96a85-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="96a85-137">INPUTS</span></span>

### <span data-ttu-id="96a85-138">System.String</span><span class="sxs-lookup"><span data-stu-id="96a85-138">System.String</span></span>
###<span data-ttu-id="96a85-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="96a85-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="96a85-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96a85-140">OUTPUTS</span></span>

### <span data-ttu-id="96a85-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="96a85-141">System.Boolean</span></span>

## <span data-ttu-id="96a85-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="96a85-142">NOTES</span></span>

## <span data-ttu-id="96a85-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96a85-143">RELATED LINKS</span></span>

<span data-ttu-id="96a85-144">[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="96a85-144">[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)</span></span>
