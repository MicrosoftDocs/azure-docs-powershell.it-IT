---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
ms.openlocfilehash: 95a9e996612827b355b141165231651e17c78f6d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193301"
---
# <span data-ttu-id="82a43-101">New-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="82a43-101">New-AzSapMonitor</span></span>

## <span data-ttu-id="82a43-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="82a43-102">SYNOPSIS</span></span>
<span data-ttu-id="82a43-103">Crea un monitor SAP per l'abbonamento, il gruppo di risorse e il nome della risorsa specificati.</span><span class="sxs-lookup"><span data-stu-id="82a43-103">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="82a43-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82a43-104">SYNTAX</span></span>

```
New-AzSapMonitor -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-EnableCustomerAnalytic] [-LogAnalyticsWorkspaceId <String>] [-LogAnalyticsWorkspaceResourceId <String>]
 [-LogAnalyticsWorkspaceSharedKey <String>] [-MonitorSubnetResourceId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="82a43-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82a43-105">DESCRIPTION</span></span>
<span data-ttu-id="82a43-106">Crea un monitor SAP per l'abbonamento, il gruppo di risorse e il nome della risorsa specificati.</span><span class="sxs-lookup"><span data-stu-id="82a43-106">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="82a43-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82a43-107">EXAMPLES</span></span>

### <span data-ttu-id="82a43-108">Esempio 1: nuovo monitor SAP</span><span class="sxs-lookup"><span data-stu-id="82a43-108">Example 1: New SAP monitor</span></span> 
```powershell
PS C:\> $Workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName nancyc-hn1 -Name sapmonitor-test  -Location westus2 -Sku "Standard"
PS C:\> $WorkspaceKey = Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName nancyc-hn1 -Name sapmonitor-test
PS C:\> New-AzSapMonitor -Name ps-sapmonitor-t01 -ResourceGroupName nancyc-hn1 -Location westus2 -EnableCustomerAnalytic -MonitorSubnet "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.Network/virtualNetworks/vnet-sap/subnets/subnet-admin" -LogAnalyticsWorkspaceSharedKey $WorkspaceKey.PrimarySharedKey -LogAnalyticsWorkspaceId $Workspace.CustomerId -LogAnalyticsWorkspaceResourceId $Workspace.ResourceId

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="82a43-109">Questo comando crea un monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="82a43-109">This command creates a SAP monitor.</span></span>

## <span data-ttu-id="82a43-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="82a43-110">PARAMETERS</span></span>

### <span data-ttu-id="82a43-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82a43-111">-AsJob</span></span>
<span data-ttu-id="82a43-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="82a43-112">Run the command as a job</span></span>

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

### <span data-ttu-id="82a43-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82a43-113">-DefaultProfile</span></span>
<span data-ttu-id="82a43-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82a43-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82a43-115">-EnableCustomerAnalytic</span><span class="sxs-lookup"><span data-stu-id="82a43-115">-EnableCustomerAnalytic</span></span>
<span data-ttu-id="82a43-116">Valore che indica se inviare analisi a Microsoft</span><span class="sxs-lookup"><span data-stu-id="82a43-116">The value indicating whether to send analytics to Microsoft</span></span>

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

### <span data-ttu-id="82a43-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="82a43-117">-Location</span></span>
<span data-ttu-id="82a43-118">Posizione geografica in cui vive la risorsa</span><span class="sxs-lookup"><span data-stu-id="82a43-118">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="82a43-119">-LogAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="82a43-119">-LogAnalyticsWorkspaceId</span></span>
<span data-ttu-id="82a43-120">ID area di lavoro dell'area di lavoro analisi log da usare per il monitoraggio</span><span class="sxs-lookup"><span data-stu-id="82a43-120">The workspace ID of the log analytics workspace to be used for monitoring</span></span>

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

### <span data-ttu-id="82a43-121">-LogAnalyticsWorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="82a43-121">-LogAnalyticsWorkspaceResourceId</span></span>
<span data-ttu-id="82a43-122">ID ARM dell'area di lavoro analisi log usata per il monitoraggio</span><span class="sxs-lookup"><span data-stu-id="82a43-122">The ARM ID of the Log Analytics Workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="82a43-123">-LogAnalyticsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="82a43-123">-LogAnalyticsWorkspaceSharedKey</span></span>
<span data-ttu-id="82a43-124">Chiave condivisa dell'area di lavoro analisi log usata per il monitoraggio</span><span class="sxs-lookup"><span data-stu-id="82a43-124">The shared key of the log analytics workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="82a43-125">-MonitorSubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="82a43-125">-MonitorSubnetResourceId</span></span>
<span data-ttu-id="82a43-126">Subnet in cui verrà distribuito il monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="82a43-126">The subnet which the SAP monitor will be deployed in.</span></span>
<span data-ttu-id="82a43-127">Dovrebbe essere la stessa subnet del database HANA.</span><span class="sxs-lookup"><span data-stu-id="82a43-127">It should be the same subnet of HANA database.</span></span>

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

### <span data-ttu-id="82a43-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="82a43-128">-Name</span></span>
<span data-ttu-id="82a43-129">Nome della risorsa monitoraggio SAP.</span><span class="sxs-lookup"><span data-stu-id="82a43-129">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="82a43-130">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="82a43-130">-NoWait</span></span>
<span data-ttu-id="82a43-131">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="82a43-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="82a43-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82a43-132">-ResourceGroupName</span></span>
<span data-ttu-id="82a43-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="82a43-133">Name of the resource group.</span></span>

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

### <span data-ttu-id="82a43-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="82a43-134">-SubscriptionId</span></span>
<span data-ttu-id="82a43-135">ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="82a43-135">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="82a43-136">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="82a43-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="82a43-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="82a43-137">-Tag</span></span>
<span data-ttu-id="82a43-138">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="82a43-138">Resource tags.</span></span>

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

### <span data-ttu-id="82a43-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="82a43-139">-Confirm</span></span>
<span data-ttu-id="82a43-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82a43-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82a43-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82a43-141">-WhatIf</span></span>
<span data-ttu-id="82a43-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82a43-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82a43-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82a43-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82a43-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82a43-144">CommonParameters</span></span>
<span data-ttu-id="82a43-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82a43-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82a43-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82a43-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82a43-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="82a43-147">INPUTS</span></span>

## <span data-ttu-id="82a43-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82a43-148">OUTPUTS</span></span>

### <span data-ttu-id="82a43-149">Microsoft. Azure. PowerShell. Cmdlets. HanaOnAzure. Models. Api20200207Preview. ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="82a43-149">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="82a43-150">Note</span><span class="sxs-lookup"><span data-stu-id="82a43-150">NOTES</span></span>

<span data-ttu-id="82a43-151">ALIAS</span><span class="sxs-lookup"><span data-stu-id="82a43-151">ALIASES</span></span>

## <span data-ttu-id="82a43-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82a43-152">RELATED LINKS</span></span>

