---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/remove-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: fe7c391b8f15e3389a9d61070b8f55d47af6d6ec
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861674"
---
# <span data-ttu-id="6ab58-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="6ab58-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="6ab58-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ab58-102">SYNOPSIS</span></span>
<span data-ttu-id="6ab58-103">Eliminare una quota per nome.</span><span class="sxs-lookup"><span data-stu-id="6ab58-103">Delete a quota by name.</span></span>

## <span data-ttu-id="6ab58-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ab58-104">SYNTAX</span></span>

### <span data-ttu-id="6ab58-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6ab58-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6ab58-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6ab58-106">DeleteViaIdentity</span></span>
```
Remove-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6ab58-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ab58-107">DESCRIPTION</span></span>
<span data-ttu-id="6ab58-108">Eliminare una quota per nome.</span><span class="sxs-lookup"><span data-stu-id="6ab58-108">Delete a quota by name.</span></span>

## <span data-ttu-id="6ab58-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ab58-109">EXAMPLES</span></span>

### <span data-ttu-id="6ab58-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6ab58-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="6ab58-111">Rimuovere una quota di rete per nome.</span><span class="sxs-lookup"><span data-stu-id="6ab58-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="6ab58-112">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="6ab58-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="6ab58-113">Rimuovere una quota di rete usando una pipe.</span><span class="sxs-lookup"><span data-stu-id="6ab58-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="6ab58-114">--------------------------ESEMPIO 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="6ab58-114">-------------------------- EXAMPLE 3 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="6ab58-115">Rimuovere una quota di rete.</span><span class="sxs-lookup"><span data-stu-id="6ab58-115">Remove a network quota.</span></span>

## <span data-ttu-id="6ab58-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ab58-116">PARAMETERS</span></span>

### <span data-ttu-id="6ab58-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ab58-117">-AsJob</span></span>
<span data-ttu-id="6ab58-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="6ab58-118">Run the command as a job</span></span>

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

### <span data-ttu-id="6ab58-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ab58-119">-DefaultProfile</span></span>
<span data-ttu-id="6ab58-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab58-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ab58-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ab58-121">-InputObject</span></span>
<span data-ttu-id="6ab58-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="6ab58-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="6ab58-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6ab58-123">-Location</span></span>
<span data-ttu-id="6ab58-124">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6ab58-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6ab58-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ab58-125">-Name</span></span>
<span data-ttu-id="6ab58-126">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6ab58-126">Name of the resource.</span></span>

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

### <span data-ttu-id="6ab58-127">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="6ab58-127">-NoWait</span></span>
<span data-ttu-id="6ab58-128">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="6ab58-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6ab58-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ab58-129">-PassThru</span></span>
<span data-ttu-id="6ab58-130">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="6ab58-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6ab58-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6ab58-131">-SubscriptionId</span></span>
<span data-ttu-id="6ab58-132">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab58-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6ab58-133">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="6ab58-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6ab58-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6ab58-134">-Confirm</span></span>
<span data-ttu-id="6ab58-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ab58-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ab58-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ab58-136">-WhatIf</span></span>
<span data-ttu-id="6ab58-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ab58-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ab58-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ab58-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ab58-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ab58-139">CommonParameters</span></span>
<span data-ttu-id="6ab58-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ab58-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ab58-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ab58-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ab58-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ab58-142">INPUTS</span></span>

### <span data-ttu-id="6ab58-143">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="6ab58-143">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="6ab58-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ab58-144">OUTPUTS</span></span>

### <span data-ttu-id="6ab58-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6ab58-145">System.Boolean</span></span>



## <span data-ttu-id="6ab58-146">Note</span><span class="sxs-lookup"><span data-stu-id="6ab58-146">NOTES</span></span>

<span data-ttu-id="6ab58-147">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="6ab58-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6ab58-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6ab58-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="6ab58-149">INPUTOBJECT <INetworkAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="6ab58-149">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6ab58-150">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="6ab58-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6ab58-151">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6ab58-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="6ab58-152">`[ResourceName <String>]`: Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6ab58-152">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="6ab58-153">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab58-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6ab58-154">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="6ab58-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6ab58-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ab58-155">RELATED LINKS</span></span>

