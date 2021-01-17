---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
ms.openlocfilehash: 315a44b986317157a0ada22955c04ea01726327a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486192"
---
# <span data-ttu-id="6d583-101">New-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="6d583-101">New-AzSentinelDataConnector</span></span>

## <span data-ttu-id="6d583-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6d583-102">SYNOPSIS</span></span>
<span data-ttu-id="6d583-103">Creare un connettore dati.</span><span class="sxs-lookup"><span data-stu-id="6d583-103">Create a Data Connector.</span></span>

## <span data-ttu-id="6d583-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d583-104">SYNTAX</span></span>

### <span data-ttu-id="6d583-105">AzureActiveDirectory (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6d583-105">AzureActiveDirectory (Default)</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureActiveDirectory] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6d583-106">AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="6d583-106">AzureAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d583-107">AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="6d583-107">AzureSecurityCenter</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureSecurityCenter] -Alerts <String> -SubscriptionId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d583-108">AmazonWebServicesCloudTrail</span><span class="sxs-lookup"><span data-stu-id="6d583-108">AmazonWebServicesCloudTrail</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AmazonWebServicesCloudTrail] -AwsRoleArn <String> -Logs <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d583-109">MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="6d583-109">MicrosoftCloudAppSecurity</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftCloudAppSecurity] -Alerts <String> -DiscoveryLogs <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d583-110">MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="6d583-110">MicrosoftDefenderAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftDefenderAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d583-111">Office365</span><span class="sxs-lookup"><span data-stu-id="6d583-111">Office365</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-Office365] -Exchange <String> -SharePoint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d583-112">ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="6d583-112">ThreatIntelligence</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-ThreatIntelligence] -Indicators <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d583-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d583-113">DESCRIPTION</span></span>
<span data-ttu-id="6d583-114">Il cmdlet **New-AzSentinelAlertRule** crea una regola analitica (avviso) nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="6d583-114">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="6d583-115">È necessario specificare uno dei parametri, ad esempio-AzureActiveDirectory, per specificare il tipo di regola di avviso da creare.</span><span class="sxs-lookup"><span data-stu-id="6d583-115">You must specify one of the parameters, for example -AzureActiveDirectory, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="6d583-116">Ogni tipo ha diversi parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="6d583-116">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="6d583-117">Puoi usare il parametro *Confirm* e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="6d583-117">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="6d583-118">Nota: non tutti i connettori dati disponibili nel portale sono avaialble tramite API.</span><span class="sxs-lookup"><span data-stu-id="6d583-118">Note:  Not all data connectors available in the portal are avaialble via API.</span></span>

## <span data-ttu-id="6d583-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d583-119">EXAMPLES</span></span>

### <span data-ttu-id="6d583-120">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6d583-120">Example 1</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AzureSecurityCenter -Alerts Enabled -SubscriptionId ((Get-AzContext).Subscription.Id)
```

<span data-ttu-id="6d583-121">Questo esempio crea un **DataConnector** per Azure Security Center nell'area di lavoro specificata e lo archivia nella variabile $DataConnector.</span><span class="sxs-lookup"><span data-stu-id="6d583-121">This example creates a **DataConnector** for Azure Security Center in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

### <span data-ttu-id="6d583-122">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6d583-122">Example 2</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftCloudAppSecurity -Alerts Enabled -DiscoveryLogs Disabled
```

<span data-ttu-id="6d583-123">Questo esempio crea un **DataConnector** per la sicurezza dell'app cloud Microsoft nell'area di lavoro specificata e lo archivia nella variabile $DataConnector.</span><span class="sxs-lookup"><span data-stu-id="6d583-123">This example creates a **DataConnector** for Microsoft Cloud App Security in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="6d583-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6d583-124">PARAMETERS</span></span>

### <span data-ttu-id="6d583-125">-Avvisi</span><span class="sxs-lookup"><span data-stu-id="6d583-125">-Alerts</span></span>
<span data-ttu-id="6d583-126">Avvisi del connettore dati</span><span class="sxs-lookup"><span data-stu-id="6d583-126">Data Connector Alerts</span></span>

