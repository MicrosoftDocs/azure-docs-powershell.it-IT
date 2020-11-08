---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: ae4fc80c54aedf7f35ebfc6c0c5f16bb2e5028ee
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030189"
---
# <span data-ttu-id="c2f05-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="c2f05-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="c2f05-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2f05-102">SYNOPSIS</span></span>
<span data-ttu-id="c2f05-103">Eliminare un'immagine della piattaforma</span><span class="sxs-lookup"><span data-stu-id="c2f05-103">Delete a platform image</span></span>

## <span data-ttu-id="c2f05-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2f05-104">SYNTAX</span></span>

### <span data-ttu-id="c2f05-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c2f05-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c2f05-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c2f05-106">DeleteViaIdentity</span></span>
```
Remove-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c2f05-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2f05-107">DESCRIPTION</span></span>
<span data-ttu-id="c2f05-108">Eliminare un'immagine della piattaforma</span><span class="sxs-lookup"><span data-stu-id="c2f05-108">Delete a platform image</span></span>

## <span data-ttu-id="c2f05-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2f05-109">EXAMPLES</span></span>

### <span data-ttu-id="c2f05-110">Esempio 1: rimuovere un'immagine della piattaforma</span><span class="sxs-lookup"><span data-stu-id="c2f05-110">Example 1: Remove a Platform Image</span></span>
```powershell
PS C:\>Remove-AzsPlatformImage -Location northwest -Offer UbuntuServer -Publisher Microsoft -Sku 16.04-LTS -Version 1.0.0
```

<span data-ttu-id="c2f05-111">Una chiamata corretta per rimuovere un'immagine della piattaforma non restituirà alcun output</span><span class="sxs-lookup"><span data-stu-id="c2f05-111">A successful call to remove a platform image will not return any output</span></span>

### <span data-ttu-id="c2f05-112">Esempio 2: rimuovere un'immagine della piattaforma non esiste</span><span class="sxs-lookup"><span data-stu-id="c2f05-112">Example 2: Remove a Platform Image the Does Not Exist</span></span>
```powershell
PS C:\>  Remove-AzsPlatformImage -Location northwest -Offer UbuntuServer -Publisher Microsoft -Sku 16.04-LTS -Version 1.1.6

```

<span data-ttu-id="c2f05-113">Una chiamata corretta per rimuovere un'immagine della piattaforma che non esiste non restituirà alcun output</span><span class="sxs-lookup"><span data-stu-id="c2f05-113">A successful call to remove a platform image that doesn't exist will not return any output</span></span>

## <span data-ttu-id="c2f05-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2f05-114">PARAMETERS</span></span>

### <span data-ttu-id="c2f05-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2f05-115">-DefaultProfile</span></span>
<span data-ttu-id="c2f05-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c2f05-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2f05-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2f05-117">-InputObject</span></span>
<span data-ttu-id="c2f05-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c2f05-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c2f05-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c2f05-119">-Location</span></span>
<span data-ttu-id="c2f05-120">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c2f05-120">Location of the resource.</span></span>

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

### <span data-ttu-id="c2f05-121">-Offerta</span><span class="sxs-lookup"><span data-stu-id="c2f05-121">-Offer</span></span>
<span data-ttu-id="c2f05-122">Nome dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="c2f05-122">Name of the offer.</span></span>

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

### <span data-ttu-id="c2f05-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2f05-123">-PassThru</span></span>
<span data-ttu-id="c2f05-124">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="c2f05-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c2f05-125">-Publisher</span><span class="sxs-lookup"><span data-stu-id="c2f05-125">-Publisher</span></span>
<span data-ttu-id="c2f05-126">Nome dell'autore.</span><span class="sxs-lookup"><span data-stu-id="c2f05-126">Name of the publisher.</span></span>

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

### <span data-ttu-id="c2f05-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="c2f05-127">-Sku</span></span>
<span data-ttu-id="c2f05-128">Nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="c2f05-128">Name of the SKU.</span></span>

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

### <span data-ttu-id="c2f05-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c2f05-129">-SubscriptionId</span></span>
<span data-ttu-id="c2f05-130">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c2f05-130">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c2f05-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="c2f05-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c2f05-132">-Versione</span><span class="sxs-lookup"><span data-stu-id="c2f05-132">-Version</span></span>
<span data-ttu-id="c2f05-133">La versione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c2f05-133">The version of the resource.</span></span>

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

### <span data-ttu-id="c2f05-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c2f05-134">-Confirm</span></span>
<span data-ttu-id="c2f05-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2f05-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2f05-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2f05-136">-WhatIf</span></span>
<span data-ttu-id="c2f05-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2f05-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2f05-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2f05-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2f05-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2f05-139">CommonParameters</span></span>
<span data-ttu-id="c2f05-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2f05-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2f05-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2f05-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2f05-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2f05-142">INPUTS</span></span>

### <span data-ttu-id="c2f05-143">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="c2f05-143">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="c2f05-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2f05-144">OUTPUTS</span></span>

### <span data-ttu-id="c2f05-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2f05-145">System.Boolean</span></span>



## <span data-ttu-id="c2f05-146">Note</span><span class="sxs-lookup"><span data-stu-id="c2f05-146">NOTES</span></span>

<span data-ttu-id="c2f05-147">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="c2f05-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c2f05-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c2f05-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c2f05-149">INPUTOBJECT <IComputeAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="c2f05-149">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c2f05-150">`[DiskId <String>]`: GUID del disco come identità.</span><span class="sxs-lookup"><span data-stu-id="c2f05-150">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="c2f05-151">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="c2f05-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c2f05-152">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c2f05-152">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="c2f05-153">`[MigrationId <String>]`: Nome GUID processo di migrazione.</span><span class="sxs-lookup"><span data-stu-id="c2f05-153">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="c2f05-154">`[Offer <String>]`: Nome dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="c2f05-154">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="c2f05-155">`[Publisher <String>]`: Nome del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="c2f05-155">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="c2f05-156">`[QuotaName <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="c2f05-156">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="c2f05-157">`[Sku <String>]`: Nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="c2f05-157">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="c2f05-158">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c2f05-158">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c2f05-159">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="c2f05-159">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c2f05-160">`[Type <String>]`: Tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="c2f05-160">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="c2f05-161">`[Version <String>]`: La versione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c2f05-161">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="c2f05-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2f05-162">RELATED LINKS</span></span>

