---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/powershell/module/az.portal/get-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
ms.openlocfilehash: fc888161df56e3edbf1a51014c7173542e395ad3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989028"
---
# <span data-ttu-id="ac60f-101">Get-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="ac60f-101">Get-AzPortalDashboard</span></span>

## <span data-ttu-id="ac60f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac60f-102">SYNOPSIS</span></span>
<span data-ttu-id="ac60f-103">Ottiene il dashboard.</span><span class="sxs-lookup"><span data-stu-id="ac60f-103">Gets the Dashboard.</span></span>

## <span data-ttu-id="ac60f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac60f-104">SYNTAX</span></span>

### <span data-ttu-id="ac60f-105">Elenco1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ac60f-105">List1 (Default)</span></span>
```
Get-AzPortalDashboard [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ac60f-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="ac60f-106">Get</span></span>
```
Get-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ac60f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ac60f-107">GetViaIdentity</span></span>
```
Get-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ac60f-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="ac60f-108">List</span></span>
```
Get-AzPortalDashboard -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac60f-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ac60f-109">DESCRIPTION</span></span>
<span data-ttu-id="ac60f-110">Ottiene il dashboard.</span><span class="sxs-lookup"><span data-stu-id="ac60f-110">Gets the Dashboard.</span></span>

## <span data-ttu-id="ac60f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac60f-111">EXAMPLES</span></span>

### <span data-ttu-id="ac60f-112">Esempio 1: Elencare tutti i dashboard di una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="ac60f-112">Example 1: List all dashboards in a subscription</span></span>
```powershell
PS C:> Get-AzPortalDashboard                                                                                                                     
Location Name                                           Type
-------- ----                                           ----
eastasia my-custom-dashboard1                           Microsoft.Portal/dashboards
westus   my-second-custom-dashboard1                    Microsoft.Portal/dashboards

```

<span data-ttu-id="ac60f-113">Elencare tutti i dashboard di una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="ac60f-113">List all dashboards in a subscription</span></span>

### <span data-ttu-id="ac60f-114">Esempio 2: Ottenere i dettagli per un singolo dashboard del portale</span><span class="sxs-lookup"><span data-stu-id="ac60f-114">Example 2: Get details for a single Portal Dashboard</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name mydashboard

Location Name        Type
-------- ----        ----
eastus   mydashboard Microsoft.Portal/dashboards
```

<span data-ttu-id="ac60f-115">Ottenere i dettagli per un singolo dashboard</span><span class="sxs-lookup"><span data-stu-id="ac60f-115">Get details for a single dashboard</span></span>

## <span data-ttu-id="ac60f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac60f-116">PARAMETERS</span></span>

### <span data-ttu-id="ac60f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac60f-117">-DefaultProfile</span></span>
<span data-ttu-id="ac60f-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ac60f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac60f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac60f-119">-InputObject</span></span>
<span data-ttu-id="ac60f-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ac60f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac60f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ac60f-121">-Name</span></span>
<span data-ttu-id="ac60f-122">Nome del dashboard.</span><span class="sxs-lookup"><span data-stu-id="ac60f-122">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac60f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac60f-123">-ResourceGroupName</span></span>
<span data-ttu-id="ac60f-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ac60f-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac60f-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac60f-125">-SubscriptionId</span></span>
<span data-ttu-id="ac60f-126">ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ac60f-126">The Azure subscription ID.</span></span>
<span data-ttu-id="ac60f-127">Stringa in formato GUID, ad esempio 00000000-0000-0000-0000-0000-000000000000000.</span><span class="sxs-lookup"><span data-stu-id="ac60f-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac60f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac60f-128">CommonParameters</span></span>
<span data-ttu-id="ac60f-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac60f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac60f-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ac60f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac60f-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="ac60f-131">INPUTS</span></span>

### <span data-ttu-id="ac60f-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="ac60f-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="ac60f-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac60f-133">OUTPUTS</span></span>

### <span data-ttu-id="ac60f-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="ac60f-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="ac60f-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="ac60f-135">NOTES</span></span>

<span data-ttu-id="ac60f-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ac60f-136">ALIASES</span></span>

<span data-ttu-id="ac60f-137">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="ac60f-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ac60f-138">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ac60f-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ac60f-139">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ac60f-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ac60f-140">INPUTOBJECT <IPortalIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="ac60f-140">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ac60f-141">`[DashboardName <String>]`: nome del dashboard.</span><span class="sxs-lookup"><span data-stu-id="ac60f-141">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="ac60f-142">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="ac60f-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ac60f-143">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ac60f-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="ac60f-144">`[SubscriptionId <String>]`: ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ac60f-144">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="ac60f-145">Stringa in formato GUID, ad esempio 00000000-0000-0000-0000-0000-000000000000000.</span><span class="sxs-lookup"><span data-stu-id="ac60f-145">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="ac60f-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac60f-146">RELATED LINKS</span></span>

