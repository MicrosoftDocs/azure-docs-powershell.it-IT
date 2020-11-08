---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
ms.openlocfilehash: 338486954fe04b6497eb82bc5a11dbede1b25709
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191946"
---
# <span data-ttu-id="798e4-101">Get-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="798e4-101">Get-AzIotSecuritySolution</span></span>

## <span data-ttu-id="798e4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="798e4-102">SYNOPSIS</span></span>
<span data-ttu-id="798e4-103">Soluzione di sicurezza per gli altri</span><span class="sxs-lookup"><span data-stu-id="798e4-103">Get IoT security solution</span></span>

## <span data-ttu-id="798e4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="798e4-104">SYNTAX</span></span>

### <span data-ttu-id="798e4-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="798e4-105">SubscriptionScope (Default)</span></span>
```
Get-AzIotSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="798e4-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="798e4-106">ResourceGroupScope</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="798e4-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="798e4-107">ResourceGroupLevelResource</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="798e4-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="798e4-108">ResourceId</span></span>
```
Get-AzIotSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="798e4-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="798e4-109">DESCRIPTION</span></span>
<span data-ttu-id="798e4-110">Il cmdlet Get-AzIotSecuritySolution restituisce una o più soluzioni di sicurezza per gli altri.</span><span class="sxs-lookup"><span data-stu-id="798e4-110">The Get-AzIotSecuritySolution cmdlet returns one or more iot security solutions.</span></span> <span data-ttu-id="798e4-111">La soluzione per la sicurezza degli argomenti raccoglie i dati di sicurezza e gli eventi provenienti da dispositivi molto e hub per evitare e rilevare le minacce.</span><span class="sxs-lookup"><span data-stu-id="798e4-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="798e4-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="798e4-112">EXAMPLES</span></span>

### <span data-ttu-id="798e4-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="798e4-113">Example 1</span></span>
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

<span data-ttu-id="798e4-114">Ottenere la soluzione "esempio" nel gruppo di risorse "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="798e4-114">Get the solution "MySample" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="798e4-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="798e4-115">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -ResourceGroupName "MyResourceGroup"

Array of security solution items as shown is example 1
```

<span data-ttu-id="798e4-116">Ottenere l'elenco di tutte le soluzioni di sicurezza nel gruppo di risorse "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="798e4-116">Get list of all security solutions in resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="798e4-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="798e4-117">PARAMETERS</span></span>

### <span data-ttu-id="798e4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="798e4-118">-DefaultProfile</span></span>
<span data-ttu-id="798e4-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="798e4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="798e4-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="798e4-120">-Name</span></span>
<span data-ttu-id="798e4-121">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="798e4-121">Resource name.</span></span>

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

### <span data-ttu-id="798e4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="798e4-122">-ResourceGroupName</span></span>
<span data-ttu-id="798e4-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="798e4-123">Resource group name.</span></span>

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

### <span data-ttu-id="798e4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="798e4-124">-ResourceId</span></span>
<span data-ttu-id="798e4-125">ID della risorsa di sicurezza a cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="798e4-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="798e4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="798e4-126">CommonParameters</span></span>
<span data-ttu-id="798e4-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="798e4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="798e4-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="798e4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="798e4-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="798e4-129">INPUTS</span></span>

### <span data-ttu-id="798e4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="798e4-130">System.String</span></span>

## <span data-ttu-id="798e4-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="798e4-131">OUTPUTS</span></span>

### <span data-ttu-id="798e4-132">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="798e4-132">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="798e4-133">Note</span><span class="sxs-lookup"><span data-stu-id="798e4-133">NOTES</span></span>

## <span data-ttu-id="798e4-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="798e4-134">RELATED LINKS</span></span>
