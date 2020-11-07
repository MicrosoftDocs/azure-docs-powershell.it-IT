---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/resume-azsupdaterun
schema: 2.0.0
ms.openlocfilehash: 65d2b3a045d38435cdd709d47c0be88f7fc98af0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860101"
---
# <span data-ttu-id="8c28f-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="8c28f-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="8c28f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8c28f-102">SYNOPSIS</span></span>
<span data-ttu-id="8c28f-103">Riprendere un aggiornamento non riuscito.</span><span class="sxs-lookup"><span data-stu-id="8c28f-103">Resume a failed update.</span></span>

## <span data-ttu-id="8c28f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c28f-104">SYNTAX</span></span>

### <span data-ttu-id="8c28f-105">Rieseguire (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8c28f-105">Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8c28f-106">RerunViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8c28f-106">RerunViaIdentity</span></span>
```
Resume-AzsUpdateRun -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8c28f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c28f-107">DESCRIPTION</span></span>
<span data-ttu-id="8c28f-108">Riprendere un aggiornamento non riuscito.</span><span class="sxs-lookup"><span data-stu-id="8c28f-108">Resume a failed update.</span></span>

## <span data-ttu-id="8c28f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c28f-109">EXAMPLES</span></span>

### <span data-ttu-id="8c28f-110">Esempio 1: Resume-AzsUpdateRun per nome e UpdateName</span><span class="sxs-lookup"><span data-stu-id="8c28f-110">Example 1: Resume-AzsUpdateRun By Name and UpdateName</span></span>
```powershell
PS C:\> Resume-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10 -Name 45aaeb26-805b-495b-9c8c-d5da5542dbf4

```

<span data-ttu-id="8c28f-111">Unifiedgroup consente di eseguire nuovamente una specifica operazione di aggiornamento non riuscita.</span><span class="sxs-lookup"><span data-stu-id="8c28f-111">Commandlet allows you to rerun a specific failed update run.</span></span>
<span data-ttu-id="8c28f-112">Tieni presente che è necessario che la versione dell'aggiornamento sia strettamente superiore alla versione corrente.</span><span class="sxs-lookup"><span data-stu-id="8c28f-112">Note that there is a requirement that the update version is strictly greater than the current version.</span></span>

## <span data-ttu-id="8c28f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8c28f-113">PARAMETERS</span></span>

### <span data-ttu-id="8c28f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c28f-114">-DefaultProfile</span></span>
<span data-ttu-id="8c28f-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8c28f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c28f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c28f-116">-InputObject</span></span>
<span data-ttu-id="8c28f-117">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="8c28f-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: RerunViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8c28f-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8c28f-118">-Location</span></span>
<span data-ttu-id="8c28f-119">Il nome del percorso di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="8c28f-119">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c28f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8c28f-120">-Name</span></span>
<span data-ttu-id="8c28f-121">Identificatore esecuzione aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="8c28f-121">Update run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c28f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c28f-122">-PassThru</span></span>
<span data-ttu-id="8c28f-123">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="8c28f-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8c28f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c28f-124">-ResourceGroupName</span></span>
<span data-ttu-id="8c28f-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8c28f-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c28f-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8c28f-126">-SubscriptionId</span></span>
<span data-ttu-id="8c28f-127">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8c28f-127">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8c28f-128">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="8c28f-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c28f-129">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="8c28f-129">-UpdateName</span></span>
<span data-ttu-id="8c28f-130">Nome dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="8c28f-130">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c28f-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8c28f-131">-Confirm</span></span>
<span data-ttu-id="8c28f-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c28f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c28f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c28f-133">-WhatIf</span></span>
<span data-ttu-id="8c28f-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8c28f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c28f-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8c28f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c28f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c28f-136">CommonParameters</span></span>
<span data-ttu-id="8c28f-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c28f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c28f-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c28f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c28f-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8c28f-139">INPUTS</span></span>

### <span data-ttu-id="8c28f-140">Microsoft. Azure. PowerShell. Cmdlets. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="8c28f-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="8c28f-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c28f-141">OUTPUTS</span></span>

### <span data-ttu-id="8c28f-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8c28f-142">System.Boolean</span></span>



## <span data-ttu-id="8c28f-143">Note</span><span class="sxs-lookup"><span data-stu-id="8c28f-143">NOTES</span></span>

<span data-ttu-id="8c28f-144">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="8c28f-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8c28f-145">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8c28f-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8c28f-146">INPUTOBJECT <IUpdateAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="8c28f-146">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8c28f-147">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="8c28f-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8c28f-148">`[ResourceGroupName <String>]`: Nome gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="8c28f-148">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="8c28f-149">`[RunName <String>]`: Identificatore esecuzione aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="8c28f-149">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="8c28f-150">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8c28f-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="8c28f-151">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="8c28f-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="8c28f-152">`[UpdateLocation <String>]`: Nome del percorso di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="8c28f-152">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="8c28f-153">`[UpdateName <String>]`: Nome dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="8c28f-153">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="8c28f-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c28f-154">RELATED LINKS</span></span>

