---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
ms.openlocfilehash: d0bcbaf0edee0a0631621c0dccc73f8d6eda4c74
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973517"
---
# <span data-ttu-id="5b4ab-101">Get-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="5b4ab-101">Get-AzIotSecuritySolution</span></span>

## <span data-ttu-id="5b4ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b4ab-102">SYNOPSIS</span></span>
<span data-ttu-id="5b4ab-103">Ottieni la soluzione di sicurezza IoT</span><span class="sxs-lookup"><span data-stu-id="5b4ab-103">Get IoT security solution</span></span>

## <span data-ttu-id="5b4ab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b4ab-104">SYNTAX</span></span>

### <span data-ttu-id="5b4ab-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5b4ab-105">SubscriptionScope (Default)</span></span>
```
Get-AzIotSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b4ab-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="5b4ab-106">ResourceGroupScope</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b4ab-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="5b4ab-107">ResourceGroupLevelResource</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b4ab-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b4ab-108">ResourceId</span></span>
```
Get-AzIotSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b4ab-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5b4ab-109">DESCRIPTION</span></span>
<span data-ttu-id="5b4ab-110">Il Get-AzIotSecuritySolution cmdlet di sicurezza restituisce una o più soluzioni di sicurezza iot.</span><span class="sxs-lookup"><span data-stu-id="5b4ab-110">The Get-AzIotSecuritySolution cmdlet returns one or more iot security solutions.</span></span> <span data-ttu-id="5b4ab-111">La soluzione di sicurezza IoT raccoglie dati di sicurezza ed eventi dai dispositivi iot e dall'hub iot per prevenire e rilevare le minacce.</span><span class="sxs-lookup"><span data-stu-id="5b4ab-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="5b4ab-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b4ab-112">EXAMPLES</span></span>

### <span data-ttu-id="5b4ab-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5b4ab-113">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/IoTSecuritySolutions/MySample"
Name: "MySample"
Type: "Microsoft.Security/IoTSecuritySolutions"
Location: "centraluseuap"
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

<span data-ttu-id="5b4ab-114">Ottenere la soluzione "MySample" nel gruppo di risorse "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="5b4ab-114">Get the solution "MySample" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="5b4ab-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5b4ab-115">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -ResourceGroupName "MyResourceGroup"

Array of security solution items as shown is example 1
```

<span data-ttu-id="5b4ab-116">Ottenere l'elenco di tutte le soluzioni di sicurezza nel gruppo di risorse "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="5b4ab-116">Get list of all security solutions in resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="5b4ab-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b4ab-117">PARAMETERS</span></span>

### <span data-ttu-id="5b4ab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b4ab-118">-DefaultProfile</span></span>
<span data-ttu-id="5b4ab-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5b4ab-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b4ab-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5b4ab-120">-Name</span></span>
<span data-ttu-id="5b4ab-121">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5b4ab-121">Resource name.</span></span>

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

### <span data-ttu-id="5b4ab-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b4ab-122">-ResourceGroupName</span></span>
<span data-ttu-id="5b4ab-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5b4ab-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4ab-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b4ab-124">-ResourceId</span></span>
<span data-ttu-id="5b4ab-125">ID della risorsa di sicurezza su cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="5b4ab-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="5b4ab-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b4ab-126">CommonParameters</span></span>
<span data-ttu-id="5b4ab-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b4ab-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b4ab-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5b4ab-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b4ab-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="5b4ab-129">INPUTS</span></span>

### <span data-ttu-id="5b4ab-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5b4ab-130">System.String</span></span>

## <span data-ttu-id="5b4ab-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b4ab-131">OUTPUTS</span></span>

### <span data-ttu-id="5b4ab-132">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="5b4ab-132">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="5b4ab-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="5b4ab-133">NOTES</span></span>

## <span data-ttu-id="5b4ab-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b4ab-134">RELATED LINKS</span></span>
