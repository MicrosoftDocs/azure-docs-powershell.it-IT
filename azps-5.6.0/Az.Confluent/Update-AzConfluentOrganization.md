---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/update-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Update-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Update-AzConfluentOrganization.md
ms.openlocfilehash: 7332d3154e87da2d9249dc16e3986efd636b737a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012558"
---
# <span data-ttu-id="16c79-101">Update-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="16c79-101">Update-AzConfluentOrganization</span></span>

## <span data-ttu-id="16c79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16c79-102">SYNOPSIS</span></span>
<span data-ttu-id="16c79-103">Aggiorna risorsa organizzazione</span><span class="sxs-lookup"><span data-stu-id="16c79-103">Update Organization resource</span></span>

## <span data-ttu-id="16c79-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16c79-104">SYNTAX</span></span>

### <span data-ttu-id="16c79-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="16c79-105">UpdateExpanded (Default)</span></span>
```
Update-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="16c79-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="16c79-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConfluentOrganization -InputObject <IConfluentIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="16c79-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="16c79-107">DESCRIPTION</span></span>
<span data-ttu-id="16c79-108">Aggiorna risorsa organizzazione</span><span class="sxs-lookup"><span data-stu-id="16c79-108">Update Organization resource</span></span>

## <span data-ttu-id="16c79-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16c79-109">EXAMPLES</span></span>

### <span data-ttu-id="16c79-110">Esempio 1: Aggiornare un'organizzazione confluente in base al nome</span><span class="sxs-lookup"><span data-stu-id="16c79-110">Example 1: Update a confluent organization by name</span></span>
```powershell
PS C:\> pdate-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Tag @{"key01" = "value01"}

Location Name                 Type
-------- ----                 ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="16c79-111">Questo comando aggiorna un'organizzazione confluente in base al nome.</span><span class="sxs-lookup"><span data-stu-id="16c79-111">This command updates a confluent organization by name.</span></span>

### <span data-ttu-id="16c79-112">Esempio 2: Aggiornare un'organizzazione confluente tramite pipeline</span><span class="sxs-lookup"><span data-stu-id="16c79-112">Example 2: Update a confluent organization by pipeline</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh | Update-AzConfluentOrganization -Tag @{"key01" = "value01"; "key02"="value02"}

Location Name                 Type
-------- ----                 ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="16c79-113">Questo comando aggiorna un'organizzazione confluente tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="16c79-113">This command updates a confluent organization by pipeline.</span></span>

## <span data-ttu-id="16c79-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16c79-114">PARAMETERS</span></span>

### <span data-ttu-id="16c79-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c79-115">-DefaultProfile</span></span>
<span data-ttu-id="16c79-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16c79-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16c79-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16c79-117">-InputObject</span></span>
<span data-ttu-id="16c79-118">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="16c79-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16c79-119">-Name</span><span class="sxs-lookup"><span data-stu-id="16c79-119">-Name</span></span>
<span data-ttu-id="16c79-120">Nome risorsa organizzazione</span><span class="sxs-lookup"><span data-stu-id="16c79-120">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16c79-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16c79-121">-ResourceGroupName</span></span>
<span data-ttu-id="16c79-122">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="16c79-122">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16c79-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="16c79-123">-SubscriptionId</span></span>
<span data-ttu-id="16c79-124">ID sottoscrizione Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="16c79-124">Microsoft Azure subscription id</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16c79-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="16c79-125">-Tag</span></span>
<span data-ttu-id="16c79-126">ARM tag di risorse</span><span class="sxs-lookup"><span data-stu-id="16c79-126">ARM resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16c79-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16c79-127">-Confirm</span></span>
<span data-ttu-id="16c79-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16c79-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16c79-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16c79-129">-WhatIf</span></span>
<span data-ttu-id="16c79-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16c79-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16c79-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16c79-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16c79-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c79-132">CommonParameters</span></span>
<span data-ttu-id="16c79-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16c79-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c79-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="16c79-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c79-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="16c79-135">INPUTS</span></span>

### <span data-ttu-id="16c79-136">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span><span class="sxs-lookup"><span data-stu-id="16c79-136">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span></span>

## <span data-ttu-id="16c79-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16c79-137">OUTPUTS</span></span>

### <span data-ttu-id="16c79-138">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span><span class="sxs-lookup"><span data-stu-id="16c79-138">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span></span>

## <span data-ttu-id="16c79-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="16c79-139">NOTES</span></span>

<span data-ttu-id="16c79-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="16c79-140">ALIASES</span></span>

<span data-ttu-id="16c79-141">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="16c79-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="16c79-142">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="16c79-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="16c79-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="16c79-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="16c79-144">INPUTOBJECT <IConfluentIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="16c79-144">INPUTOBJECT <IConfluentIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="16c79-145">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="16c79-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="16c79-146">`[OrganizationName <String>]`: nome della risorsa dell'organizzazione</span><span class="sxs-lookup"><span data-stu-id="16c79-146">`[OrganizationName <String>]`: Organization resource name</span></span>
  - <span data-ttu-id="16c79-147">`[ResourceGroupName <String>]`: nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="16c79-147">`[ResourceGroupName <String>]`: Resource group name</span></span>
  - <span data-ttu-id="16c79-148">`[SubscriptionId <String>]`: ID sottoscrizione Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="16c79-148">`[SubscriptionId <String>]`: Microsoft Azure subscription id</span></span>

## <span data-ttu-id="16c79-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16c79-149">RELATED LINKS</span></span>

