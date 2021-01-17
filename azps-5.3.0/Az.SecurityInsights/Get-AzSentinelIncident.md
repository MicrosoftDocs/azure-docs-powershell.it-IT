---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
ms.openlocfilehash: eb0854ee3a71af3bdf19d2258187c435fb0f5860
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486212"
---
# <span data-ttu-id="9f282-101">Get-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="9f282-101">Get-AzSentinelIncident</span></span>

## <span data-ttu-id="9f282-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9f282-102">SYNOPSIS</span></span>
<span data-ttu-id="9f282-103">Ottenere un incidente.</span><span class="sxs-lookup"><span data-stu-id="9f282-103">Get an Incident.</span></span>

## <span data-ttu-id="9f282-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9f282-104">SYNTAX</span></span>

### <span data-ttu-id="9f282-105">WorkspaceScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9f282-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f282-106">IncidentId</span><span class="sxs-lookup"><span data-stu-id="9f282-106">IncidentId</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f282-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f282-107">ResourceId</span></span>
```
Get-AzSentinelIncident -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f282-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f282-108">DESCRIPTION</span></span>
<span data-ttu-id="9f282-109">Il cmdlet **Get-AzSentinelIncident** ottiene un evento incidentato dall'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="9f282-109">The **Get-AzSentinelIncident** cmdlet gets an Incident from the specified workspace.</span></span>
<span data-ttu-id="9f282-110">Se specifichi il parametro *IncidentId* , viene restituito un singolo oggetto **Incident** .</span><span class="sxs-lookup"><span data-stu-id="9f282-110">If you specify the *IncidentId* parameter, a single **Incident** object is returned.</span></span>
<span data-ttu-id="9f282-111">Se non specifichi il parametro *IncidentId* , viene restituita una matrice contenente tutti gli eventi imprevisti nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="9f282-111">If you do not specify the *IncidentId* parameter, an array containing all of the Incidents in the specified workspace are returned.</span></span>
<span data-ttu-id="9f282-112">Puoi usare l'oggetto **Incident** per aggiornare l'evento Incident, ad esempio puoi aggiungere note all' **evento Incident**.</span><span class="sxs-lookup"><span data-stu-id="9f282-112">You can use the **Incident** object to update the Incident, for example you can add Notes the **Incident**.</span></span>

## <span data-ttu-id="9f282-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9f282-113">EXAMPLES</span></span>

### <span data-ttu-id="9f282-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9f282-114">Example 1</span></span>
```powershell
PS C:\> $Incidents = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="9f282-115">Questo esempio recupera tutti gli **eventi imprevisti** nell'area di lavoro specificata e lo archivia nella variabile $Incidents.</span><span class="sxs-lookup"><span data-stu-id="9f282-115">This example gets all of the **Incidents** in the specified workspace, and then stores it in the $Incidents variable.</span></span>

### <span data-ttu-id="9f282-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9f282-116">Example 2</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="9f282-117">Questo esempio ottiene un **evento Incident** nell'area di lavoro specificata e lo archivia nella variabile $Incident.</span><span class="sxs-lookup"><span data-stu-id="9f282-117">This example gets an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="9f282-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9f282-118">PARAMETERS</span></span>

### <span data-ttu-id="9f282-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f282-119">-DefaultProfile</span></span>
<span data-ttu-id="9f282-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9f282-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f282-121">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="9f282-121">-IncidentId</span></span>
<span data-ttu-id="9f282-122">ID incidente.</span><span class="sxs-lookup"><span data-stu-id="9f282-122">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f282-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f282-123">-ResourceGroupName</span></span>
<span data-ttu-id="9f282-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9f282-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f282-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f282-125">-ResourceId</span></span>
<span data-ttu-id="9f282-126">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="9f282-126">Resource Id.</span></span>

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

### <span data-ttu-id="9f282-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9f282-127">-WorkspaceName</span></span>
<span data-ttu-id="9f282-128">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9f282-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f282-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f282-129">CommonParameters</span></span>
<span data-ttu-id="9f282-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f282-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f282-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f282-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f282-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9f282-132">INPUTS</span></span>

### <span data-ttu-id="9f282-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9f282-133">System.String</span></span>
## <span data-ttu-id="9f282-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9f282-134">OUTPUTS</span></span>

### <span data-ttu-id="9f282-135">Microsoft. Azure. Commands. SecurityInsights. Models. Incidents. PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="9f282-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="9f282-136">Note</span><span class="sxs-lookup"><span data-stu-id="9f282-136">NOTES</span></span>

## <span data-ttu-id="9f282-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9f282-137">RELATED LINKS</span></span>
