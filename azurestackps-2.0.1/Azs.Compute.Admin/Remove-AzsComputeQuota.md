---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 715234586df8383a2983b4f0459ae91ca457d684
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023326"
---
# <span data-ttu-id="5db54-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="5db54-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="5db54-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5db54-102">SYNOPSIS</span></span>
<span data-ttu-id="5db54-103">Eliminare una quota di calcolo esistente.</span><span class="sxs-lookup"><span data-stu-id="5db54-103">Delete an existing Compute quota.</span></span>

## <span data-ttu-id="5db54-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5db54-104">SYNTAX</span></span>

### <span data-ttu-id="5db54-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5db54-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5db54-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5db54-106">DeleteViaIdentity</span></span>
```
Remove-AzsComputeQuota -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5db54-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5db54-107">DESCRIPTION</span></span>
<span data-ttu-id="5db54-108">Eliminare una quota di calcolo esistente.</span><span class="sxs-lookup"><span data-stu-id="5db54-108">Delete an existing Compute quota.</span></span>

## <span data-ttu-id="5db54-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5db54-109">EXAMPLES</span></span>

### <span data-ttu-id="5db54-110">Esempio 1: rimuovere una quota di calcolo</span><span class="sxs-lookup"><span data-stu-id="5db54-110">Example 1: Remove a Compute Quota</span></span>
```powershell
PS C:\> Remove-AzsComputeQuota -Name "AComputeQuota"
```

<span data-ttu-id="5db54-111">Una chiamata corretta per rimuovere una quota di calcolo non restituirà alcun output</span><span class="sxs-lookup"><span data-stu-id="5db54-111">A successful call to remove a compute quota will not return any output</span></span>

## <span data-ttu-id="5db54-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5db54-112">PARAMETERS</span></span>

### <span data-ttu-id="5db54-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5db54-113">-DefaultProfile</span></span>
<span data-ttu-id="5db54-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5db54-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5db54-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5db54-115">-InputObject</span></span>
<span data-ttu-id="5db54-116">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="5db54-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="5db54-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5db54-117">-Location</span></span>
<span data-ttu-id="5db54-118">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5db54-118">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5db54-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="5db54-119">-Name</span></span>
<span data-ttu-id="5db54-120">Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="5db54-120">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5db54-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5db54-121">-PassThru</span></span>
<span data-ttu-id="5db54-122">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="5db54-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5db54-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5db54-123">-SubscriptionId</span></span>
<span data-ttu-id="5db54-124">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5db54-124">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5db54-125">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="5db54-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5db54-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5db54-126">-Confirm</span></span>
<span data-ttu-id="5db54-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5db54-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5db54-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5db54-128">-WhatIf</span></span>
<span data-ttu-id="5db54-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5db54-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5db54-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5db54-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5db54-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5db54-131">CommonParameters</span></span>
<span data-ttu-id="5db54-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5db54-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5db54-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5db54-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5db54-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5db54-134">INPUTS</span></span>

### <span data-ttu-id="5db54-135">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="5db54-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="5db54-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5db54-136">OUTPUTS</span></span>

### <span data-ttu-id="5db54-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5db54-137">System.Boolean</span></span>



## <span data-ttu-id="5db54-138">Note</span><span class="sxs-lookup"><span data-stu-id="5db54-138">NOTES</span></span>

<span data-ttu-id="5db54-139">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="5db54-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5db54-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5db54-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5db54-141">INPUTOBJECT <IComputeAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="5db54-141">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5db54-142">`[DiskId <String>]`: GUID del disco come identità.</span><span class="sxs-lookup"><span data-stu-id="5db54-142">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="5db54-143">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="5db54-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5db54-144">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5db54-144">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="5db54-145">`[MigrationId <String>]`: Nome GUID processo di migrazione.</span><span class="sxs-lookup"><span data-stu-id="5db54-145">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="5db54-146">`[Offer <String>]`: Nome dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="5db54-146">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="5db54-147">`[Publisher <String>]`: Nome del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="5db54-147">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="5db54-148">`[QuotaName <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="5db54-148">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="5db54-149">`[Sku <String>]`: Nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="5db54-149">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="5db54-150">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5db54-150">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5db54-151">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="5db54-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="5db54-152">`[Type <String>]`: Tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="5db54-152">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="5db54-153">`[Version <String>]`: La versione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5db54-153">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="5db54-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5db54-154">RELATED LINKS</span></span>

