---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
ms.openlocfilehash: d33c126da2a77736871a9ec1f950382168f52bee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486208"
---
# <span data-ttu-id="9ed0c-101">Get-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="9ed0c-101">Get-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="9ed0c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9ed0c-102">SYNOPSIS</span></span>
<span data-ttu-id="9ed0c-103">Ottenere un commento di incidente.</span><span class="sxs-lookup"><span data-stu-id="9ed0c-103">Get an Incident Comment.</span></span>

## <span data-ttu-id="9ed0c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9ed0c-104">SYNTAX</span></span>

### <span data-ttu-id="9ed0c-105">IncidentId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9ed0c-105">IncidentId (Default)</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ed0c-106">IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="9ed0c-106">IncidentCommentId</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 -IncidentCommentId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ed0c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ed0c-107">ResourceId</span></span>
```
Get-AzSentinelIncidentComment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ed0c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ed0c-108">DESCRIPTION</span></span>
<span data-ttu-id="9ed0c-109">Il cmdlet **Get-AzSentinelIncidentComment** ottiene un commento Incident dall'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="9ed0c-109">The **Get-AzSentinelIncidentComment** cmdlet gets a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="9ed0c-110">Se specifichi i parametri *IncidentCommentId* e *IncidentId* , viene restituito un singolo oggetto **IncidentComment** .</span><span class="sxs-lookup"><span data-stu-id="9ed0c-110">If you specify the *IncidentCommentId* and *IncidentId* parameters, a single **IncidentComment** object is returned.</span></span>
<span data-ttu-id="9ed0c-111">Se non specifichi il parametro *IncidentCommentId* , viene restituita una matrice contenente tutti i commenti imprevisti per l'evento Incident specificato nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="9ed0c-111">If you do not specify the *IncidentCommentId* parameter, an array containing all of the Incident Comments for the specified Incident in the specified workspace are returned.</span></span>

## <span data-ttu-id="9ed0c-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9ed0c-112">EXAMPLES</span></span>

### <span data-ttu-id="9ed0c-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9ed0c-113">Example 1</span></span>
```powershell
PS C:\> $IncidentComments = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="9ed0c-114">Questo esempio recupera tutti i **IncidentComments** per l'evento Incident specificato nell'area di lavoro specificata e lo archivia nella variabile $IncidentComments.</span><span class="sxs-lookup"><span data-stu-id="9ed0c-114">This example gets all of the **IncidentComments** for the specified Incident in the specified workspace, and then stores it in the $IncidentComments variable.</span></span>

### <span data-ttu-id="9ed0c-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9ed0c-115">Example 2</span></span>
```powershell
PS C:\> $IncidentComment = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -IncidentCommentId "MyIncidentCommentId"
```

<span data-ttu-id="9ed0c-116">Questo esempio ottiene un **IncidentComment** per l'evento Incident specificato nell'area di lavoro specificata e lo archivia nella variabile $IncidentComment.</span><span class="sxs-lookup"><span data-stu-id="9ed0c-116">This example gets an **IncidentComment** for the specified Incident in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="9ed0c-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9ed0c-117">PARAMETERS</span></span>

### <span data-ttu-id="9ed0c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ed0c-118">-DefaultProfile</span></span>
<span data-ttu-id="9ed0c-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9ed0c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ed0c-120">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="9ed0c-120">-IncidentCommentId</span></span>
<span data-ttu-id="9ed0c-121">ID commento incidente.</span><span class="sxs-lookup"><span data-stu-id="9ed0c-121">Incident Comment Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ed0c-122">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="9ed0c-122">-IncidentId</span></span>
<span data-ttu-id="9ed0c-123">ID incidente.</span><span class="sxs-lookup"><span data-stu-id="9ed0c-123">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ed0c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ed0c-124">-ResourceGroupName</span></span>
<span data-ttu-id="9ed0c-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9ed0c-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ed0c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ed0c-126">-ResourceId</span></span>
<span data-ttu-id="9ed0c-127">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="9ed0c-127">Resource Id.</span></span>

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

### <span data-ttu-id="9ed0c-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9ed0c-128">-WorkspaceName</span></span>
<span data-ttu-id="9ed0c-129">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9ed0c-129">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ed0c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ed0c-130">CommonParameters</span></span>
<span data-ttu-id="9ed0c-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ed0c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ed0c-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ed0c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ed0c-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9ed0c-133">INPUTS</span></span>

### <span data-ttu-id="9ed0c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9ed0c-134">System.String</span></span>
## <span data-ttu-id="9ed0c-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9ed0c-135">OUTPUTS</span></span>

### <span data-ttu-id="9ed0c-136">Microsoft. Azure. Commands. SecurityInsights. Models. IncidentComments. PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="9ed0c-136">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="9ed0c-137">Note</span><span class="sxs-lookup"><span data-stu-id="9ed0c-137">NOTES</span></span>

## <span data-ttu-id="9ed0c-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9ed0c-138">RELATED LINKS</span></span>
