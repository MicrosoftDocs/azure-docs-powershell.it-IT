---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
ms.openlocfilehash: 30b6979be7f3aae23bec5d1ca45d48d4dd2290f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188849"
---
# <span data-ttu-id="7a072-101">Set-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="7a072-101">Set-AzIotSecuritySolution</span></span>

## <span data-ttu-id="7a072-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7a072-102">SYNOPSIS</span></span>
<span data-ttu-id="7a072-103">Soluzione di sicurezza per creare o aggiornare un sacco</span><span class="sxs-lookup"><span data-stu-id="7a072-103">Create or update IoT security solution</span></span>

## <span data-ttu-id="7a072-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a072-104">SYNTAX</span></span>

### <span data-ttu-id="7a072-105">ResourceGroupLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7a072-105">ResourceGroupLevelResource (Default)</span></span>
```
Set-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a072-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7a072-106">InputObject</span></span>
```
Set-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a072-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a072-107">ResourceId</span></span>
```
Set-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>] -Location <String> -Workspace <String>
 -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>] [-DisabledDataSource <String[]>]
 -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a072-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a072-108">DESCRIPTION</span></span>
<span data-ttu-id="7a072-109">Il cmdlet Set-AzIotSecuritySolution crea o aggiorna una specifica soluzione di sicurezza per gli altri.</span><span class="sxs-lookup"><span data-stu-id="7a072-109">The Set-AzIotSecuritySolution cmdlet creates or updates a specific iot security solution.</span></span> <span data-ttu-id="7a072-110">La soluzione per la sicurezza degli argomenti raccoglie i dati di sicurezza e gli eventi provenienti da dispositivi molto e hub per evitare e rilevare le minacce.</span><span class="sxs-lookup"><span data-stu-id="7a072-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>
<span data-ttu-id="7a072-111">Il nome della soluzione di sicurezza degli spessori deve essere identico al nome dell'hub.</span><span class="sxs-lookup"><span data-stu-id="7a072-111">The name of iot security solution should be identical to the name of the iot hub.</span></span>

## <span data-ttu-id="7a072-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a072-112">EXAMPLES</span></span>

### <span data-ttu-id="7a072-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7a072-113">Example 1</span></span>
```powershell
PS C:\> $Workspace = "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.OperationalInsights/workspaces/IoTHubWorkspace"
PS C:\> $IotHubs = @("/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample")
PS C:\> Set-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup" -Location "West US" 
-Workspace $Workspace -DisplayName "MySample" -Enabled $true -IotHub $IotHubs

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
    Query: "" 
    QuerySubscriptions: []
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
    }]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
