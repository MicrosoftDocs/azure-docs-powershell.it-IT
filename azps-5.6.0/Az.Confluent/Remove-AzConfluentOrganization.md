---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/remove-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Remove-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Remove-AzConfluentOrganization.md
ms.openlocfilehash: d35de003bd4822758fd75c7dbbcf616ebecbbccb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012557"
---
# <span data-ttu-id="fa1c3-101">Remove-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="fa1c3-101">Remove-AzConfluentOrganization</span></span>

## <span data-ttu-id="fa1c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa1c3-102">SYNOPSIS</span></span>
<span data-ttu-id="fa1c3-103">Elimina risorsa organizzazione</span><span class="sxs-lookup"><span data-stu-id="fa1c3-103">Delete Organization resource</span></span>

## <span data-ttu-id="fa1c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fa1c3-104">SYNTAX</span></span>

### <span data-ttu-id="fa1c3-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fa1c3-105">Delete (Default)</span></span>
```
Remove-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fa1c3-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fa1c3-106">DeleteViaIdentity</span></span>
```
Remove-AzConfluentOrganization -InputObject <IConfluentIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fa1c3-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fa1c3-107">DESCRIPTION</span></span>
<span data-ttu-id="fa1c3-108">Elimina risorsa organizzazione</span><span class="sxs-lookup"><span data-stu-id="fa1c3-108">Delete Organization resource</span></span>

## <span data-ttu-id="fa1c3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fa1c3-109">EXAMPLES</span></span>

### <span data-ttu-id="fa1c3-110">Esempio 1: Rimuovere un'organizzazione confluente in base al nome</span><span class="sxs-lookup"><span data-stu-id="fa1c3-110">Example 1: Remove a confluent organization by name</span></span>
```powershell
PS C:\> Remove-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-01-portal

```

<span data-ttu-id="fa1c3-111">Questo comando rimuove un'organizzazione confluente in base al nome</span><span class="sxs-lookup"><span data-stu-id="fa1c3-111">This command removes a confluent organization by name</span></span>

### <span data-ttu-id="fa1c3-112">Esempio 2: Rimuovere un'organizzazione confluente tramite pipeline</span><span class="sxs-lookup"><span data-stu-id="fa1c3-112">Example 2: Remove a confluent organization by pipeline</span></span>
```powershell
PS C:\>  Get-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh | Remove-AzConfluentOrganization

```

<span data-ttu-id="fa1c3-113">Questo comando rimuove un'organizzazione confluente tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="fa1c3-113">This command removes a confluent organization by pipeline.</span></span>

## <span data-ttu-id="fa1c3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa1c3-114">PARAMETERS</span></span>

### <span data-ttu-id="fa1c3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa1c3-115">-AsJob</span></span>
<span data-ttu-id="fa1c3-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="fa1c3-116">Run the command as a job</span></span>

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

### <span data-ttu-id="fa1c3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa1c3-117">-DefaultProfile</span></span>
<span data-ttu-id="fa1c3-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fa1c3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa1c3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa1c3-119">-InputObject</span></span>
<span data-ttu-id="fa1c3-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="fa1c3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa1c3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fa1c3-121">-Name</span></span>
<span data-ttu-id="fa1c3-122">Nome risorsa organizzazione</span><span class="sxs-lookup"><span data-stu-id="fa1c3-122">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa1c3-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fa1c3-123">-NoWait</span></span>
<span data-ttu-id="fa1c3-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="fa1c3-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fa1c3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa1c3-125">-PassThru</span></span>
<span data-ttu-id="fa1c3-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="fa1c3-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fa1c3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa1c3-127">-ResourceGroupName</span></span>
<span data-ttu-id="fa1c3-128">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fa1c3-128">Resource group name</span></span>

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

### <span data-ttu-id="fa1c3-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fa1c3-129">-SubscriptionId</span></span>
<span data-ttu-id="fa1c3-130">ID sottoscrizione Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="fa1c3-130">Microsoft Azure subscription id</span></span>

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

### <span data-ttu-id="fa1c3-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa1c3-131">-Confirm</span></span>
<span data-ttu-id="fa1c3-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa1c3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa1c3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa1c3-133">-WhatIf</span></span>
<span data-ttu-id="fa1c3-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa1c3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa1c3-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa1c3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa1c3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa1c3-136">CommonParameters</span></span>
<span data-ttu-id="fa1c3-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa1c3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa1c3-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fa1c3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa1c3-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="fa1c3-139">INPUTS</span></span>

### <span data-ttu-id="fa1c3-140">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span><span class="sxs-lookup"><span data-stu-id="fa1c3-140">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span></span>

## <span data-ttu-id="fa1c3-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fa1c3-141">OUTPUTS</span></span>

### <span data-ttu-id="fa1c3-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fa1c3-142">System.Boolean</span></span>

## <span data-ttu-id="fa1c3-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="fa1c3-143">NOTES</span></span>

<span data-ttu-id="fa1c3-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="fa1c3-144">ALIASES</span></span>

<span data-ttu-id="fa1c3-145">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="fa1c3-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fa1c3-146">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="fa1c3-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fa1c3-147">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fa1c3-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fa1c3-148">INPUTOBJECT <IConfluentIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="fa1c3-148">INPUTOBJECT <IConfluentIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fa1c3-149">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="fa1c3-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fa1c3-150">`[OrganizationName <String>]`: nome della risorsa dell'organizzazione</span><span class="sxs-lookup"><span data-stu-id="fa1c3-150">`[OrganizationName <String>]`: Organization resource name</span></span>
  - <span data-ttu-id="fa1c3-151">`[ResourceGroupName <String>]`: nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fa1c3-151">`[ResourceGroupName <String>]`: Resource group name</span></span>
  - <span data-ttu-id="fa1c3-152">`[SubscriptionId <String>]`: ID sottoscrizione Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="fa1c3-152">`[SubscriptionId <String>]`: Microsoft Azure subscription id</span></span>

## <span data-ttu-id="fa1c3-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fa1c3-153">RELATED LINKS</span></span>

