---
external help file: ''
Module Name: Azs.Gallery.Admin
online version: https://docs.microsoft.com/powershell/module/azs.gallery.admin/remove-azsgalleryitem
schema: 2.0.0
ms.openlocfilehash: c39a6cd64f48a7d8d6657499357daa1dd70fc091
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030412"
---
# <span data-ttu-id="1fd3c-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="1fd3c-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="1fd3c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1fd3c-102">SYNOPSIS</span></span>
<span data-ttu-id="1fd3c-103">Eliminare un elemento della raccolta specifico.</span><span class="sxs-lookup"><span data-stu-id="1fd3c-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="1fd3c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1fd3c-104">SYNTAX</span></span>

### <span data-ttu-id="1fd3c-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1fd3c-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem -Name <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1fd3c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1fd3c-106">DeleteViaIdentity</span></span>
```
Remove-AzsGalleryItem -InputObject <IGalleryIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1fd3c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1fd3c-107">DESCRIPTION</span></span>
<span data-ttu-id="1fd3c-108">Eliminare un elemento della raccolta specifico.</span><span class="sxs-lookup"><span data-stu-id="1fd3c-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="1fd3c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1fd3c-109">EXAMPLES</span></span>

### <span data-ttu-id="1fd3c-110">Esempio 1: Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="1fd3c-110">Example 1: Remove-AzsGalleryItem</span></span>
```powershell
PS C:\> Remove-AzsGalleryItem -Name TestUbuntu.Test.1.0.0

```

<span data-ttu-id="1fd3c-111">Elimina TestUbuntu. test. 1.0.0 dalla raccolta stack di Azure.</span><span class="sxs-lookup"><span data-stu-id="1fd3c-111">Deletes TestUbuntu.Test.1.0.0 from Azure Stack gallery.</span></span>

### <span data-ttu-id="1fd3c-112">Esempio 2: Remove-AzsGalleryItem tramite pipeline</span><span class="sxs-lookup"><span data-stu-id="1fd3c-112">Example 2: Remove-AzsGalleryItem through pipeline</span></span>
```powershell
PS C:\> Get-AzsGalleryItem -Name TestUbuntu.Test.1.0.0 | Remove-AzsGalleryItem

```

<span data-ttu-id="1fd3c-113">Elimina TestUbuntu. test. 1.0.0 tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="1fd3c-113">Deletes TestUbuntu.Test.1.0.0 through pipeline.</span></span>

## <span data-ttu-id="1fd3c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1fd3c-114">PARAMETERS</span></span>

### <span data-ttu-id="1fd3c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fd3c-115">-DefaultProfile</span></span>
<span data-ttu-id="1fd3c-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1fd3c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fd3c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fd3c-117">-InputObject</span></span>
<span data-ttu-id="1fd3c-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1fd3c-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="1fd3c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="1fd3c-119">-Name</span></span>
<span data-ttu-id="1fd3c-120">Identità dell'elemento della raccolta.</span><span class="sxs-lookup"><span data-stu-id="1fd3c-120">Identity of the gallery item.</span></span>
<span data-ttu-id="1fd3c-121">Include il nome dell'autore, il nome dell'elemento e può includere la versione separata per carattere periodo.</span><span class="sxs-lookup"><span data-stu-id="1fd3c-121">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: GalleryItemName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1fd3c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fd3c-122">-PassThru</span></span>
<span data-ttu-id="1fd3c-123">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="1fd3c-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1fd3c-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1fd3c-124">-SubscriptionId</span></span>
<span data-ttu-id="1fd3c-125">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1fd3c-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1fd3c-126">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="1fd3c-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1fd3c-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1fd3c-127">-Confirm</span></span>
<span data-ttu-id="1fd3c-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fd3c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fd3c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fd3c-129">-WhatIf</span></span>
<span data-ttu-id="1fd3c-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1fd3c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fd3c-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1fd3c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fd3c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fd3c-132">CommonParameters</span></span>
<span data-ttu-id="1fd3c-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fd3c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fd3c-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1fd3c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fd3c-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1fd3c-135">INPUTS</span></span>

### <span data-ttu-id="1fd3c-136">Microsoft. Azure. PowerShell. Cmdlets. gallery. Models. IGalleryIdentity</span><span class="sxs-lookup"><span data-stu-id="1fd3c-136">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity</span></span>

## <span data-ttu-id="1fd3c-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1fd3c-137">OUTPUTS</span></span>

### <span data-ttu-id="1fd3c-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1fd3c-138">System.Boolean</span></span>



## <span data-ttu-id="1fd3c-139">Note</span><span class="sxs-lookup"><span data-stu-id="1fd3c-139">NOTES</span></span>

<span data-ttu-id="1fd3c-140">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="1fd3c-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1fd3c-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1fd3c-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1fd3c-142">INPUTOBJECT <IGalleryIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="1fd3c-142">INPUTOBJECT <IGalleryIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1fd3c-143">`[GalleryItemName <String>]`: Identità dell'elemento della raccolta.</span><span class="sxs-lookup"><span data-stu-id="1fd3c-143">`[GalleryItemName <String>]`: Identity of the gallery item.</span></span> <span data-ttu-id="1fd3c-144">Include il nome dell'autore, il nome dell'elemento e può includere la versione separata per carattere periodo.</span><span class="sxs-lookup"><span data-stu-id="1fd3c-144">Includes publisher name, item name, and may include version separated by period character.</span></span>
  - <span data-ttu-id="1fd3c-145">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="1fd3c-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1fd3c-146">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1fd3c-146">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1fd3c-147">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="1fd3c-147">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1fd3c-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1fd3c-148">RELATED LINKS</span></span>

