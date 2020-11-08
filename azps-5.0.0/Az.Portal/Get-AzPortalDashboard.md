---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/get-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
ms.openlocfilehash: aa11a9828c422069823226b2d5df57efc84f8c7b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202645"
---
# <span data-ttu-id="96881-101">Get-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="96881-101">Get-AzPortalDashboard</span></span>

## <span data-ttu-id="96881-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="96881-102">SYNOPSIS</span></span>
<span data-ttu-id="96881-103">Ottiene il dashboard.</span><span class="sxs-lookup"><span data-stu-id="96881-103">Gets the Dashboard.</span></span>

## <span data-ttu-id="96881-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96881-104">SYNTAX</span></span>

### <span data-ttu-id="96881-105">List1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="96881-105">List1 (Default)</span></span>
```
Get-AzPortalDashboard [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="96881-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="96881-106">Get</span></span>
```
Get-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="96881-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="96881-107">GetViaIdentity</span></span>
```
Get-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="96881-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="96881-108">List</span></span>
```
Get-AzPortalDashboard -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="96881-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96881-109">DESCRIPTION</span></span>
<span data-ttu-id="96881-110">Ottiene il dashboard.</span><span class="sxs-lookup"><span data-stu-id="96881-110">Gets the Dashboard.</span></span>

## <span data-ttu-id="96881-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96881-111">EXAMPLES</span></span>

### <span data-ttu-id="96881-112">Esempio 1: elencare tutti i dashboard in una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="96881-112">Example 1: List all dashboards in a subscription</span></span>
```powershell
PS C:> Get-AzPortalDashboard                                                                                                                     
Location Name                                           Type
-------- ----                                           ----
eastasia my-custom-dashboard1                           Microsoft.Portal/dashboards
westus   my-second-custom-dashboard1                    Microsoft.Portal/dashboards

```

<span data-ttu-id="96881-113">Elencare tutti i dashboard in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="96881-113">List all dashboards in a subscription</span></span>

### <span data-ttu-id="96881-114">Esempio 2: ottenere informazioni dettagliate su un singolo dashboard del portale</span><span class="sxs-lookup"><span data-stu-id="96881-114">Example 2: Get details for a single Portal Dashboard</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name mydashboard

Location Name        Type
-------- ----        ----
eastus   mydashboard Microsoft.Portal/dashboards
```

<span data-ttu-id="96881-115">Ottenere informazioni dettagliate su un singolo dashboard</span><span class="sxs-lookup"><span data-stu-id="96881-115">Get details for a single dashboard</span></span>

## <span data-ttu-id="96881-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="96881-116">PARAMETERS</span></span>

### <span data-ttu-id="96881-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96881-117">-DefaultProfile</span></span>
<span data-ttu-id="96881-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="96881-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96881-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96881-119">-InputObject</span></span>
<span data-ttu-id="96881-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="96881-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="96881-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="96881-121">-Name</span></span>
<span data-ttu-id="96881-122">Nome del dashboard.</span><span class="sxs-lookup"><span data-stu-id="96881-122">The name of the dashboard.</span></span>

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

### <span data-ttu-id="96881-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96881-123">-ResourceGroupName</span></span>
<span data-ttu-id="96881-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="96881-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="96881-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="96881-125">-SubscriptionId</span></span>
<span data-ttu-id="96881-126">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="96881-126">The Azure subscription ID.</span></span>
<span data-ttu-id="96881-127">Si tratta di una stringa formattata con GUID (ad esempio 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="96881-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="96881-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96881-128">CommonParameters</span></span>
<span data-ttu-id="96881-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96881-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96881-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96881-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96881-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="96881-131">INPUTS</span></span>

### <span data-ttu-id="96881-132">Microsoft. Azure. PowerShell. Cmdlets. Portal. Models. IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="96881-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="96881-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96881-133">OUTPUTS</span></span>

### <span data-ttu-id="96881-134">Microsoft. Azure. PowerShell. Cmdlets. Portal. Models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="96881-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="96881-135">Note</span><span class="sxs-lookup"><span data-stu-id="96881-135">NOTES</span></span>

<span data-ttu-id="96881-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="96881-136">ALIASES</span></span>

<span data-ttu-id="96881-137">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="96881-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="96881-138">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="96881-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="96881-139">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="96881-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="96881-140">INPUTOBJECT <IPortalIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="96881-140">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="96881-141">`[DashboardName <String>]`: Nome del dashboard.</span><span class="sxs-lookup"><span data-stu-id="96881-141">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="96881-142">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="96881-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="96881-143">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="96881-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="96881-144">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="96881-144">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="96881-145">Si tratta di una stringa formattata con GUID (ad esempio 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="96881-145">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="96881-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96881-146">RELATED LINKS</span></span>