```yaml
Type: System.String
Parameter Sets: AzureActiveDirectory, AzureAdvancedThreatProtection, AzureSecurityCenter, MicrosoftCloudAppSecurity, MicrosoftDefenderAdvancedThreatProtection
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d583-127">-AmazonWebServicesCloudTrail</span><span class="sxs-lookup"><span data-stu-id="6d583-127">-AmazonWebServicesCloudTrail</span></span>
<span data-ttu-id="6d583-128">Data Connector Amazon Web Services cloud Trail</span><span class="sxs-lookup"><span data-stu-id="6d583-128">Data Connector Amazon Web Services Cloud Trail</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d583-129">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="6d583-129">-AwsRoleArn</span></span>
<span data-ttu-id="6d583-130">Data Connector AWS ruolo ARN</span><span class="sxs-lookup"><span data-stu-id="6d583-130">Data Connector AWS Role Arn</span></span>

```yaml
Type: System.String
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d583-131">-AzureActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="6d583-131">-AzureActiveDirectory</span></span>
<span data-ttu-id="6d583-132">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="6d583-132">Data Connector Azure Active Directory</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureActiveDirectory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d583-133">-AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="6d583-133">-AzureAdvancedThreatProtection</span></span>
<span data-ttu-id="6d583-134">Data Connector Azure Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="6d583-134">Data Connector Azure Advanced Threat Protection</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureAdvancedThreatProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d583-135">-AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="6d583-135">-AzureSecurityCenter</span></span>
<span data-ttu-id="6d583-136">Centro sicurezza di Azure di Data Connector</span><span class="sxs-lookup"><span data-stu-id="6d583-136">Data Connector Azure Security Center</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureSecurityCenter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d583-137">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="6d583-137">-DataConnectorId</span></span>
<span data-ttu-id="6d583-138">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="6d583-138">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="6d583-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d583-139">-DefaultProfile</span></span>
<span data-ttu-id="6d583-140">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6d583-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d583-141">-DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="6d583-141">-DiscoveryLogs</span></span>
<span data-ttu-id="6d583-142">Log di individuazione dei connettori dati</span><span class="sxs-lookup"><span data-stu-id="6d583-142">Data Connector Discovery Logs</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftCloudAppSecurity
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d583-143">-Exchange</span><span class="sxs-lookup"><span data-stu-id="6d583-143">-Exchange</span></span>
<span data-ttu-id="6d583-144">Scambio di Data Connector</span><span class="sxs-lookup"><span data-stu-id="6d583-144">Data Connector Exchange</span></span>

```yaml
Type: System.String
Parameter Sets: Office365
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d583-145">-Indicatori</span><span class="sxs-lookup"><span data-stu-id="6d583-145">-Indicators</span></span>
<span data-ttu-id="6d583-146">Indicatori del connettore dati</span><span class="sxs-lookup"><span data-stu-id="6d583-146">Data Connector Indicators</span></span>

```yaml
Type: System.String
Parameter Sets: ThreatIntelligence
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d583-147">-Log</span><span class="sxs-lookup"><span data-stu-id="6d583-147">-Logs</span></span>
<span data-ttu-id="6d583-148">Registri connettore dati</span><span class="sxs-lookup"><span data-stu-id="6d583-148">Data Connector Logs</span></span>

```yaml
Type: System.String
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d583-149">-MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="6d583-149">-MicrosoftCloudAppSecurity</span></span>
<span data-ttu-id="6d583-150">Sicurezza delle app di Microsoft Cloud Data Connector</span><span class="sxs-lookup"><span data-stu-id="6d583-150">Data Connector Microsoft Cloud App Security</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftCloudAppSecurity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d583-151">-MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="6d583-151">-MicrosoftDefenderAdvancedThreatProtection</span></span>
<span data-ttu-id="6d583-152">Data Connector Microsoft Defender Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="6d583-152">Data Connector Microsoft Defender Advanced Threat Protection</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftDefenderAdvancedThreatProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d583-153">-Office365</span><span class="sxs-lookup"><span data-stu-id="6d583-153">-Office365</span></span>
<span data-ttu-id="6d583-154">Data Connector Office 365</span><span class="sxs-lookup"><span data-stu-id="6d583-154">Data Connector Office 365</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Office365
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d583-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d583-155">-ResourceGroupName</span></span>
<span data-ttu-id="6d583-156">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="6d583-156">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="6d583-157">-SharePoint</span><span class="sxs-lookup"><span data-stu-id="6d583-157">-SharePoint</span></span>
<span data-ttu-id="6d583-158">Data Connector SharePoint</span><span class="sxs-lookup"><span data-stu-id="6d583-158">Data Connector SharePoint</span></span>

```yaml
Type: System.String
Parameter Sets: Office365
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d583-159">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d583-159">-SubscriptionId</span></span>
<span data-ttu-id="6d583-160">ID abbonamento a Data Connector</span><span class="sxs-lookup"><span data-stu-id="6d583-160">Data connector Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSecurityCenter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d583-161">-ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="6d583-161">-ThreatIntelligence</span></span>
<span data-ttu-id="6d583-162">Threat Intelligence per il connettore dati</span><span class="sxs-lookup"><span data-stu-id="6d583-162">Data Connector Threat Intelligence</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ThreatIntelligence
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d583-163">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6d583-163">-WorkspaceName</span></span>
<span data-ttu-id="6d583-164">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="6d583-164">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="6d583-165">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6d583-165">-Confirm</span></span>
<span data-ttu-id="6d583-166">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d583-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d583-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d583-167">-WhatIf</span></span>
<span data-ttu-id="6d583-168">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d583-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d583-169">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d583-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d583-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d583-170">CommonParameters</span></span>
<span data-ttu-id="6d583-171">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d583-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d583-172">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d583-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d583-173">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6d583-173">INPUTS</span></span>

### <span data-ttu-id="6d583-174">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6d583-174">None</span></span>
## <span data-ttu-id="6d583-175">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d583-175">OUTPUTS</span></span>

### <span data-ttu-id="6d583-176">Microsoft. Azure. Commands. SecurityInsights. Models. dataconnectors. PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="6d583-176">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="6d583-177">Note</span><span class="sxs-lookup"><span data-stu-id="6d583-177">NOTES</span></span>

## <span data-ttu-id="6d583-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d583-178">RELATED LINKS</span></span>
