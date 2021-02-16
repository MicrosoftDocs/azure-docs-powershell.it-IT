---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: b174fdec51ece178b2e49a8e6e33d1e74f62c61f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402440"
---
# <span data-ttu-id="b3092-101">New-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="b3092-101">New-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="b3092-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3092-102">SYNOPSIS</span></span>
<span data-ttu-id="b3092-103">Creare l'associazione delle regole di raccolta dati.</span><span class="sxs-lookup"><span data-stu-id="b3092-103">Create data collection rule association.</span></span>

## <span data-ttu-id="b3092-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3092-104">SYNTAX</span></span>

### <span data-ttu-id="b3092-105">ByDataCollectionRuleId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b3092-105">ByDataCollectionRuleId (Default)</span></span>
```
New-AzDataCollectionRuleAssociation
   -TargetResourceId <string>
   -AssociationName <string>
   -RuleId <string>
   [-Description <string>]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="b3092-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b3092-106">ByInputObject</span></span>
```
New-AzDataCollectionRuleAssociation
   -TargetResourceId <string>
   -AssociationName <string>
   -InputObject <PSDataCollectionRuleResource>
   [-Description <string>]
   [-DefaultProfile <IAzureContextContainer>]  
   [-WhatIf]   
   [-Confirm]   
   [<CommonParameters>]
```


## <span data-ttu-id="b3092-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b3092-107">DESCRIPTION</span></span>
<span data-ttu-id="b3092-108">Il cmdlet **New-AzDataCollectionRuleAssociation** crea un'associazione DCRA (Data Collection Rules Association).</span><span class="sxs-lookup"><span data-stu-id="b3092-108">The **New-AzDataCollectionRuleAssociation** cmdlet creates a data collection rules association (DCRA).</span></span>

<span data-ttu-id="b3092-109">Per applicare un DCR a una macchina virtuale, creare un'associazione per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b3092-109">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="b3092-110">Una macchina virtuale può avere un'associazione a più controller di dominio e a una DCR possono essere associate più macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="b3092-110">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="b3092-111">In questo modo è possibile definire un set di controller di dominio, che corrispondono a uno specifico requisito, e applicarli solo alle macchine virtuali a cui sono applicabili.</span><span class="sxs-lookup"><span data-stu-id="b3092-111">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="b3092-112">Ecco "Configurare la [raccolta di dati per l'agente di Monitoraggio](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) di Azure" usando l'articolo DCRA.</span><span class="sxs-lookup"><span data-stu-id="b3092-112">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="b3092-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3092-113">EXAMPLES</span></span>

### <span data-ttu-id="b3092-114">Esempio 1: Creare un'associazione di regole di raccolta dati</span><span class="sxs-lookup"><span data-stu-id="b3092-114">Example 1: Create data collection rule association</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName $rg -RuleName $dcrName
PS C:\>$vmId = '/subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}'
PS C:\>New-AzDataCollectionRuleAssociation -TargetResourceId $vmId -AssociationName "dcrAssoc" -RuleId $dcr.Id

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Insights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/dcrAssoc
Name                 : dcrAssoc
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="b3092-115">Questo comando crea un'associazione tra regole di raccolta dati per una determinata regola e ID risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b3092-115">This command creates a data collection rule association for given rule and target resource ID.</span></span>

### <span data-ttu-id="b3092-116">Esempio 2: Creare l'associazione della regola di raccolta dati da un oggetto DCR</span><span class="sxs-lookup"><span data-stu-id="b3092-116">Example 2: Create data collection rule association from a DCR object</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName $rg -RuleName $dcrName
PS C:\>$vmId = '/subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}'
PS C:\>$dcr | New-AzDataCollectionRuleAssociation -TargetResourceId $vmId -AssociationName "dcrAssocInput"

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Insights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/dcrAssocInput
Name                 : dcrAssocInput
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="b3092-117">Questo comando crea un'associazione tra regole di raccolta dati per una determinata regola e ID risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b3092-117">This command creates a data collection rule association for given rule and target resource ID.</span></span>

## <span data-ttu-id="b3092-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3092-118">PARAMETERS</span></span>

### <span data-ttu-id="b3092-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3092-119">-DefaultProfile</span></span>
<span data-ttu-id="b3092-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b3092-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3092-121">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="b3092-121">-TargetResourceId</span></span>
<span data-ttu-id="b3092-122">ID della risorsa da associare</span><span class="sxs-lookup"><span data-stu-id="b3092-122">The resource ID to associate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3092-123">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="b3092-123">-AssociationName</span></span>
<span data-ttu-id="b3092-124">Nome della risorsa</span><span class="sxs-lookup"><span data-stu-id="b3092-124">The resource name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3092-125">-RuleId</span><span class="sxs-lookup"><span data-stu-id="b3092-125">-RuleId</span></span>
<span data-ttu-id="b3092-126">ID regola raccolta dati</span><span class="sxs-lookup"><span data-stu-id="b3092-126">The data collection rule ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByDataCollectionRuleId
Aliases: DataCollectionRuleId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3092-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3092-127">-InputObject</span></span>
<span data-ttu-id="b3092-128">Oggetto PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="b3092-128">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="b3092-129">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3092-129">-Description</span></span>
<span data-ttu-id="b3092-130">Descrizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="b3092-130">The resource description</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3092-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3092-131">-Confirm</span></span>
<span data-ttu-id="b3092-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3092-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3092-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3092-133">-WhatIf</span></span>
<span data-ttu-id="b3092-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3092-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3092-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3092-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3092-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3092-136">CommonParameters</span></span>
<span data-ttu-id="b3092-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3092-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3092-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b3092-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3092-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="b3092-139">INPUTS</span></span>

### <span data-ttu-id="b3092-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b3092-140">System.String</span></span>

## <span data-ttu-id="b3092-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3092-141">OUTPUTS</span></span>

### <span data-ttu-id="b3092-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="b3092-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="b3092-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="b3092-143">NOTES</span></span>

## <span data-ttu-id="b3092-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3092-144">RELATED LINKS</span></span>

<span data-ttu-id="b3092-145">[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md) 
 [Get-AzDataCollectionRuleAssociation](./Get-AzDataCollectionRuleAssociation.md)</span><span class="sxs-lookup"><span data-stu-id="b3092-145">[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md)
[Get-AzDataCollectionRuleAssociation](./Get-AzDataCollectionRuleAssociation.md)</span></span>
