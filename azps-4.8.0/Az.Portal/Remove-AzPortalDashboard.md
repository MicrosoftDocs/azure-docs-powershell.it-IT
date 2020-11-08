---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/remove-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
ms.openlocfilehash: f0ef681f09caf43ac2f2100d1a30af19b1b3c364
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192237"
---
# <span data-ttu-id="7c70e-101">Remove-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="7c70e-101">Remove-AzPortalDashboard</span></span>

## <span data-ttu-id="7c70e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c70e-102">SYNOPSIS</span></span>
<span data-ttu-id="7c70e-103">Elimina il dashboard.</span><span class="sxs-lookup"><span data-stu-id="7c70e-103">Deletes the Dashboard.</span></span>

## <span data-ttu-id="7c70e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c70e-104">SYNTAX</span></span>

### <span data-ttu-id="7c70e-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7c70e-105">Delete (Default)</span></span>
```
Remove-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7c70e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7c70e-106">DeleteViaIdentity</span></span>
```
Remove-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7c70e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c70e-107">DESCRIPTION</span></span>
<span data-ttu-id="7c70e-108">Elimina il dashboard.</span><span class="sxs-lookup"><span data-stu-id="7c70e-108">Deletes the Dashboard.</span></span>

## <span data-ttu-id="7c70e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c70e-109">EXAMPLES</span></span>

### <span data-ttu-id="7c70e-110">Esempio 1: rimuovere un dashboard</span><span class="sxs-lookup"><span data-stu-id="7c70e-110">Example 1: Remove a Dashboard</span></span>
```powershell
PS C:\td\> Remove-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02
```

<span data-ttu-id="7c70e-111">Rimuovere un Dashbaord usando il nome del gruppo di risorse e il nome del dashboard.</span><span class="sxs-lookup"><span data-stu-id="7c70e-111">Remove a Dashbaord using resource group name and dashboard name.</span></span>

### <span data-ttu-id="7c70e-112">Esempio 2: rimuovere un dashboard usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="7c70e-112">Example 2: Remove a Dashboard using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02 | Remove-AzPortalDashboard
```

<span data-ttu-id="7c70e-113">Rimuovere il dashboard restituito da una chiamata di Get-AzDashboard.</span><span class="sxs-lookup"><span data-stu-id="7c70e-113">Remove the dashboard returned from a Get-AzDashboard call.</span></span>

## <span data-ttu-id="7c70e-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c70e-114">PARAMETERS</span></span>

### <span data-ttu-id="7c70e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c70e-115">-DefaultProfile</span></span>
<span data-ttu-id="7c70e-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c70e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c70e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c70e-117">-InputObject</span></span>
<span data-ttu-id="7c70e-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="7c70e-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c70e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="7c70e-119">-Name</span></span>
<span data-ttu-id="7c70e-120">Nome del dashboard.</span><span class="sxs-lookup"><span data-stu-id="7c70e-120">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c70e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c70e-121">-PassThru</span></span>
<span data-ttu-id="7c70e-122">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="7c70e-122">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c70e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c70e-123">-ResourceGroupName</span></span>
<span data-ttu-id="7c70e-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7c70e-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c70e-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7c70e-125">-SubscriptionId</span></span>
<span data-ttu-id="7c70e-126">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="7c70e-126">The Azure subscription ID.</span></span>
<span data-ttu-id="7c70e-127">Si tratta di una stringa formattata con GUID (ad esempio 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="7c70e-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c70e-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7c70e-128">-Confirm</span></span>
<span data-ttu-id="7c70e-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c70e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c70e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c70e-130">-WhatIf</span></span>
<span data-ttu-id="7c70e-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c70e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c70e-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c70e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c70e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c70e-133">CommonParameters</span></span>
<span data-ttu-id="7c70e-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c70e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c70e-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c70e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c70e-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c70e-136">INPUTS</span></span>

### <span data-ttu-id="7c70e-137">Microsoft. Azure. PowerShell. Cmdlets. Portal. Models. IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="7c70e-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="7c70e-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c70e-138">OUTPUTS</span></span>

### <span data-ttu-id="7c70e-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7c70e-139">System.Boolean</span></span>

## <span data-ttu-id="7c70e-140">Note</span><span class="sxs-lookup"><span data-stu-id="7c70e-140">NOTES</span></span>

<span data-ttu-id="7c70e-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7c70e-141">ALIASES</span></span>

<span data-ttu-id="7c70e-142">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c70e-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7c70e-143">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="7c70e-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7c70e-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7c70e-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7c70e-145">INPUTOBJECT <IPortalIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="7c70e-145">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7c70e-146">`[DashboardName <String>]`: Nome del dashboard.</span><span class="sxs-lookup"><span data-stu-id="7c70e-146">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="7c70e-147">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="7c70e-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7c70e-148">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7c70e-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="7c70e-149">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="7c70e-149">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="7c70e-150">Si tratta di una stringa formattata con GUID (ad esempio 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="7c70e-150">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="7c70e-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c70e-151">RELATED LINKS</span></span>
