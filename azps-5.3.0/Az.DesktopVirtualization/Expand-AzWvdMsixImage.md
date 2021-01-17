---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/expand-azwvdmsiximage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
ms.openlocfilehash: 56122e8d1ae94b6a898c073f2b2f2fb891504789
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387309"
---
# <span data-ttu-id="83ab4-101">Expand-AzWvdMsixImage</span><span class="sxs-lookup"><span data-stu-id="83ab4-101">Expand-AzWvdMsixImage</span></span>

## <span data-ttu-id="83ab4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="83ab4-102">SYNOPSIS</span></span>
<span data-ttu-id="83ab4-103">Espande ed elenca i pacchetti di MSIX in un'immagine, in base al percorso dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="83ab4-103">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="83ab4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83ab4-104">SYNTAX</span></span>

### <span data-ttu-id="83ab4-105">ExpandExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="83ab4-105">ExpandExpanded (Default)</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Uri <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="83ab4-106">Espandere</span><span class="sxs-lookup"><span data-stu-id="83ab4-106">Expand</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> -MsixImageUri <IMsixImageUri>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="83ab4-107">ExpandViaIdentity</span><span class="sxs-lookup"><span data-stu-id="83ab4-107">ExpandViaIdentity</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> -MsixImageUri <IMsixImageUri>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="83ab4-108">ExpandViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="83ab4-108">ExpandViaIdentityExpanded</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> [-Uri <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="83ab4-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83ab4-109">DESCRIPTION</span></span>
<span data-ttu-id="83ab4-110">Espande ed elenca i pacchetti di MSIX in un'immagine, in base al percorso dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="83ab4-110">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="83ab4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83ab4-111">EXAMPLES</span></span>

### <span data-ttu-id="83ab4-112">Esempio 1: espande il percorso dell'immagine specificato e recupera i metadati del pacchetto trovati in AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="83ab4-112">Example 1: Expands specified Image Path and retrieves Package metadata found in AppxManifest.xml</span></span>
```powershell
PS C:\> Expand-AzWvdMsixImage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
          -Uri ImagePathURI

Name                          Type
----                          ----
HostPoolName/extractmsiximage Microsoft.DesktopVirtualization/hostpools/extractmsiximage
```

<span data-ttu-id="83ab4-113">Questo comando restituisce i metadati del pacchetto MSIX trovato nel percorso dell'immagine specificato.</span><span class="sxs-lookup"><span data-stu-id="83ab4-113">This command returns Metadata of MSIX Package found in the given Image Path.</span></span>

## <span data-ttu-id="83ab4-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83ab4-114">PARAMETERS</span></span>

### <span data-ttu-id="83ab4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83ab4-115">-DefaultProfile</span></span>
<span data-ttu-id="83ab4-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83ab4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83ab4-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="83ab4-117">-HostPoolName</span></span>
<span data-ttu-id="83ab4-118">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="83ab4-118">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ab4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83ab4-119">-InputObject</span></span>
<span data-ttu-id="83ab4-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="83ab4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: ExpandViaIdentity, ExpandViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83ab4-121">-MsixImageUri</span><span class="sxs-lookup"><span data-stu-id="83ab4-121">-MsixImageUri</span></span>
<span data-ttu-id="83ab4-122">Rappresenta l'URI che fa riferimento all'immagine MSIX da costruire, vedi la sezione Note per le proprietà di MSIXIMAGEURI e crea una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="83ab4-122">Represents URI referring to MSIX Image To construct, see NOTES section for MSIXIMAGEURI properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri
Parameter Sets: Expand, ExpandViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83ab4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83ab4-123">-ResourceGroupName</span></span>
<span data-ttu-id="83ab4-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="83ab4-124">The name of the resource group.</span></span>
<span data-ttu-id="83ab4-125">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="83ab4-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ab4-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83ab4-126">-SubscriptionId</span></span>
<span data-ttu-id="83ab4-127">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="83ab4-127">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ab4-128">-URI</span><span class="sxs-lookup"><span data-stu-id="83ab4-128">-Uri</span></span>
<span data-ttu-id="83ab4-129">URI per l'immagine</span><span class="sxs-lookup"><span data-stu-id="83ab4-129">URI to Image</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandExpanded, ExpandViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ab4-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="83ab4-130">-Confirm</span></span>
<span data-ttu-id="83ab4-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83ab4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83ab4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83ab4-132">-WhatIf</span></span>
<span data-ttu-id="83ab4-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83ab4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83ab4-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83ab4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83ab4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83ab4-135">CommonParameters</span></span>
<span data-ttu-id="83ab4-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83ab4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83ab4-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83ab4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83ab4-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="83ab4-138">INPUTS</span></span>

### <span data-ttu-id="83ab4-139">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20201102Preview. IMsixImageUri</span><span class="sxs-lookup"><span data-stu-id="83ab4-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri</span></span>

### <span data-ttu-id="83ab4-140">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="83ab4-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="83ab4-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83ab4-141">OUTPUTS</span></span>

### <span data-ttu-id="83ab4-142">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20201102Preview. IExpandMsixImage</span><span class="sxs-lookup"><span data-stu-id="83ab4-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage</span></span>

## <span data-ttu-id="83ab4-143">Note</span><span class="sxs-lookup"><span data-stu-id="83ab4-143">NOTES</span></span>

<span data-ttu-id="83ab4-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="83ab4-144">ALIASES</span></span>

<span data-ttu-id="83ab4-145">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83ab4-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="83ab4-146">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="83ab4-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="83ab4-147">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="83ab4-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="83ab4-148">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="83ab4-148">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="83ab4-149">`[ApplicationGroupName <String>]`: Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="83ab4-149">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="83ab4-150">`[ApplicationName <String>]`: Nome dell'applicazione nel gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="83ab4-150">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="83ab4-151">`[DesktopName <String>]`: Nome del desktop nel gruppo desktop specificato</span><span class="sxs-lookup"><span data-stu-id="83ab4-151">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="83ab4-152">`[HostPoolName <String>]`: Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="83ab4-152">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="83ab4-153">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="83ab4-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="83ab4-154">`[MsixPackageFullName <String>]`: Pacchetto specifico della versione nome completo del pacchetto MSIX all'interno di hostpool specificato</span><span class="sxs-lookup"><span data-stu-id="83ab4-154">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="83ab4-155">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="83ab4-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="83ab4-156">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="83ab4-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="83ab4-157">`[SessionHostName <String>]`: Nome dell'host di sessione nel pool di host specificato</span><span class="sxs-lookup"><span data-stu-id="83ab4-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="83ab4-158">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="83ab4-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="83ab4-159">`[UserSessionId <String>]`: Nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="83ab4-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="83ab4-160">`[WorkspaceName <String>]`: Nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="83ab4-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

<span data-ttu-id="83ab4-161">MSIXIMAGEURI <IMsixImageUri> : rappresenta l'URI che fa riferimento all'immagine di MSIX</span><span class="sxs-lookup"><span data-stu-id="83ab4-161">MSIXIMAGEURI <IMsixImageUri>: Represents URI referring to MSIX Image</span></span>
  - <span data-ttu-id="83ab4-162">`[Uri <String>]`: URI per l'immagine</span><span class="sxs-lookup"><span data-stu-id="83ab4-162">`[Uri <String>]`: URI to Image</span></span>

## <span data-ttu-id="83ab4-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83ab4-163">RELATED LINKS</span></span>

