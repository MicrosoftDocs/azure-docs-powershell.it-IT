---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azsvmextension
schema: 2.0.0
ms.openlocfilehash: 0b2bca9555b14a391df69acc4abdb2fc8c95017c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93864006"
---
# <span data-ttu-id="36b8f-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="36b8f-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="36b8f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="36b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="36b8f-103">Elimina l'immagine dell'estensione della macchina virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="36b8f-103">Deletes specified Virtual Machine Extension Image.</span></span>

## <span data-ttu-id="36b8f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36b8f-104">SYNTAX</span></span>

### <span data-ttu-id="36b8f-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="36b8f-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="36b8f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="36b8f-106">DeleteViaIdentity</span></span>
```
Remove-AzsVMExtension -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="36b8f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36b8f-107">DESCRIPTION</span></span>
<span data-ttu-id="36b8f-108">Elimina l'immagine dell'estensione della macchina virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="36b8f-108">Deletes specified Virtual Machine Extension Image.</span></span>

## <span data-ttu-id="36b8f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36b8f-109">EXAMPLES</span></span>

### <span data-ttu-id="36b8f-110">Esempio 1: rimuovere un'estensione VM esistente</span><span class="sxs-lookup"><span data-stu-id="36b8f-110">Example 1: Remove a VM Extension that Exists</span></span> 
```powershell
PS C:\> Remove-AzsVMExtension -Location local -Publisher Microsoft -Type MicroExtension -Version 0.1.0
```

<span data-ttu-id="36b8f-111">Una chiamata corretta per rimuovere una quota di calcolo non restituirà alcun output</span><span class="sxs-lookup"><span data-stu-id="36b8f-111">A successful call to remove a compute quota will not return any output</span></span>

### <span data-ttu-id="36b8f-112">Esempio 2: rimuovere un'estensione VM che non esiste</span><span class="sxs-lookup"><span data-stu-id="36b8f-112">Example 2: Remove a VM Extension that Does Not Exist</span></span>
```powershell
PS C:\> Remove-AzsVMExtension -Location local -Publisher Microsoft -Type DoesntExist -Version 9.8.7
```

<span data-ttu-id="36b8f-113">Una chiamata corretta per rimuovere un'immagine della piattaforma che non esiste non restituirà alcun output</span><span class="sxs-lookup"><span data-stu-id="36b8f-113">A successful call to remove a platform image that doesn't exist will not return any output</span></span>

## <span data-ttu-id="36b8f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36b8f-114">PARAMETERS</span></span>

### <span data-ttu-id="36b8f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36b8f-115">-DefaultProfile</span></span>
<span data-ttu-id="36b8f-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36b8f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36b8f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36b8f-117">-InputObject</span></span>
<span data-ttu-id="36b8f-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="36b8f-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="36b8f-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="36b8f-119">-Location</span></span>
<span data-ttu-id="36b8f-120">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="36b8f-120">Location of the resource.</span></span>

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

### <span data-ttu-id="36b8f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36b8f-121">-PassThru</span></span>
<span data-ttu-id="36b8f-122">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="36b8f-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="36b8f-123">-Publisher</span><span class="sxs-lookup"><span data-stu-id="36b8f-123">-Publisher</span></span>
<span data-ttu-id="36b8f-124">Nome dell'autore.</span><span class="sxs-lookup"><span data-stu-id="36b8f-124">Name of the publisher.</span></span>

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

### <span data-ttu-id="36b8f-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="36b8f-125">-SubscriptionId</span></span>
<span data-ttu-id="36b8f-126">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="36b8f-126">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="36b8f-127">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="36b8f-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="36b8f-128">-Digitare</span><span class="sxs-lookup"><span data-stu-id="36b8f-128">-Type</span></span>
<span data-ttu-id="36b8f-129">Tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="36b8f-129">Type of extension.</span></span>

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

### <span data-ttu-id="36b8f-130">-Versione</span><span class="sxs-lookup"><span data-stu-id="36b8f-130">-Version</span></span>
<span data-ttu-id="36b8f-131">La versione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="36b8f-131">The version of the resource.</span></span>

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

### <span data-ttu-id="36b8f-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="36b8f-132">-Confirm</span></span>
<span data-ttu-id="36b8f-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36b8f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36b8f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36b8f-134">-WhatIf</span></span>
<span data-ttu-id="36b8f-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36b8f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36b8f-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36b8f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36b8f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36b8f-137">CommonParameters</span></span>
<span data-ttu-id="36b8f-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36b8f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36b8f-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36b8f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36b8f-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="36b8f-140">INPUTS</span></span>

### <span data-ttu-id="36b8f-141">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="36b8f-141">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="36b8f-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36b8f-142">OUTPUTS</span></span>

### <span data-ttu-id="36b8f-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="36b8f-143">System.Boolean</span></span>



## <span data-ttu-id="36b8f-144">Note</span><span class="sxs-lookup"><span data-stu-id="36b8f-144">NOTES</span></span>

<span data-ttu-id="36b8f-145">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="36b8f-145">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="36b8f-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="36b8f-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="36b8f-147">INPUTOBJECT <IComputeAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="36b8f-147">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="36b8f-148">`[DiskId <String>]`: GUID del disco come identità.</span><span class="sxs-lookup"><span data-stu-id="36b8f-148">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="36b8f-149">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="36b8f-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="36b8f-150">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="36b8f-150">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="36b8f-151">`[MigrationId <String>]`: Nome GUID processo di migrazione.</span><span class="sxs-lookup"><span data-stu-id="36b8f-151">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="36b8f-152">`[Offer <String>]`: Nome dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="36b8f-152">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="36b8f-153">`[Publisher <String>]`: Nome del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="36b8f-153">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="36b8f-154">`[QuotaName <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="36b8f-154">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="36b8f-155">`[Sku <String>]`: Nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="36b8f-155">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="36b8f-156">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="36b8f-156">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="36b8f-157">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="36b8f-157">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="36b8f-158">`[Type <String>]`: Tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="36b8f-158">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="36b8f-159">`[Version <String>]`: La versione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="36b8f-159">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="36b8f-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36b8f-160">RELATED LINKS</span></span>