Tags: {}
```

<span data-ttu-id="7a072-114">Creare una nuova soluzione di sicurezza per gli altri "esempio" per hub degli utili con l'ID risorsa "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (il nome della soluzione deve essere identico al nome dell'hub degli utili)</span><span class="sxs-lookup"><span data-stu-id="7a072-114">Create new iot security solution "MySample" for IoT hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (the name of the solution should be identical to the name of the IoT hub)</span></span>

## <span data-ttu-id="7a072-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7a072-115">PARAMETERS</span></span>

### <span data-ttu-id="7a072-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a072-116">-DefaultProfile</span></span>
<span data-ttu-id="7a072-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7a072-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a072-118">-DisabledDataSource</span><span class="sxs-lookup"><span data-stu-id="7a072-118">-DisabledDataSource</span></span>
<span data-ttu-id="7a072-119">Origini dati disabilitate.</span><span class="sxs-lookup"><span data-stu-id="7a072-119">Disabled data sources.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a072-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7a072-120">-DisplayName</span></span>
<span data-ttu-id="7a072-121">Nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="7a072-121">Display name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a072-122">-Enabled</span><span class="sxs-lookup"><span data-stu-id="7a072-122">-Enabled</span></span>
<span data-ttu-id="7a072-123">Stato.</span><span class="sxs-lookup"><span data-stu-id="7a072-123">Status .</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a072-124">-Export</span><span class="sxs-lookup"><span data-stu-id="7a072-124">-Export</span></span>
<span data-ttu-id="7a072-125">Esportare i dati.</span><span class="sxs-lookup"><span data-stu-id="7a072-125">Export data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a072-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a072-126">-InputObject</span></span>
<span data-ttu-id="7a072-127">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="7a072-127">Input Object.</span></span>

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

### <span data-ttu-id="7a072-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="7a072-128">-IotHub</span></span>
<span data-ttu-id="7a072-129">Hub di un sacco.</span><span class="sxs-lookup"><span data-stu-id="7a072-129">Iot hubs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a072-130">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7a072-130">-Location</span></span>
<span data-ttu-id="7a072-131">Posizione.</span><span class="sxs-lookup"><span data-stu-id="7a072-131">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a072-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a072-132">-Name</span></span>
<span data-ttu-id="7a072-133">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="7a072-133">Resource name.</span></span>

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

### <span data-ttu-id="7a072-134">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a072-134">-RecommendationsConfiguration</span></span>
<span data-ttu-id="7a072-135">Configurazione suggerimenti.</span><span class="sxs-lookup"><span data-stu-id="7a072-135">Recommendations configuration.</span></span>

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

### <span data-ttu-id="7a072-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a072-136">-ResourceGroupName</span></span>
<span data-ttu-id="7a072-137">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7a072-137">Resource group name.</span></span>

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

### <span data-ttu-id="7a072-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a072-138">-ResourceId</span></span>
<span data-ttu-id="7a072-139">ID della risorsa di sicurezza a cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="7a072-139">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="7a072-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="7a072-140">-Tag</span></span>
<span data-ttu-id="7a072-141">Tag.</span><span class="sxs-lookup"><span data-stu-id="7a072-141">Tags.</span></span>

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

### <span data-ttu-id="7a072-142">-UnmaskedIpLoggingStatus</span><span class="sxs-lookup"><span data-stu-id="7a072-142">-UnmaskedIpLoggingStatus</span></span>
<span data-ttu-id="7a072-143">Stato di registrazione IP non mascherato.</span><span class="sxs-lookup"><span data-stu-id="7a072-143">Unmasked ip logging status.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a072-144">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="7a072-144">-UserDefinedResource</span></span>
<span data-ttu-id="7a072-145">Risorse definite dall'utente.</span><span class="sxs-lookup"><span data-stu-id="7a072-145">User defined resources.</span></span>

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

### <span data-ttu-id="7a072-146">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="7a072-146">-Workspace</span></span>
<span data-ttu-id="7a072-147">ID area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="7a072-147">Workspace ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a072-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7a072-148">-Confirm</span></span>
<span data-ttu-id="7a072-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a072-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a072-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a072-150">-WhatIf</span></span>
<span data-ttu-id="7a072-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a072-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a072-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a072-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a072-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a072-153">CommonParameters</span></span>
<span data-ttu-id="7a072-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a072-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a072-155">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a072-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a072-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7a072-156">INPUTS</span></span>

### <span data-ttu-id="7a072-157">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="7a072-157">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="7a072-158">System. String</span><span class="sxs-lookup"><span data-stu-id="7a072-158">System.String</span></span>

### <span data-ttu-id="7a072-159">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7a072-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7a072-160">System. String []</span><span class="sxs-lookup"><span data-stu-id="7a072-160">System.String[]</span></span>

### <span data-ttu-id="7a072-161">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="7a072-161">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="7a072-162">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSRecommendationConfiguration []</span><span class="sxs-lookup"><span data-stu-id="7a072-162">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="7a072-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a072-163">OUTPUTS</span></span>

### <span data-ttu-id="7a072-164">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="7a072-164">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="7a072-165">Note</span><span class="sxs-lookup"><span data-stu-id="7a072-165">NOTES</span></span>

## <span data-ttu-id="7a072-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a072-166">RELATED LINKS</span></span>