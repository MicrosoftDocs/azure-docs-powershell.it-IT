---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelincidentowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
ms.openlocfilehash: b8981d40f3412dd77ca120cd80d29fb160915e8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950958"
---
# <span data-ttu-id="14ff3-101">New-AzSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="14ff3-101">New-AzSentinelIncidentOwner</span></span>

## <span data-ttu-id="14ff3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14ff3-102">SYNOPSIS</span></span>
<span data-ttu-id="14ff3-103">Creare l'oggetto Proprietario evento per aggiornare il proprietario di un evento.</span><span class="sxs-lookup"><span data-stu-id="14ff3-103">Create Incident Owner object to update an incident owner.</span></span>

## <span data-ttu-id="14ff3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14ff3-104">SYNTAX</span></span>

```
New-AzSentinelIncidentOwner -AssignedTo <String> -Email <String> -ObjectId <String> -UserPrincipalName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14ff3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="14ff3-105">DESCRIPTION</span></span>
<span data-ttu-id="14ff3-106">Il cmdlet **New-AzSentinelIncidentOwner** crea un oggetto Incident Owner in memoria per aggiornare un evento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="14ff3-106">The **New-AzSentinelIncidentOwner** cmdlet creates a Incident Owner object in memory to update an incident.</span></span>

## <span data-ttu-id="14ff3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14ff3-107">EXAMPLES</span></span>

### <span data-ttu-id="14ff3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="14ff3-108">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $owner = New-AzSentinelIncidentOwner -AssignedTo "First Last" -Email "user@domain.com" -Objectid "userobjectId" -UserPrincipalName "user@domain.com"
PS C:\> $Incident.Owner = $owner
PS C:\> $Incident | Set-AzSentinelIncident
```

<span data-ttu-id="14ff3-109">Questo esempio crea **un proprietario incident** e aggiorna un evento imprevisto al nuovo proprietario.</span><span class="sxs-lookup"><span data-stu-id="14ff3-109">This example creates an **IncidentOwner** and updates an Incident to the new owner.</span></span>

## <span data-ttu-id="14ff3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14ff3-110">PARAMETERS</span></span>

### <span data-ttu-id="14ff3-111">-AssignedTo</span><span class="sxs-lookup"><span data-stu-id="14ff3-111">-AssignedTo</span></span>
<span data-ttu-id="14ff3-112">Proprietario evento - Assegnato a</span><span class="sxs-lookup"><span data-stu-id="14ff3-112">Incident Owner - Assigned To</span></span>

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

### <span data-ttu-id="14ff3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14ff3-113">-DefaultProfile</span></span>
<span data-ttu-id="14ff3-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14ff3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14ff3-115">-E-mail</span><span class="sxs-lookup"><span data-stu-id="14ff3-115">-Email</span></span>
<span data-ttu-id="14ff3-116">Proprietario dell'evento - Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="14ff3-116">Incident Owner - Email</span></span>

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

### <span data-ttu-id="14ff3-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="14ff3-117">-ObjectId</span></span>
<span data-ttu-id="14ff3-118">Proprietario evento - ObjectId</span><span class="sxs-lookup"><span data-stu-id="14ff3-118">Incident Owner - ObjectId</span></span>

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

### <span data-ttu-id="14ff3-119">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="14ff3-119">-UserPrincipalName</span></span>
<span data-ttu-id="14ff3-120">Proprietario evento - Nome entità utente</span><span class="sxs-lookup"><span data-stu-id="14ff3-120">Incident Owner - User Principal Name</span></span>

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

### <span data-ttu-id="14ff3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14ff3-121">CommonParameters</span></span>
<span data-ttu-id="14ff3-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14ff3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14ff3-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="14ff3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14ff3-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="14ff3-124">INPUTS</span></span>

### <span data-ttu-id="14ff3-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="14ff3-125">None</span></span>
## <span data-ttu-id="14ff3-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14ff3-126">OUTPUTS</span></span>

### <span data-ttu-id="14ff3-127">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="14ff3-127">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="14ff3-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="14ff3-128">NOTES</span></span>

## <span data-ttu-id="14ff3-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14ff3-129">RELATED LINKS</span></span>
