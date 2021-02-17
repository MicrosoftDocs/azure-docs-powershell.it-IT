---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincidentowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
ms.openlocfilehash: aa3cddd70ad1c17df9415499d0b33fa33e68f7f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191214"
---
# <span data-ttu-id="58ab7-101">New-AzSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="58ab7-101">New-AzSentinelIncidentOwner</span></span>

## <span data-ttu-id="58ab7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58ab7-102">SYNOPSIS</span></span>
<span data-ttu-id="58ab7-103">Creare l'oggetto Proprietario evento per aggiornare il proprietario di un evento.</span><span class="sxs-lookup"><span data-stu-id="58ab7-103">Create Incident Owner object to update an incident owner.</span></span>

## <span data-ttu-id="58ab7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58ab7-104">SYNTAX</span></span>

```
New-AzSentinelIncidentOwner -AssignedTo <String> -Email <String> -ObjectId <String> -UserPrincipalName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58ab7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="58ab7-105">DESCRIPTION</span></span>
<span data-ttu-id="58ab7-106">Il cmdlet **New-AzSentinelIncidentOwner** crea un oggetto Incident Owner in memoria per aggiornare un evento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="58ab7-106">The **New-AzSentinelIncidentOwner** cmdlet creates a Incident Owner object in memory to update an incident.</span></span>

## <span data-ttu-id="58ab7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58ab7-107">EXAMPLES</span></span>

### <span data-ttu-id="58ab7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="58ab7-108">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $owner = New-AzSentinelIncidentOwner -AssignedTo "First Last" -Email "user@domain.com" -Objectid "userobjectId" -UserPrincipalName "user@domain.com"
PS C:\> $Incident.Owner = $owner
PS C:\> $Incident | Set-AzSentinelIncident
```

<span data-ttu-id="58ab7-109">Questo esempio crea **un proprietario incident** e aggiorna un evento imprevisto al nuovo proprietario.</span><span class="sxs-lookup"><span data-stu-id="58ab7-109">This example creates an **IncidentOwner** and updates an Incident to the new owner.</span></span>

## <span data-ttu-id="58ab7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58ab7-110">PARAMETERS</span></span>

### <span data-ttu-id="58ab7-111">-AssignedTo</span><span class="sxs-lookup"><span data-stu-id="58ab7-111">-AssignedTo</span></span>
<span data-ttu-id="58ab7-112">Proprietario evento - Assegnato a</span><span class="sxs-lookup"><span data-stu-id="58ab7-112">Incident Owner - Assigned To</span></span>

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

### <span data-ttu-id="58ab7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58ab7-113">-DefaultProfile</span></span>
<span data-ttu-id="58ab7-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="58ab7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58ab7-115">-E-mail</span><span class="sxs-lookup"><span data-stu-id="58ab7-115">-Email</span></span>
<span data-ttu-id="58ab7-116">Proprietario dell'evento - Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="58ab7-116">Incident Owner - Email</span></span>

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

### <span data-ttu-id="58ab7-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="58ab7-117">-ObjectId</span></span>
<span data-ttu-id="58ab7-118">Proprietario evento - ObjectId</span><span class="sxs-lookup"><span data-stu-id="58ab7-118">Incident Owner - ObjectId</span></span>

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

### <span data-ttu-id="58ab7-119">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="58ab7-119">-UserPrincipalName</span></span>
<span data-ttu-id="58ab7-120">Proprietario evento - Nome entità utente</span><span class="sxs-lookup"><span data-stu-id="58ab7-120">Incident Owner - User Principal Name</span></span>

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

### <span data-ttu-id="58ab7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58ab7-121">CommonParameters</span></span>
<span data-ttu-id="58ab7-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58ab7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58ab7-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="58ab7-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58ab7-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="58ab7-124">INPUTS</span></span>

### <span data-ttu-id="58ab7-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="58ab7-125">None</span></span>
## <span data-ttu-id="58ab7-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58ab7-126">OUTPUTS</span></span>

### <span data-ttu-id="58ab7-127">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="58ab7-127">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="58ab7-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="58ab7-128">NOTES</span></span>

## <span data-ttu-id="58ab7-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58ab7-129">RELATED LINKS</span></span>
