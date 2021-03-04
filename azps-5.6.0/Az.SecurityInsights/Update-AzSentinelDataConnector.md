---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/update-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
ms.openlocfilehash: 6ccb7b5a38a85d114e3bb93b594d838c61dcff4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974333"
---
# <span data-ttu-id="478ef-101">Update-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="478ef-101">Update-AzSentinelDataConnector</span></span>

## <span data-ttu-id="478ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="478ef-102">SYNOPSIS</span></span>
<span data-ttu-id="478ef-103">Aggiornare un connettore dati.</span><span class="sxs-lookup"><span data-stu-id="478ef-103">Update a Data Connector.</span></span>

## <span data-ttu-id="478ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="478ef-104">SYNTAX</span></span>

### <span data-ttu-id="478ef-105">DataConnectorId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="478ef-105">DataConnectorId (Default)</span></span>
```
Update-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-Alerts <String>] [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>]
 [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="478ef-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="478ef-106">InputObject</span></span>
```
Update-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-Alerts <String>]
 [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>]
 [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="478ef-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="478ef-107">ResourceId</span></span>
```
Update-AzSentinelDataConnector -ResourceId <String> [-Alerts <String>] [-SubscriptionId <String>]
 [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>]
 [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="478ef-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="478ef-108">DESCRIPTION</span></span>
<span data-ttu-id="478ef-109">Il cmdlet **Update-AzSentinelDataConnector** aggiorna il connettore di dati nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="478ef-109">The **Update-AzSentinelDataConnector** cmdlet updates the Data Connector in the specified workspace.</span></span>
<span data-ttu-id="478ef-110">È possibile passare un **oggetto DataConnector** come parametro o usando l'operatore pipeline oppure in alternativa è possibile specificare i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="478ef-110">You can pass an **DataConnector** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="478ef-111">È possibile usare il *parametro Confirm* $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="478ef-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="478ef-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="478ef-112">EXAMPLES</span></span>

### <span data-ttu-id="478ef-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="478ef-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId" -Alerts Disabled
```

<span data-ttu-id="478ef-114">Il comando recupera il connettore di dati in *base a DataConnectorId* e imposta lo *stato degli* avvisi su *Disabilitato.*</span><span class="sxs-lookup"><span data-stu-id="478ef-114">The command gets the Data Connector by *DataConnectorId* and sets the *Alerts* state to *Disabled*.</span></span>  <span data-ttu-id="478ef-115">Tutte le altre proprietà rimangono invariate.</span><span class="sxs-lookup"><span data-stu-id="478ef-115">All other properties remain the same.</span></span>

## <span data-ttu-id="478ef-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="478ef-116">PARAMETERS</span></span>

### <span data-ttu-id="478ef-117">-Avvisi</span><span class="sxs-lookup"><span data-stu-id="478ef-117">-Alerts</span></span>
<span data-ttu-id="478ef-118">Avvisi connettore dati</span><span class="sxs-lookup"><span data-stu-id="478ef-118">Data Connector Alerts</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="478ef-119">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="478ef-119">-AwsRoleArn</span></span>
<span data-ttu-id="478ef-120">Data Connector AWS Role Arn</span><span class="sxs-lookup"><span data-stu-id="478ef-120">Data Connector AWS Role Arn</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="478ef-121">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="478ef-121">-DataConnectorId</span></span>
<span data-ttu-id="478ef-122">ID connettore dati.</span><span class="sxs-lookup"><span data-stu-id="478ef-122">Data Connector Id.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="478ef-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="478ef-123">-DefaultProfile</span></span>
<span data-ttu-id="478ef-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="478ef-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="478ef-125">-DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="478ef-125">-DiscoveryLogs</span></span>
<span data-ttu-id="478ef-126">Log di individuazione dei connettori di dati</span><span class="sxs-lookup"><span data-stu-id="478ef-126">Data Connector Discovery Logs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="478ef-127">-Exchange</span><span class="sxs-lookup"><span data-stu-id="478ef-127">-Exchange</span></span>
<span data-ttu-id="478ef-128">Exchange con connettore dati</span><span class="sxs-lookup"><span data-stu-id="478ef-128">Data Connector Exchange</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="478ef-129">-Indicatori</span><span class="sxs-lookup"><span data-stu-id="478ef-129">-Indicators</span></span>
<span data-ttu-id="478ef-130">Indicatori del connettore dati</span><span class="sxs-lookup"><span data-stu-id="478ef-130">Data Connector Indicators</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="478ef-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="478ef-131">-InputObject</span></span>
<span data-ttu-id="478ef-132">InputObject.</span><span class="sxs-lookup"><span data-stu-id="478ef-132">InputObject.</span></span>

```yaml
Type: PSSentinelDataConnector
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="478ef-133">-Logs</span><span class="sxs-lookup"><span data-stu-id="478ef-133">-Logs</span></span>
<span data-ttu-id="478ef-134">Log di Data Connector</span><span class="sxs-lookup"><span data-stu-id="478ef-134">Data Connector Logs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="478ef-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="478ef-135">-ResourceGroupName</span></span>
<span data-ttu-id="478ef-136">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="478ef-136">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="478ef-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="478ef-137">-ResourceId</span></span>
<span data-ttu-id="478ef-138">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="478ef-138">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="478ef-139">-SharePoint</span><span class="sxs-lookup"><span data-stu-id="478ef-139">-SharePoint</span></span>
<span data-ttu-id="478ef-140">Connettore dati di SharePoint</span><span class="sxs-lookup"><span data-stu-id="478ef-140">Data Connector SharePoint</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="478ef-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="478ef-141">-SubscriptionId</span></span>
<span data-ttu-id="478ef-142">ID sottoscrizione connettore dati</span><span class="sxs-lookup"><span data-stu-id="478ef-142">Data connector Subscription Id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="478ef-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="478ef-143">-WorkspaceName</span></span>
<span data-ttu-id="478ef-144">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="478ef-144">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="478ef-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="478ef-145">-Confirm</span></span>
<span data-ttu-id="478ef-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="478ef-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="478ef-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="478ef-147">-WhatIf</span></span>
<span data-ttu-id="478ef-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="478ef-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="478ef-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="478ef-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="478ef-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="478ef-150">CommonParameters</span></span>
<span data-ttu-id="478ef-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="478ef-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="478ef-152">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="478ef-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="478ef-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="478ef-153">INPUTS</span></span>

### <span data-ttu-id="478ef-154">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="478ef-154">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>

### <span data-ttu-id="478ef-155">System.String</span><span class="sxs-lookup"><span data-stu-id="478ef-155">System.String</span></span>

## <span data-ttu-id="478ef-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="478ef-156">OUTPUTS</span></span>

### <span data-ttu-id="478ef-157">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="478ef-157">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>

## <span data-ttu-id="478ef-158">NOTE</span><span class="sxs-lookup"><span data-stu-id="478ef-158">NOTES</span></span>

## <span data-ttu-id="478ef-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="478ef-159">RELATED LINKS</span></span>
