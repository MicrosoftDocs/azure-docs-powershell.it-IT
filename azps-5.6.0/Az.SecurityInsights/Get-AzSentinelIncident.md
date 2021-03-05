---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
ms.openlocfilehash: 669e0961327b6419e86f288ec71bffa6cdc69b4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986438"
---
# <span data-ttu-id="fabb9-101">Get-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="fabb9-101">Get-AzSentinelIncident</span></span>

## <span data-ttu-id="fabb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fabb9-102">SYNOPSIS</span></span>
<span data-ttu-id="fabb9-103">Ottieni un evento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="fabb9-103">Get an Incident.</span></span>

## <span data-ttu-id="fabb9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fabb9-104">SYNTAX</span></span>

### <span data-ttu-id="fabb9-105">WorkspaceScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fabb9-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fabb9-106">IncidentId</span><span class="sxs-lookup"><span data-stu-id="fabb9-106">IncidentId</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fabb9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fabb9-107">ResourceId</span></span>
```
Get-AzSentinelIncident -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fabb9-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fabb9-108">DESCRIPTION</span></span>
<span data-ttu-id="fabb9-109">Il **cmdlet Get-AzSentinelIncident** ottiene un evento imprevisto dall'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="fabb9-109">The **Get-AzSentinelIncident** cmdlet gets an Incident from the specified workspace.</span></span>
<span data-ttu-id="fabb9-110">Se si specifica il *parametro IncidentId,* viene restituito **un singolo oggetto Incident.**</span><span class="sxs-lookup"><span data-stu-id="fabb9-110">If you specify the *IncidentId* parameter, a single **Incident** object is returned.</span></span>
<span data-ttu-id="fabb9-111">Se non si specifica il parametro *IncidentId,* verrà restituita una matrice contenente tutti gli eventi imprevisti nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="fabb9-111">If you do not specify the *IncidentId* parameter, an array containing all of the Incidents in the specified workspace are returned.</span></span>
<span data-ttu-id="fabb9-112">È possibile usare **l'oggetto** Evento imprevisto per aggiornare l'evento, ad esempio aggiungere Note per **l'evento imprevisto.**</span><span class="sxs-lookup"><span data-stu-id="fabb9-112">You can use the **Incident** object to update the Incident, for example you can add Notes the **Incident**.</span></span>

## <span data-ttu-id="fabb9-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fabb9-113">EXAMPLES</span></span>

### <span data-ttu-id="fabb9-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fabb9-114">Example 1</span></span>
```powershell
PS C:\> $Incidents = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="fabb9-115">Questo esempio recupera tutti gli eventi **imprevisti nell'area** di lavoro specificata e quindi li archivia nella $Incidents variabile.</span><span class="sxs-lookup"><span data-stu-id="fabb9-115">This example gets all of the **Incidents** in the specified workspace, and then stores it in the $Incidents variable.</span></span>

### <span data-ttu-id="fabb9-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fabb9-116">Example 2</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="fabb9-117">Questo esempio recupera un **evento imprevisto** nell'area di lavoro specificata e quindi lo archivia nella $Incident variabile.</span><span class="sxs-lookup"><span data-stu-id="fabb9-117">This example gets an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="fabb9-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fabb9-118">PARAMETERS</span></span>

### <span data-ttu-id="fabb9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fabb9-119">-DefaultProfile</span></span>
<span data-ttu-id="fabb9-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fabb9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fabb9-121">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="fabb9-121">-IncidentId</span></span>
<span data-ttu-id="fabb9-122">ID evento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="fabb9-122">Incident Id.</span></span>

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

### <span data-ttu-id="fabb9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fabb9-123">-ResourceGroupName</span></span>
<span data-ttu-id="fabb9-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fabb9-124">Resource group name.</span></span>

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

### <span data-ttu-id="fabb9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fabb9-125">-ResourceId</span></span>
<span data-ttu-id="fabb9-126">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="fabb9-126">Resource Id.</span></span>

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

### <span data-ttu-id="fabb9-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fabb9-127">-WorkspaceName</span></span>
<span data-ttu-id="fabb9-128">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="fabb9-128">Workspace Name.</span></span>

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

### <span data-ttu-id="fabb9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fabb9-129">CommonParameters</span></span>
<span data-ttu-id="fabb9-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fabb9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fabb9-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fabb9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fabb9-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="fabb9-132">INPUTS</span></span>

### <span data-ttu-id="fabb9-133">System.String</span><span class="sxs-lookup"><span data-stu-id="fabb9-133">System.String</span></span>
## <span data-ttu-id="fabb9-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fabb9-134">OUTPUTS</span></span>

### <span data-ttu-id="fabb9-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="fabb9-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="fabb9-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="fabb9-136">NOTES</span></span>

## <span data-ttu-id="fabb9-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fabb9-137">RELATED LINKS</span></span>
