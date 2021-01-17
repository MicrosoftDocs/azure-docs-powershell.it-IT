---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincidentowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
ms.openlocfilehash: aa3cddd70ad1c17df9415499d0b33fa33e68f7f4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486179"
---
# <span data-ttu-id="31504-101">New-AzSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="31504-101">New-AzSentinelIncidentOwner</span></span>

## <span data-ttu-id="31504-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31504-102">SYNOPSIS</span></span>
<span data-ttu-id="31504-103">Creare un oggetto proprietario Incident per aggiornare un proprietario dell'evento.</span><span class="sxs-lookup"><span data-stu-id="31504-103">Create Incident Owner object to update an incident owner.</span></span>

## <span data-ttu-id="31504-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31504-104">SYNTAX</span></span>

```
New-AzSentinelIncidentOwner -AssignedTo <String> -Email <String> -ObjectId <String> -UserPrincipalName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31504-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31504-105">DESCRIPTION</span></span>
<span data-ttu-id="31504-106">Il cmdlet **New-AzSentinelIncidentOwner** crea un oggetto Incident Owner in memory per aggiornare un evento Incident.</span><span class="sxs-lookup"><span data-stu-id="31504-106">The **New-AzSentinelIncidentOwner** cmdlet creates a Incident Owner object in memory to update an incident.</span></span>

## <span data-ttu-id="31504-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31504-107">EXAMPLES</span></span>

### <span data-ttu-id="31504-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="31504-108">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $owner = New-AzSentinelIncidentOwner -AssignedTo "First Last" -Email "user@domain.com" -Objectid "userobjectId" -UserPrincipalName "user@domain.com"
PS C:\> $Incident.Owner = $owner
PS C:\> $Incident | Set-AzSentinelIncident
```

<span data-ttu-id="31504-109">Questo esempio crea un **IncidentOwner** e aggiorna un evento Incident nel nuovo proprietario.</span><span class="sxs-lookup"><span data-stu-id="31504-109">This example creates an **IncidentOwner** and updates an Incident to the new owner.</span></span>

## <span data-ttu-id="31504-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31504-110">PARAMETERS</span></span>

### <span data-ttu-id="31504-111">-AssignedTo</span><span class="sxs-lookup"><span data-stu-id="31504-111">-AssignedTo</span></span>
<span data-ttu-id="31504-112">Proprietario dell'evento-assegnato a</span><span class="sxs-lookup"><span data-stu-id="31504-112">Incident Owner - Assigned To</span></span>

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

### <span data-ttu-id="31504-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31504-113">-DefaultProfile</span></span>
<span data-ttu-id="31504-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31504-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31504-115">-Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="31504-115">-Email</span></span>
<span data-ttu-id="31504-116">Proprietario incidente-posta elettronica</span><span class="sxs-lookup"><span data-stu-id="31504-116">Incident Owner - Email</span></span>

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

### <span data-ttu-id="31504-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="31504-117">-ObjectId</span></span>
<span data-ttu-id="31504-118">Proprietario dell'evento-ObjectId</span><span class="sxs-lookup"><span data-stu-id="31504-118">Incident Owner - ObjectId</span></span>

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

### <span data-ttu-id="31504-119">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="31504-119">-UserPrincipalName</span></span>
<span data-ttu-id="31504-120">Proprietario incidente-nome dell'entità utente</span><span class="sxs-lookup"><span data-stu-id="31504-120">Incident Owner - User Principal Name</span></span>

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

### <span data-ttu-id="31504-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31504-121">CommonParameters</span></span>
<span data-ttu-id="31504-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31504-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31504-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31504-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31504-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31504-124">INPUTS</span></span>

### <span data-ttu-id="31504-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="31504-125">None</span></span>
## <span data-ttu-id="31504-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31504-126">OUTPUTS</span></span>

### <span data-ttu-id="31504-127">Microsoft. Azure. Commands. SecurityInsights. Models. Incidents. PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="31504-127">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="31504-128">Note</span><span class="sxs-lookup"><span data-stu-id="31504-128">NOTES</span></span>

## <span data-ttu-id="31504-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31504-129">RELATED LINKS</span></span>
