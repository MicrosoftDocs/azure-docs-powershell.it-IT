---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/remove-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
ms.openlocfilehash: f0ef681f09caf43ac2f2100d1a30af19b1b3c364
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179166"
---
# <span data-ttu-id="6c2b3-101">Remove-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="6c2b3-101">Remove-AzPortalDashboard</span></span>

## <span data-ttu-id="6c2b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c2b3-102">SYNOPSIS</span></span>
<span data-ttu-id="6c2b3-103">Elimina il dashboard.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-103">Deletes the Dashboard.</span></span>

## <span data-ttu-id="6c2b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c2b3-104">SYNTAX</span></span>

### <span data-ttu-id="6c2b3-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6c2b3-105">Delete (Default)</span></span>
```
Remove-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6c2b3-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6c2b3-106">DeleteViaIdentity</span></span>
```
Remove-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6c2b3-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6c2b3-107">DESCRIPTION</span></span>
<span data-ttu-id="6c2b3-108">Elimina il dashboard.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-108">Deletes the Dashboard.</span></span>

## <span data-ttu-id="6c2b3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c2b3-109">EXAMPLES</span></span>

### <span data-ttu-id="6c2b3-110">Esempio 1: Rimuovere un dashboard</span><span class="sxs-lookup"><span data-stu-id="6c2b3-110">Example 1: Remove a Dashboard</span></span>
```powershell
PS C:\td\> Remove-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02
```

<span data-ttu-id="6c2b3-111">Rimuovere un trattino usando il nome del gruppo di risorse e il nome del dashboard.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-111">Remove a Dashbaord using resource group name and dashboard name.</span></span>

### <span data-ttu-id="6c2b3-112">Esempio 2: Rimuovere un dashboard usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="6c2b3-112">Example 2: Remove a Dashboard using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02 | Remove-AzPortalDashboard
```

<span data-ttu-id="6c2b3-113">Rimuovi il dashboard restituito da una Get-AzDashboard chiamata.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-113">Remove the dashboard returned from a Get-AzDashboard call.</span></span>

## <span data-ttu-id="6c2b3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c2b3-114">PARAMETERS</span></span>

### <span data-ttu-id="6c2b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c2b3-115">-DefaultProfile</span></span>
<span data-ttu-id="6c2b3-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c2b3-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c2b3-117">-InputObject</span></span>
<span data-ttu-id="6c2b3-118">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6c2b3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6c2b3-119">-Name</span></span>
<span data-ttu-id="6c2b3-120">Nome del dashboard.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-120">The name of the dashboard.</span></span>

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

### <span data-ttu-id="6c2b3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c2b3-121">-PassThru</span></span>
<span data-ttu-id="6c2b3-122">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="6c2b3-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6c2b3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c2b3-123">-ResourceGroupName</span></span>
<span data-ttu-id="6c2b3-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="6c2b3-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6c2b3-125">-SubscriptionId</span></span>
<span data-ttu-id="6c2b3-126">ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-126">The Azure subscription ID.</span></span>
<span data-ttu-id="6c2b3-127">Stringa in formato GUID, ad esempio 00000000-0000-0000-0000-0000-00000000000000</span><span class="sxs-lookup"><span data-stu-id="6c2b3-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="6c2b3-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c2b3-128">-Confirm</span></span>
<span data-ttu-id="6c2b3-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c2b3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c2b3-130">-WhatIf</span></span>
<span data-ttu-id="6c2b3-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c2b3-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c2b3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c2b3-133">CommonParameters</span></span>
<span data-ttu-id="6c2b3-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c2b3-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c2b3-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="6c2b3-136">INPUTS</span></span>

### <span data-ttu-id="6c2b3-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="6c2b3-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="6c2b3-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c2b3-138">OUTPUTS</span></span>

### <span data-ttu-id="6c2b3-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6c2b3-139">System.Boolean</span></span>

## <span data-ttu-id="6c2b3-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="6c2b3-140">NOTES</span></span>

<span data-ttu-id="6c2b3-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6c2b3-141">ALIASES</span></span>

<span data-ttu-id="6c2b3-142">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="6c2b3-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6c2b3-143">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6c2b3-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6c2b3-145">INPUTOBJECT <IPortalIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="6c2b3-145">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6c2b3-146">`[DashboardName <String>]`: nome del dashboard.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-146">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="6c2b3-147">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="6c2b3-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6c2b3-148">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="6c2b3-149">`[SubscriptionId <String>]`: l'ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="6c2b3-149">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="6c2b3-150">Stringa in formato GUID, ad esempio 00000000-0000-0000-0000-0000-00000000000000</span><span class="sxs-lookup"><span data-stu-id="6c2b3-150">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="6c2b3-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c2b3-151">RELATED LINKS</span></span>

