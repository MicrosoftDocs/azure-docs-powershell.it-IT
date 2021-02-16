---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 144e67a2e58aeaa7fe7aa424ddc79bfca4aaa538
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180190"
---
# <span data-ttu-id="43e42-101">Get-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="43e42-101">Get-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="43e42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43e42-102">SYNOPSIS</span></span>
<span data-ttu-id="43e42-103">Ottiene le associazioni delle regole di raccolta dati.</span><span class="sxs-lookup"><span data-stu-id="43e42-103">Gets data collection rule association(s).</span></span>

## <span data-ttu-id="43e42-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43e42-104">SYNTAX</span></span>

### <span data-ttu-id="43e42-105">ByAssociatedResource (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="43e42-105">ByAssociatedResource (Default)</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -TargetResourceId <string> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="43e42-106">ByName</span><span class="sxs-lookup"><span data-stu-id="43e42-106">ByName</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -TargetResourceId <string> 
   -AssociationName <string> 
   [-DefaultProfile <IAzureContextContainer>] 
   [<CommonParameters>]
```

### <span data-ttu-id="43e42-107">ByRule</span><span class="sxs-lookup"><span data-stu-id="43e42-107">ByRule</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -ResourceGroupName <string> 
   -RuleName <string> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="43e42-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="43e42-108">ByInputObject</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -InputObject <PSDataCollectionRuleResource> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

## <span data-ttu-id="43e42-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="43e42-109">DESCRIPTION</span></span>
<span data-ttu-id="43e42-110">Il cmdlet **Get-AzDataCollectionRuleAssociation** ottiene una o più associazioni di regole di raccolta dati (DCRA).</span><span class="sxs-lookup"><span data-stu-id="43e42-110">The **Get-AzDataCollectionRuleAssociation** cmdlet gets one or more data collection rules associations (DCRA).</span></span>

<span data-ttu-id="43e42-111">Per applicare un DCR a una macchina virtuale, creare un'associazione per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="43e42-111">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="43e42-112">Una macchina virtuale può avere un'associazione a più controller di dominio e a una DCR possono essere associate più macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="43e42-112">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="43e42-113">In questo modo è possibile definire un set di controller di dominio, che corrispondono a uno specifico requisito, e applicarli solo alle macchine virtuali a cui sono applicabili.</span><span class="sxs-lookup"><span data-stu-id="43e42-113">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="43e42-114">Ecco l'articolo ["Configurare la raccolta di dati per l'agente di Monitoraggio di Azure"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) usando l'articolo DCRA.</span><span class="sxs-lookup"><span data-stu-id="43e42-114">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="43e42-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43e42-115">EXAMPLES</span></span>

### <span data-ttu-id="43e42-116">Esempio 1: Ottenere le associazioni delle regole di raccolta dati in base all'ID risorsa di destinazione (macchina virtuale associata)</span><span class="sxs-lookup"><span data-stu-id="43e42-116">Example 1: Get data collection rules associations by target resource ID (associated virtual machine)</span></span>
```
PS C:\>$vm = Get-AzVM -ResourceGroupName $rg -Name $vmName
PS C:\>Get-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="43e42-117">Questo comando elenca tutte le regole di raccolta dati per l'ID risorsa di destinazione (macchina virtuale) specificato.</span><span class="sxs-lookup"><span data-stu-id="43e42-117">This command lists all the data collection rules for the given target resource ID (virtual machine).</span></span>

### <span data-ttu-id="43e42-118">Esempio 2: Ottenere le associazioni delle regole di raccolta dati per regola (DCR)</span><span class="sxs-lookup"><span data-stu-id="43e42-118">Example 2: Get data collection rules associations by rule (DCR)</span></span>
```
PS C:\>Get-AzDataCollectionRuleAssociation -ResourceGroup $rg -RuleName $dcrName

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="43e42-119">Questo comando elenca le associazioni delle regole di raccolta dati per il gruppo di risorse e la regola specificata (DCR).</span><span class="sxs-lookup"><span data-stu-id="43e42-119">This command lists data collection rules associations for the given resource group and rule (DCR).</span></span>

### <span data-ttu-id="43e42-120">Esempio 3: Ottenere le associazioni delle regole di raccolta dati per l'oggetto di input (PSDataCollectionRuleResource)</span><span class="sxs-lookup"><span data-stu-id="43e42-120">Example 3: Get data collection rule associations by input object (PSDataCollectionRuleResource)</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName $rg -RuleName $dcrName
PS C:\>$dcr | Get-AzDataCollectionRuleAssociation

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="43e42-121">Questo comando elenca le associazioni delle regole di raccolta dati per l'oggetto di input specificato.</span><span class="sxs-lookup"><span data-stu-id="43e42-121">This command lists data collection rules associations for the given input object.</span></span>

### <span data-ttu-id="43e42-122">Esempio 4: Ottenere l'associazione di una regola di raccolta dati in base all'ID risorsa di destinazione (macchina virtuale associata) e al nome dell'associazione</span><span class="sxs-lookup"><span data-stu-id="43e42-122">Example 4: Get a data collection rule association by target resource ID (associated virtual machine) and association name</span></span>
```
PS C:\>Get-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id -AssociationName $assocName

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="43e42-123">Questo comando elenca un'associazione con una regola di raccolta dati (un elenco con un singolo elemento).</span><span class="sxs-lookup"><span data-stu-id="43e42-123">This command lists one (a list with a single element) data collection rule association.</span></span>

## <span data-ttu-id="43e42-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43e42-124">PARAMETERS</span></span>

### <span data-ttu-id="43e42-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43e42-125">-DefaultProfile</span></span>
<span data-ttu-id="43e42-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="43e42-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43e42-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="43e42-127">-TargetResourceId</span></span>
<span data-ttu-id="43e42-128">ID risorsa associato</span><span class="sxs-lookup"><span data-stu-id="43e42-128">The associated resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByAssociatedResource (Default)
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="43e42-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43e42-129">-ResourceGroupName</span></span>
<span data-ttu-id="43e42-130">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="43e42-130">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43e42-131">-RuleName</span><span class="sxs-lookup"><span data-stu-id="43e42-131">-RuleName</span></span>
<span data-ttu-id="43e42-132">Nome della regola per la raccolta dei dati</span><span class="sxs-lookup"><span data-stu-id="43e42-132">The data collection rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRule
Aliases: DataCollectionRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e42-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43e42-133">-InputObject</span></span>
<span data-ttu-id="43e42-134">Oggetto PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="43e42-134">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="43e42-135">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="43e42-135">-AssociationName</span></span>
<span data-ttu-id="43e42-136">Nome dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="43e42-136">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43e42-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43e42-137">CommonParameters</span></span>
<span data-ttu-id="43e42-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43e42-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43e42-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="43e42-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43e42-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="43e42-140">INPUTS</span></span>

### <span data-ttu-id="43e42-141">System.String</span><span class="sxs-lookup"><span data-stu-id="43e42-141">System.String</span></span>
### <span data-ttu-id="43e42-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="43e42-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="43e42-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43e42-143">OUTPUTS</span></span>

### <span data-ttu-id="43e42-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="43e42-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="43e42-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="43e42-145">NOTES</span></span>

## <span data-ttu-id="43e42-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43e42-146">RELATED LINKS</span></span>

<span data-ttu-id="43e42-147">[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md) 
 [New-AzDataCollectionRuleAssociation](./New-AzDataCollectionRuleAssociation.md)</span><span class="sxs-lookup"><span data-stu-id="43e42-147">[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md)
[New-AzDataCollectionRuleAssociation](./New-AzDataCollectionRuleAssociation.md)</span></span>
