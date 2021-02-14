---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
ms.openlocfilehash: 338486954fe04b6497eb82bc5a11dbede1b25709
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176359"
---
# <span data-ttu-id="c2371-101">Get-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="c2371-101">Get-AzIotSecuritySolution</span></span>

## <span data-ttu-id="c2371-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2371-102">SYNOPSIS</span></span>
<span data-ttu-id="c2371-103">Ottieni la soluzione di sicurezza IoT</span><span class="sxs-lookup"><span data-stu-id="c2371-103">Get IoT security solution</span></span>

## <span data-ttu-id="c2371-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2371-104">SYNTAX</span></span>

### <span data-ttu-id="c2371-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c2371-105">SubscriptionScope (Default)</span></span>
```
Get-AzIotSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2371-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="c2371-106">ResourceGroupScope</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2371-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="c2371-107">ResourceGroupLevelResource</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2371-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2371-108">ResourceId</span></span>
```
Get-AzIotSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2371-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c2371-109">DESCRIPTION</span></span>
<span data-ttu-id="c2371-110">Il Get-AzIotSecuritySolution cmdlet di sicurezza restituisce una o più soluzioni di sicurezza iot.</span><span class="sxs-lookup"><span data-stu-id="c2371-110">The Get-AzIotSecuritySolution cmdlet returns one or more iot security solutions.</span></span> <span data-ttu-id="c2371-111">La soluzione di sicurezza IoT raccoglie dati di sicurezza ed eventi dai dispositivi iot e dall'hub iot per prevenire e rilevare le minacce.</span><span class="sxs-lookup"><span data-stu-id="c2371-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="c2371-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2371-112">EXAMPLES</span></span>

### <span data-ttu-id="c2371-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c2371-113">Example 1</span></span>
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

<span data-ttu-id="c2371-114">Ottenere la soluzione "MySample" nel gruppo di risorse "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="c2371-114">Get the solution "MySample" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="c2371-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c2371-115">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -ResourceGroupName "MyResourceGroup"

Array of security solution items as shown is example 1
```

<span data-ttu-id="c2371-116">Ottenere l'elenco di tutte le soluzioni di sicurezza nel gruppo di risorse "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="c2371-116">Get list of all security solutions in resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="c2371-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2371-117">PARAMETERS</span></span>

### <span data-ttu-id="c2371-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2371-118">-DefaultProfile</span></span>
<span data-ttu-id="c2371-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c2371-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2371-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c2371-120">-Name</span></span>
<span data-ttu-id="c2371-121">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c2371-121">Resource name.</span></span>

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

### <span data-ttu-id="c2371-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2371-122">-ResourceGroupName</span></span>
<span data-ttu-id="c2371-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c2371-123">Resource group name.</span></span>

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

### <span data-ttu-id="c2371-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2371-124">-ResourceId</span></span>
<span data-ttu-id="c2371-125">ID della risorsa di sicurezza su cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="c2371-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="c2371-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2371-126">CommonParameters</span></span>
<span data-ttu-id="c2371-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2371-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2371-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c2371-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2371-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="c2371-129">INPUTS</span></span>

### <span data-ttu-id="c2371-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c2371-130">System.String</span></span>

## <span data-ttu-id="c2371-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2371-131">OUTPUTS</span></span>

### <span data-ttu-id="c2371-132">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="c2371-132">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="c2371-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="c2371-133">NOTES</span></span>

## <span data-ttu-id="c2371-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2371-134">RELATED LINKS</span></span>
