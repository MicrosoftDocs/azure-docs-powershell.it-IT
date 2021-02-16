---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
ms.openlocfilehash: 95a9e996612827b355b141165231651e17c78f6d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203968"
---
# <span data-ttu-id="56858-101">New-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="56858-101">New-AzSapMonitor</span></span>

## <span data-ttu-id="56858-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56858-102">SYNOPSIS</span></span>
<span data-ttu-id="56858-103">Crea un monitor SAP per la sottoscrizione, il gruppo di risorse e il nome della risorsa specificati.</span><span class="sxs-lookup"><span data-stu-id="56858-103">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="56858-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56858-104">SYNTAX</span></span>

```
New-AzSapMonitor -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-EnableCustomerAnalytic] [-LogAnalyticsWorkspaceId <String>] [-LogAnalyticsWorkspaceResourceId <String>]
 [-LogAnalyticsWorkspaceSharedKey <String>] [-MonitorSubnetResourceId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="56858-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="56858-105">DESCRIPTION</span></span>
<span data-ttu-id="56858-106">Crea un monitor SAP per la sottoscrizione, il gruppo di risorse e il nome della risorsa specificati.</span><span class="sxs-lookup"><span data-stu-id="56858-106">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="56858-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56858-107">EXAMPLES</span></span>

### <span data-ttu-id="56858-108">Esempio 1: Nuovo monitor SAP</span><span class="sxs-lookup"><span data-stu-id="56858-108">Example 1: New SAP monitor</span></span> 
```powershell
PS C:\> $Workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName nancyc-hn1 -Name sapmonitor-test  -Location westus2 -Sku "Standard"
PS C:\> $WorkspaceKey = Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName nancyc-hn1 -Name sapmonitor-test
PS C:\> New-AzSapMonitor -Name ps-sapmonitor-t01 -ResourceGroupName nancyc-hn1 -Location westus2 -EnableCustomerAnalytic -MonitorSubnet "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.Network/virtualNetworks/vnet-sap/subnets/subnet-admin" -LogAnalyticsWorkspaceSharedKey $WorkspaceKey.PrimarySharedKey -LogAnalyticsWorkspaceId $Workspace.CustomerId -LogAnalyticsWorkspaceResourceId $Workspace.ResourceId

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="56858-109">Questo comando crea un monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="56858-109">This command creates a SAP monitor.</span></span>

## <span data-ttu-id="56858-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56858-110">PARAMETERS</span></span>

### <span data-ttu-id="56858-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56858-111">-AsJob</span></span>
<span data-ttu-id="56858-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="56858-112">Run the command as a job</span></span>

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

### <span data-ttu-id="56858-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56858-113">-DefaultProfile</span></span>
<span data-ttu-id="56858-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56858-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56858-115">-EnableCustomerAnalytic</span><span class="sxs-lookup"><span data-stu-id="56858-115">-EnableCustomerAnalytic</span></span>
<span data-ttu-id="56858-116">Valore che indica se inviare analisi a Microsoft</span><span class="sxs-lookup"><span data-stu-id="56858-116">The value indicating whether to send analytics to Microsoft</span></span>

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

### <span data-ttu-id="56858-117">-Location</span><span class="sxs-lookup"><span data-stu-id="56858-117">-Location</span></span>
<span data-ttu-id="56858-118">Posizione geografica in cui si trova la risorsa</span><span class="sxs-lookup"><span data-stu-id="56858-118">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56858-119">-LogAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="56858-119">-LogAnalyticsWorkspaceId</span></span>
<span data-ttu-id="56858-120">ID area di lavoro dell'area di lavoro analisi log da usare per il monitoraggio</span><span class="sxs-lookup"><span data-stu-id="56858-120">The workspace ID of the log analytics workspace to be used for monitoring</span></span>

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

### <span data-ttu-id="56858-121">-LogAnalyticsWorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="56858-121">-LogAnalyticsWorkspaceResourceId</span></span>
<span data-ttu-id="56858-122">ID ARM'area di lavoro Analisi log usata per il monitoraggio</span><span class="sxs-lookup"><span data-stu-id="56858-122">The ARM ID of the Log Analytics Workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="56858-123">-LogAnalyticsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="56858-123">-LogAnalyticsWorkspaceSharedKey</span></span>
<span data-ttu-id="56858-124">Chiave condivisa dell'area di lavoro analisi log usata per il monitoraggio</span><span class="sxs-lookup"><span data-stu-id="56858-124">The shared key of the log analytics workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="56858-125">-MonitorSubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="56858-125">-MonitorSubnetResourceId</span></span>
<span data-ttu-id="56858-126">Subnet in cui verrà distribuito il monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="56858-126">The subnet which the SAP monitor will be deployed in.</span></span>
<span data-ttu-id="56858-127">Dovrebbe essere la stessa subnet del database HANA.</span><span class="sxs-lookup"><span data-stu-id="56858-127">It should be the same subnet of HANA database.</span></span>

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

### <span data-ttu-id="56858-128">-Name</span><span class="sxs-lookup"><span data-stu-id="56858-128">-Name</span></span>
<span data-ttu-id="56858-129">Nome della risorsa monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="56858-129">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56858-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="56858-130">-NoWait</span></span>
<span data-ttu-id="56858-131">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="56858-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="56858-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56858-132">-ResourceGroupName</span></span>
<span data-ttu-id="56858-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="56858-133">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56858-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56858-134">-SubscriptionId</span></span>
<span data-ttu-id="56858-135">ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="56858-135">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="56858-136">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="56858-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56858-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="56858-137">-Tag</span></span>
<span data-ttu-id="56858-138">Tag di risorse.</span><span class="sxs-lookup"><span data-stu-id="56858-138">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56858-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56858-139">-Confirm</span></span>
<span data-ttu-id="56858-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56858-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56858-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56858-141">-WhatIf</span></span>
<span data-ttu-id="56858-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56858-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56858-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56858-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56858-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56858-144">CommonParameters</span></span>
<span data-ttu-id="56858-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56858-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56858-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="56858-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56858-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="56858-147">INPUTS</span></span>

## <span data-ttu-id="56858-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56858-148">OUTPUTS</span></span>

### <span data-ttu-id="56858-149">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="56858-149">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="56858-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="56858-150">NOTES</span></span>

<span data-ttu-id="56858-151">ALIAS</span><span class="sxs-lookup"><span data-stu-id="56858-151">ALIASES</span></span>

## <span data-ttu-id="56858-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56858-152">RELATED LINKS</span></span>

