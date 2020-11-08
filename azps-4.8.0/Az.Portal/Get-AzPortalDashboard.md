---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/get-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
ms.openlocfilehash: aa11a9828c422069823226b2d5df57efc84f8c7b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192240"
---
# <span data-ttu-id="f6dd1-101">Get-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="f6dd1-101">Get-AzPortalDashboard</span></span>

## <span data-ttu-id="f6dd1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f6dd1-102">SYNOPSIS</span></span>
<span data-ttu-id="f6dd1-103">Ottiene il dashboard.</span><span class="sxs-lookup"><span data-stu-id="f6dd1-103">Gets the Dashboard.</span></span>

## <span data-ttu-id="f6dd1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f6dd1-104">SYNTAX</span></span>

### <span data-ttu-id="f6dd1-105">List1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f6dd1-105">List1 (Default)</span></span>
```
Get-AzPortalDashboard [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f6dd1-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="f6dd1-106">Get</span></span>
```
Get-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f6dd1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f6dd1-107">GetViaIdentity</span></span>
```
Get-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f6dd1-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="f6dd1-108">List</span></span>
```
Get-AzPortalDashboard -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6dd1-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6dd1-109">DESCRIPTION</span></span>
<span data-ttu-id="f6dd1-110">Ottiene il dashboard.</span><span class="sxs-lookup"><span data-stu-id="f6dd1-110">Gets the Dashboard.</span></span>

## <span data-ttu-id="f6dd1-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f6dd1-111">EXAMPLES</span></span>

### <span data-ttu-id="f6dd1-112">Esempio 1: elencare tutti i dashboard in una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="f6dd1-112">Example 1: List all dashboards in a subscription</span></span>
```powershell
PS C:> Get-AzPortalDashboard                                                                                                                     
Location Name                                           Type
-------- ----                                           ----
eastasia my-custom-dashboard1                           Microsoft.Portal/dashboards
westus   my-second-custom-dashboard1                    Microsoft.Portal/dashboards

```

<span data-ttu-id="f6dd1-113">Elencare tutti i dashboard in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="f6dd1-113">List all dashboards in a subscription</span></span>

### <span data-ttu-id="f6dd1-114">Esempio 2: ottenere informazioni dettagliate su un singolo dashboard del portale</span><span class="sxs-lookup"><span data-stu-id="f6dd1-114">Example 2: Get details for a single Portal Dashboard</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name mydashboard

Location Name        Type
-------- ----        ----
eastus   mydashboard Microsoft.Portal/dashboards
```

<span data-ttu-id="f6dd1-115">Ottenere informazioni dettagliate su un singolo dashboard</span><span class="sxs-lookup"><span data-stu-id="f6dd1-115">Get details for a single dashboard</span></span>

## <span data-ttu-id="f6dd1-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f6dd1-116">PARAMETERS</span></span>

### <span data-ttu-id="f6dd1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6dd1-117">-DefaultProfile</span></span>
<span data-ttu-id="f6dd1-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f6dd1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6dd1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6dd1-119">-InputObject</span></span>
<span data-ttu-id="f6dd1-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f6dd1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f6dd1-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6dd1-121">-Name</span></span>
<span data-ttu-id="f6dd1-122">Nome del dashboard.</span><span class="sxs-lookup"><span data-stu-id="f6dd1-122">The name of the dashboard.</span></span>

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

### <span data-ttu-id="f6dd1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6dd1-123">-ResourceGroupName</span></span>
<span data-ttu-id="f6dd1-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f6dd1-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="f6dd1-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f6dd1-125">-SubscriptionId</span></span>
<span data-ttu-id="f6dd1-126">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="f6dd1-126">The Azure subscription ID.</span></span>
<span data-ttu-id="f6dd1-127">Si tratta di una stringa formattata con GUID (ad esempio 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="f6dd1-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="f6dd1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6dd1-128">CommonParameters</span></span>
<span data-ttu-id="f6dd1-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6dd1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6dd1-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6dd1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6dd1-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f6dd1-131">INPUTS</span></span>

### <span data-ttu-id="f6dd1-132">Microsoft. Azure. PowerShell. Cmdlets. Portal. Models. IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="f6dd1-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="f6dd1-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f6dd1-133">OUTPUTS</span></span>

### <span data-ttu-id="f6dd1-134">Microsoft. Azure. PowerShell. Cmdlets. Portal. Models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="f6dd1-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="f6dd1-135">Note</span><span class="sxs-lookup"><span data-stu-id="f6dd1-135">NOTES</span></span>

<span data-ttu-id="f6dd1-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f6dd1-136">ALIASES</span></span>

<span data-ttu-id="f6dd1-137">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f6dd1-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f6dd1-138">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="f6dd1-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f6dd1-139">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f6dd1-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f6dd1-140">INPUTOBJECT <IPortalIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="f6dd1-140">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f6dd1-141">`[DashboardName <String>]`: Nome del dashboard.</span><span class="sxs-lookup"><span data-stu-id="f6dd1-141">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="f6dd1-142">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="f6dd1-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f6dd1-143">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f6dd1-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="f6dd1-144">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="f6dd1-144">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="f6dd1-145">Si tratta di una stringa formattata con GUID (ad esempio 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="f6dd1-145">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="f6dd1-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f6dd1-146">RELATED LINKS</span></span>
