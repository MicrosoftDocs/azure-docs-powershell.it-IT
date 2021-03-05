---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
ms.openlocfilehash: b25e99766c4dc0433b14810352968300fd5bd129
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986409"
---
# <span data-ttu-id="f893e-101">Get-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="f893e-101">Get-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="f893e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f893e-102">SYNOPSIS</span></span>
<span data-ttu-id="f893e-103">Ottenere un commento per l'evento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="f893e-103">Get an Incident Comment.</span></span>

## <span data-ttu-id="f893e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f893e-104">SYNTAX</span></span>

### <span data-ttu-id="f893e-105">IncidentId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f893e-105">IncidentId (Default)</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f893e-106">IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="f893e-106">IncidentCommentId</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 -IncidentCommentId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f893e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f893e-107">ResourceId</span></span>
```
Get-AzSentinelIncidentComment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f893e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f893e-108">DESCRIPTION</span></span>
<span data-ttu-id="f893e-109">Il **cmdlet Get-AzSentinelIncidentComment** ottiene un commento dell'evento dall'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="f893e-109">The **Get-AzSentinelIncidentComment** cmdlet gets a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="f893e-110">Se si specificano *i parametri IncidentCommentId* e *IncidentId,* viene restituito **un singolo oggetto IncidentComment.**</span><span class="sxs-lookup"><span data-stu-id="f893e-110">If you specify the *IncidentCommentId* and *IncidentId* parameters, a single **IncidentComment** object is returned.</span></span>
<span data-ttu-id="f893e-111">Se non si specifica il parametro *IncidentCommentId,* verrà restituita una matrice contenente tutti i commenti degli incidenti per l'evento imprevisto specificato nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="f893e-111">If you do not specify the *IncidentCommentId* parameter, an array containing all of the Incident Comments for the specified Incident in the specified workspace are returned.</span></span>

## <span data-ttu-id="f893e-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f893e-112">EXAMPLES</span></span>

### <span data-ttu-id="f893e-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f893e-113">Example 1</span></span>
```powershell
PS C:\> $IncidentComments = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="f893e-114">Questo esempio recupera tutti i **incidentComments** per l'evento imprevisto specificato nell'area di lavoro specificata e quindi li archivia nella variabile $IncidentComments specificata.</span><span class="sxs-lookup"><span data-stu-id="f893e-114">This example gets all of the **IncidentComments** for the specified Incident in the specified workspace, and then stores it in the $IncidentComments variable.</span></span>

### <span data-ttu-id="f893e-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f893e-115">Example 2</span></span>
```powershell
PS C:\> $IncidentComment = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -IncidentCommentId "MyIncidentCommentId"
```

<span data-ttu-id="f893e-116">Questo esempio recupera un **commento per** l'evento imprevisto specificato nell'area di lavoro specificata e quindi lo archivia nella variabile $IncidentComment specificata.</span><span class="sxs-lookup"><span data-stu-id="f893e-116">This example gets an **IncidentComment** for the specified Incident in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="f893e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f893e-117">PARAMETERS</span></span>

### <span data-ttu-id="f893e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f893e-118">-DefaultProfile</span></span>
<span data-ttu-id="f893e-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f893e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f893e-120">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="f893e-120">-IncidentCommentId</span></span>
<span data-ttu-id="f893e-121">ID commento evento.</span><span class="sxs-lookup"><span data-stu-id="f893e-121">Incident Comment Id.</span></span>

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

### <span data-ttu-id="f893e-122">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="f893e-122">-IncidentId</span></span>
<span data-ttu-id="f893e-123">ID evento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="f893e-123">Incident Id.</span></span>

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

### <span data-ttu-id="f893e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f893e-124">-ResourceGroupName</span></span>
<span data-ttu-id="f893e-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f893e-125">Resource group name.</span></span>

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

### <span data-ttu-id="f893e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f893e-126">-ResourceId</span></span>
<span data-ttu-id="f893e-127">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="f893e-127">Resource Id.</span></span>

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

### <span data-ttu-id="f893e-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f893e-128">-WorkspaceName</span></span>
<span data-ttu-id="f893e-129">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="f893e-129">Workspace Name.</span></span>

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

### <span data-ttu-id="f893e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f893e-130">CommonParameters</span></span>
<span data-ttu-id="f893e-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f893e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f893e-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f893e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f893e-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="f893e-133">INPUTS</span></span>

### <span data-ttu-id="f893e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f893e-134">System.String</span></span>
## <span data-ttu-id="f893e-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f893e-135">OUTPUTS</span></span>

### <span data-ttu-id="f893e-136">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="f893e-136">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="f893e-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="f893e-137">NOTES</span></span>

## <span data-ttu-id="f893e-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f893e-138">RELATED LINKS</span></span>
