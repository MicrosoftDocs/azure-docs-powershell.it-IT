---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/expand-azwvdmsiximage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
ms.openlocfilehash: f4767b87e7230727a2cf9c83af0c2aa5d03b908a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966190"
---
# <span data-ttu-id="f7ed3-101">Expand-AzWvdMsixImage</span><span class="sxs-lookup"><span data-stu-id="f7ed3-101">Expand-AzWvdMsixImage</span></span>

## <span data-ttu-id="f7ed3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7ed3-102">SYNOPSIS</span></span>
<span data-ttu-id="f7ed3-103">Espande ed elenca i pacchetti MSIX in un'immagine, in base al percorso dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="f7ed3-103">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="f7ed3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7ed3-104">SYNTAX</span></span>

### <span data-ttu-id="f7ed3-105">ExpandExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f7ed3-105">ExpandExpanded (Default)</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Uri <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f7ed3-106">Espandi</span><span class="sxs-lookup"><span data-stu-id="f7ed3-106">Expand</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> -MsixImageUri <IMsixImageUri>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f7ed3-107">ExpandViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f7ed3-107">ExpandViaIdentity</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> -MsixImageUri <IMsixImageUri>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f7ed3-108">ExpandViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f7ed3-108">ExpandViaIdentityExpanded</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> [-Uri <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f7ed3-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f7ed3-109">DESCRIPTION</span></span>
<span data-ttu-id="f7ed3-110">Espande ed elenca i pacchetti MSIX in un'immagine, in base al percorso dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="f7ed3-110">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="f7ed3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7ed3-111">EXAMPLES</span></span>

### <span data-ttu-id="f7ed3-112">Esempio 1: espande il percorso immagine specificato e recupera i metadati del pacchetto trovati in AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="f7ed3-112">Example 1: Expands specified Image Path and retrieves Package metadata found in AppxManifest.xml</span></span>
```powershell
PS C:\> Expand-AzWvdMsixImage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
          -Uri ImagePathURI

Name                          Type
----                          ----
HostPoolName/extractmsiximage Microsoft.DesktopVirtualization/hostpools/extractmsiximage
```

<span data-ttu-id="f7ed3-113">Questo comando restituisce i metadati del pacchetto MSIX trovati nel percorso immagine specificato.</span><span class="sxs-lookup"><span data-stu-id="f7ed3-113">This command returns Metadata of MSIX Package found in the given Image Path.</span></span>

## <span data-ttu-id="f7ed3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7ed3-114">PARAMETERS</span></span>

### <span data-ttu-id="f7ed3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7ed3-115">-DefaultProfile</span></span>
<span data-ttu-id="f7ed3-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f7ed3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7ed3-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="f7ed3-117">-HostPoolName</span></span>
<span data-ttu-id="f7ed3-118">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="f7ed3-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="f7ed3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7ed3-119">-InputObject</span></span>
<span data-ttu-id="f7ed3-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f7ed3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f7ed3-121">-MsixImageUri</span><span class="sxs-lookup"><span data-stu-id="f7ed3-121">-MsixImageUri</span></span>
<span data-ttu-id="f7ed3-122">Rappresenta l'URI che fa riferimento al costrutto Immagine MSIX To, vedere la sezione NOTE per le proprietà MSIXIMAGEURI e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f7ed3-122">Represents URI referring to MSIX Image To construct, see NOTES section for MSIXIMAGEURI properties and create a hash table.</span></span>

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

### <span data-ttu-id="f7ed3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7ed3-123">-ResourceGroupName</span></span>
<span data-ttu-id="f7ed3-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f7ed3-124">The name of the resource group.</span></span>
<span data-ttu-id="f7ed3-125">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="f7ed3-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f7ed3-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f7ed3-126">-SubscriptionId</span></span>
<span data-ttu-id="f7ed3-127">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f7ed3-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f7ed3-128">-Uri</span><span class="sxs-lookup"><span data-stu-id="f7ed3-128">-Uri</span></span>
<span data-ttu-id="f7ed3-129">URI in immagine</span><span class="sxs-lookup"><span data-stu-id="f7ed3-129">URI to Image</span></span>

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

### <span data-ttu-id="f7ed3-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7ed3-130">-Confirm</span></span>
<span data-ttu-id="f7ed3-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7ed3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7ed3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7ed3-132">-WhatIf</span></span>
<span data-ttu-id="f7ed3-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7ed3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7ed3-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7ed3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7ed3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7ed3-135">CommonParameters</span></span>
<span data-ttu-id="f7ed3-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7ed3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7ed3-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f7ed3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7ed3-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="f7ed3-138">INPUTS</span></span>

### <span data-ttu-id="f7ed3-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri</span><span class="sxs-lookup"><span data-stu-id="f7ed3-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri</span></span>

### <span data-ttu-id="f7ed3-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="f7ed3-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="f7ed3-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7ed3-141">OUTPUTS</span></span>

### <span data-ttu-id="f7ed3-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage</span><span class="sxs-lookup"><span data-stu-id="f7ed3-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage</span></span>

## <span data-ttu-id="f7ed3-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="f7ed3-143">NOTES</span></span>

<span data-ttu-id="f7ed3-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f7ed3-144">ALIASES</span></span>

<span data-ttu-id="f7ed3-145">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="f7ed3-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f7ed3-146">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="f7ed3-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f7ed3-147">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f7ed3-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f7ed3-148">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="f7ed3-148">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f7ed3-149">`[ApplicationGroupName <String>]`: nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="f7ed3-149">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="f7ed3-150">`[ApplicationName <String>]`: nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="f7ed3-150">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="f7ed3-151">`[DesktopName <String>]`: nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="f7ed3-151">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="f7ed3-152">`[HostPoolName <String>]`: nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="f7ed3-152">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="f7ed3-153">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="f7ed3-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f7ed3-154">`[MsixPackageFullName <String>]`: nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno dello pool host specificato</span><span class="sxs-lookup"><span data-stu-id="f7ed3-154">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="f7ed3-155">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f7ed3-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f7ed3-156">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="f7ed3-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="f7ed3-157">`[SessionHostName <String>]`: nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="f7ed3-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="f7ed3-158">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f7ed3-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f7ed3-159">`[UserSessionId <String>]`: nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="f7ed3-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="f7ed3-160">`[WorkspaceName <String>]`: nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="f7ed3-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

<span data-ttu-id="f7ed3-161">MSIXIMAGEURI: <IMsixImageUri> Rappresenta l'URI che fa riferimento all'immagine MSIX</span><span class="sxs-lookup"><span data-stu-id="f7ed3-161">MSIXIMAGEURI <IMsixImageUri>: Represents URI referring to MSIX Image</span></span>
  - <span data-ttu-id="f7ed3-162">`[Uri <String>]`: URI in immagine</span><span class="sxs-lookup"><span data-stu-id="f7ed3-162">`[Uri <String>]`: URI to Image</span></span>

## <span data-ttu-id="f7ed3-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7ed3-163">RELATED LINKS</span></span>

