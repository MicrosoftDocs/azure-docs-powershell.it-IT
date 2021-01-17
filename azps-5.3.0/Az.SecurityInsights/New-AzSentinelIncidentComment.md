---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
ms.openlocfilehash: 8824832b1b3d09a24998891ad4636e3a3e0f1e19
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486180"
---
# <span data-ttu-id="4a8b3-101">New-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="4a8b3-101">New-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="4a8b3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4a8b3-102">SYNOPSIS</span></span>
<span data-ttu-id="4a8b3-103">Aggiungere un commento Incident a un evento Incident.</span><span class="sxs-lookup"><span data-stu-id="4a8b3-103">Add an Incident Comment to an Incident.</span></span>

## <span data-ttu-id="4a8b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a8b3-104">SYNTAX</span></span>

```
New-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-IncidentCommentId <String>] -Message <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a8b3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a8b3-105">DESCRIPTION</span></span>
<span data-ttu-id="4a8b3-106">Il cmdlet **New-AzSentinelIncidentComment** crea un commento Incident dall'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="4a8b3-106">The **New-AzSentinelIncidentComment** cmdlet creates a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="4a8b3-107">Puoi usare il parametro *Confirm* e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="4a8b3-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="4a8b3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a8b3-108">EXAMPLES</span></span>

### <span data-ttu-id="4a8b3-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4a8b3-109">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $IncidentComment = New-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId ($Incident.Name) -Message "Still needs investigation"
```

<span data-ttu-id="4a8b3-110">Questo esempio crea un **IncidentComment** nell'area di lavoro specificata e lo archivia nella variabile $IncidentComment.</span><span class="sxs-lookup"><span data-stu-id="4a8b3-110">This example creates an **IncidentComment** in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="4a8b3-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4a8b3-111">PARAMETERS</span></span>

### <span data-ttu-id="4a8b3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a8b3-112">-DefaultProfile</span></span>
<span data-ttu-id="4a8b3-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4a8b3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a8b3-114">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="4a8b3-114">-IncidentCommentId</span></span>
<span data-ttu-id="4a8b3-115">ID commento incidente.</span><span class="sxs-lookup"><span data-stu-id="4a8b3-115">Incident Comment Id.</span></span>

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

### <span data-ttu-id="4a8b3-116">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="4a8b3-116">-IncidentId</span></span>
<span data-ttu-id="4a8b3-117">ID incidente.</span><span class="sxs-lookup"><span data-stu-id="4a8b3-117">Incident Id.</span></span>

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

### <span data-ttu-id="4a8b3-118">-Messaggio</span><span class="sxs-lookup"><span data-stu-id="4a8b3-118">-Message</span></span>
<span data-ttu-id="4a8b3-119">Messaggio di incidente.</span><span class="sxs-lookup"><span data-stu-id="4a8b3-119">Incident Message.</span></span>

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

### <span data-ttu-id="4a8b3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a8b3-120">-ResourceGroupName</span></span>
<span data-ttu-id="4a8b3-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4a8b3-121">Resource group name.</span></span>

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

### <span data-ttu-id="4a8b3-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4a8b3-122">-WorkspaceName</span></span>
<span data-ttu-id="4a8b3-123">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="4a8b3-123">Workspace Name.</span></span>

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

### <span data-ttu-id="4a8b3-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4a8b3-124">-Confirm</span></span>
<span data-ttu-id="4a8b3-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a8b3-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a8b3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a8b3-126">-WhatIf</span></span>
<span data-ttu-id="4a8b3-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a8b3-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a8b3-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a8b3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a8b3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a8b3-129">CommonParameters</span></span>
<span data-ttu-id="4a8b3-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a8b3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a8b3-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a8b3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a8b3-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4a8b3-132">INPUTS</span></span>

### <span data-ttu-id="4a8b3-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4a8b3-133">None</span></span>
## <span data-ttu-id="4a8b3-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a8b3-134">OUTPUTS</span></span>

### <span data-ttu-id="4a8b3-135">Microsoft. Azure. Commands. SecurityInsights. Models. IncidentComments. PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="4a8b3-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="4a8b3-136">Note</span><span class="sxs-lookup"><span data-stu-id="4a8b3-136">NOTES</span></span>

## <span data-ttu-id="4a8b3-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a8b3-137">RELATED LINKS</span></span>
