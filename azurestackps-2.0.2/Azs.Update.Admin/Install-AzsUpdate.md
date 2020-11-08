---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/install-azsupdate
schema: 2.0.0
ms.openlocfilehash: e6fc8ee19443f0861fb867a5e60d0f637642ff62
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030386"
---
# <span data-ttu-id="6ae94-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="6ae94-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="6ae94-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ae94-102">SYNOPSIS</span></span>
<span data-ttu-id="6ae94-103">Applicare un aggiornamento specifico in una posizione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="6ae94-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="6ae94-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ae94-104">SYNTAX</span></span>

### <span data-ttu-id="6ae94-105">Applica (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6ae94-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6ae94-106">ApplyViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6ae94-106">ApplyViaIdentity</span></span>
```
Install-AzsUpdate -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6ae94-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ae94-107">DESCRIPTION</span></span>
<span data-ttu-id="6ae94-108">Applicare un aggiornamento specifico in una posizione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="6ae94-108">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="6ae94-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ae94-109">EXAMPLES</span></span>

### <span data-ttu-id="6ae94-110">Esempio 1: Install-AzsUpdate per nome</span><span class="sxs-lookup"><span data-stu-id="6ae94-110">Example 1: Install-AzsUpdate By Name</span></span>
```powershell
PS C:\> Install-AzsUpdate -Name Microsoft1.1907.0.10
```

<span data-ttu-id="6ae94-111">Unifiedgroup consente di installare aggiornamenti specifici per nome.</span><span class="sxs-lookup"><span data-stu-id="6ae94-111">Commandlet allows you to install specific updates by name.</span></span>
<span data-ttu-id="6ae94-112">Tieni presente che è necessario che la versione dell'aggiornamento sia strettamente superiore alla versione corrente.</span><span class="sxs-lookup"><span data-stu-id="6ae94-112">Note that there is a requirement that the update version is strictly greater than the current version.</span></span>

## <span data-ttu-id="6ae94-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ae94-113">PARAMETERS</span></span>

### <span data-ttu-id="6ae94-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ae94-114">-AsJob</span></span>
<span data-ttu-id="6ae94-115">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="6ae94-115">Run the command as a job</span></span>

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

### <span data-ttu-id="6ae94-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ae94-116">-DefaultProfile</span></span>
<span data-ttu-id="6ae94-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6ae94-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ae94-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ae94-118">-InputObject</span></span>
<span data-ttu-id="6ae94-119">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="6ae94-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: ApplyViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="6ae94-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6ae94-120">-Location</span></span>
<span data-ttu-id="6ae94-121">Il nome del percorso di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="6ae94-121">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6ae94-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ae94-122">-Name</span></span>
<span data-ttu-id="6ae94-123">Nome dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="6ae94-123">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6ae94-124">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="6ae94-124">-NoWait</span></span>
<span data-ttu-id="6ae94-125">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="6ae94-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6ae94-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ae94-126">-ResourceGroupName</span></span>
<span data-ttu-id="6ae94-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6ae94-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6ae94-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6ae94-128">-SubscriptionId</span></span>
<span data-ttu-id="6ae94-129">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6ae94-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6ae94-130">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="6ae94-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6ae94-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6ae94-131">-Confirm</span></span>
<span data-ttu-id="6ae94-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ae94-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ae94-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ae94-133">-WhatIf</span></span>
<span data-ttu-id="6ae94-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ae94-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ae94-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ae94-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ae94-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ae94-136">CommonParameters</span></span>
<span data-ttu-id="6ae94-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ae94-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ae94-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ae94-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ae94-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ae94-139">INPUTS</span></span>

### <span data-ttu-id="6ae94-140">Microsoft. Azure. PowerShell. Cmdlets. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="6ae94-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="6ae94-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ae94-141">OUTPUTS</span></span>

### <span data-ttu-id="6ae94-142">Microsoft. Azure. PowerShell. Cmdlets. UpdateAdmin. Models. Api20160501. IUpdateRun</span><span class="sxs-lookup"><span data-stu-id="6ae94-142">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateRun</span></span>



## <span data-ttu-id="6ae94-143">Note</span><span class="sxs-lookup"><span data-stu-id="6ae94-143">NOTES</span></span>

<span data-ttu-id="6ae94-144">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="6ae94-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6ae94-145">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6ae94-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="6ae94-146">INPUTOBJECT <IUpdateAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="6ae94-146">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6ae94-147">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="6ae94-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6ae94-148">`[ResourceGroupName <String>]`: Nome gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="6ae94-148">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="6ae94-149">`[RunName <String>]`: Identificatore esecuzione aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="6ae94-149">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="6ae94-150">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6ae94-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="6ae94-151">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="6ae94-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="6ae94-152">`[UpdateLocation <String>]`: Nome del percorso di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="6ae94-152">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="6ae94-153">`[UpdateName <String>]`: Nome dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="6ae94-153">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="6ae94-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ae94-154">RELATED LINKS</span></span>

