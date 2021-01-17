---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Update-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
ms.openlocfilehash: ba84bccc92b58b7f8a21812e2f1599bbc9679d38
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353671"
---
# <span data-ttu-id="b25c9-101">Update-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="b25c9-101">Update-AzIotSecuritySolution</span></span>

## <span data-ttu-id="b25c9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b25c9-102">SYNOPSIS</span></span>
<span data-ttu-id="b25c9-103">Aggiornare una o più delle proprietà seguenti nella soluzione di sicurezza degli utenti: Tag, configurazione della raccomandazione, risorse definite dall'utente</span><span class="sxs-lookup"><span data-stu-id="b25c9-103">Update one or more of the following properties in IoT security solution: tags, recommendation configuration, user defined resources</span></span>

## <span data-ttu-id="b25c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b25c9-104">SYNTAX</span></span>

### <span data-ttu-id="b25c9-105">ResourceGroupLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b25c9-105">ResourceGroupLevelResource (Default)</span></span>
```
Update-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b25c9-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b25c9-106">ResourceId</span></span>
```
Update-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b25c9-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b25c9-107">InputObject</span></span>
```
Update-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b25c9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b25c9-108">DESCRIPTION</span></span>
<span data-ttu-id="b25c9-109">Il cmdlet Update-AzIotSecuritySolution updayes una o più delle proprietà seguenti in una specifica soluzione di sicurezza per gli utenti: Tag, configurazione della raccomandazione, risorse definite dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b25c9-109">The Update-AzIotSecuritySolution cmdlet updayes one or more of the following properties in a specific IoT security solution: tags, recommendation configuration, user defined resources.</span></span>
<span data-ttu-id="b25c9-110">Solo le proprietà specificate verranno aggiornate all'interno della soluzione di sicurezza molto.</span><span class="sxs-lookup"><span data-stu-id="b25c9-110">Only the specified properties will be updated inside the iot security solution.</span></span>
<span data-ttu-id="b25c9-111">La soluzione per la sicurezza degli argomenti raccoglie i dati di sicurezza e gli eventi provenienti da dispositivi molto e hub per evitare e rilevare le minacce.</span><span class="sxs-lookup"><span data-stu-id="b25c9-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="b25c9-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b25c9-112">EXAMPLES</span></span>

### <span data-ttu-id="b25c9-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b25c9-113">Example 1</span></span>
```powershell
PS C:\> $RecConfig = New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_OpenPorts" -Enabled $false
PS C:\> $UserDefinedResource = New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")   
PS C:\> Update-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup" -RecommendationsConfiguration @($RecConfig) -UserDefinedResource $UserDefinedResource

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/IoTSecuritySolutions/MySample"
Name: "MySample"
Type: "Microsoft.Security/IoTSecuritySolutions"
Location: "westus"
DisplayName: "MySample"
status: "Enabled"
Export: ["RawEvents"]
DisabledDataSources: ["TwinData"]
Workspace: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.operationalinsights/workspaces/MyLA"
AdditionalWorkspaces: null
IotHubs: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UserDefinedResources: {
    Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
    QuerySubscriptions: ["XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"]
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_OpenPorts"
    Name: "Device has open port"
    Status: "Disabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
}]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
```

<span data-ttu-id="b25c9-114">Aggiornamento della soluzione di sicurezza per gli utenti "esempio" dal gruppo di risorse "MyResourceGroup" con la configurazione delle raccomandazioni e le risorse definite dall'utente</span><span class="sxs-lookup"><span data-stu-id="b25c9-114">Update iot security solution "MySample" from resource group "MyResourceGroup" with recommendation configuration and user defined resources</span></span>

## <span data-ttu-id="b25c9-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b25c9-115">PARAMETERS</span></span>

### <span data-ttu-id="b25c9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b25c9-116">-DefaultProfile</span></span>
<span data-ttu-id="b25c9-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b25c9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b25c9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b25c9-118">-InputObject</span></span>
<span data-ttu-id="b25c9-119">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="b25c9-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b25c9-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b25c9-120">-Name</span></span>
<span data-ttu-id="b25c9-121">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="b25c9-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b25c9-122">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="b25c9-122">-RecommendationsConfiguration</span></span>
<span data-ttu-id="b25c9-123">Configurazione suggerimenti.</span><span class="sxs-lookup"><span data-stu-id="b25c9-123">Recommendations configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b25c9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b25c9-124">-ResourceGroupName</span></span>
<span data-ttu-id="b25c9-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b25c9-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b25c9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b25c9-126">-ResourceId</span></span>
<span data-ttu-id="b25c9-127">ID della risorsa di sicurezza a cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="b25c9-127">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b25c9-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="b25c9-128">-Tag</span></span>
<span data-ttu-id="b25c9-129">Tag.</span><span class="sxs-lookup"><span data-stu-id="b25c9-129">Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b25c9-130">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="b25c9-130">-UserDefinedResource</span></span>
<span data-ttu-id="b25c9-131">Risorse definite dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b25c9-131">User defined resources.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b25c9-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b25c9-132">-Confirm</span></span>
<span data-ttu-id="b25c9-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b25c9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b25c9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b25c9-134">-WhatIf</span></span>
<span data-ttu-id="b25c9-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b25c9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b25c9-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b25c9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b25c9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b25c9-137">CommonParameters</span></span>
<span data-ttu-id="b25c9-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b25c9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b25c9-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b25c9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b25c9-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b25c9-140">INPUTS</span></span>

### <span data-ttu-id="b25c9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b25c9-141">System.String</span></span>

### <span data-ttu-id="b25c9-142">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="b25c9-142">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="b25c9-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b25c9-143">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b25c9-144">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="b25c9-144">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="b25c9-145">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSRecommendationConfiguration []</span><span class="sxs-lookup"><span data-stu-id="b25c9-145">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="b25c9-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b25c9-146">OUTPUTS</span></span>

### <span data-ttu-id="b25c9-147">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="b25c9-147">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="b25c9-148">Note</span><span class="sxs-lookup"><span data-stu-id="b25c9-148">NOTES</span></span>

## <span data-ttu-id="b25c9-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b25c9-149">RELATED LINKS</span></span>
