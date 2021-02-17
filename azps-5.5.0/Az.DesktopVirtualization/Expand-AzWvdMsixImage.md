---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/expand-azwvdmsiximage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
ms.openlocfilehash: 56122e8d1ae94b6a898c073f2b2f2fb891504789
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186071"
---
# <span data-ttu-id="09ec0-101">Expand-AzWvdMsixImage</span><span class="sxs-lookup"><span data-stu-id="09ec0-101">Expand-AzWvdMsixImage</span></span>

## <span data-ttu-id="09ec0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09ec0-102">SYNOPSIS</span></span>
<span data-ttu-id="09ec0-103">Espande ed elenca i pacchetti MSIX in un'immagine, in base al percorso dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="09ec0-103">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="09ec0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09ec0-104">SYNTAX</span></span>

### <span data-ttu-id="09ec0-105">ExpandExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="09ec0-105">ExpandExpanded (Default)</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Uri <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="09ec0-106">Espandi</span><span class="sxs-lookup"><span data-stu-id="09ec0-106">Expand</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> -MsixImageUri <IMsixImageUri>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="09ec0-107">ExpandViaIdentity</span><span class="sxs-lookup"><span data-stu-id="09ec0-107">ExpandViaIdentity</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> -MsixImageUri <IMsixImageUri>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="09ec0-108">ExpandViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="09ec0-108">ExpandViaIdentityExpanded</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> [-Uri <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="09ec0-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="09ec0-109">DESCRIPTION</span></span>
<span data-ttu-id="09ec0-110">Espande ed elenca i pacchetti MSIX in un'immagine, in base al percorso dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="09ec0-110">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="09ec0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09ec0-111">EXAMPLES</span></span>

### <span data-ttu-id="09ec0-112">Esempio 1: espande il percorso immagine specificato e recupera i metadati del pacchetto trovati in AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="09ec0-112">Example 1: Expands specified Image Path and retrieves Package metadata found in AppxManifest.xml</span></span>
```powershell
PS C:\> Expand-AzWvdMsixImage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
          -Uri ImagePathURI

Name                          Type
----                          ----
HostPoolName/extractmsiximage Microsoft.DesktopVirtualization/hostpools/extractmsiximage
```

<span data-ttu-id="09ec0-113">Questo comando restituisce i metadati del pacchetto MSIX trovati nel percorso immagine specificato.</span><span class="sxs-lookup"><span data-stu-id="09ec0-113">This command returns Metadata of MSIX Package found in the given Image Path.</span></span>

## <span data-ttu-id="09ec0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09ec0-114">PARAMETERS</span></span>

### <span data-ttu-id="09ec0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09ec0-115">-DefaultProfile</span></span>
<span data-ttu-id="09ec0-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="09ec0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09ec0-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="09ec0-117">-HostPoolName</span></span>
<span data-ttu-id="09ec0-118">Nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="09ec0-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="09ec0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09ec0-119">-InputObject</span></span>
<span data-ttu-id="09ec0-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="09ec0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="09ec0-121">-MsixImageUri</span><span class="sxs-lookup"><span data-stu-id="09ec0-121">-MsixImageUri</span></span>
<span data-ttu-id="09ec0-122">Rappresenta l'URI che fa riferimento al costrutto Immagine MSIX, vedere la sezione NOTE per le proprietà MSIXIMAGEURI e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="09ec0-122">Represents URI referring to MSIX Image To construct, see NOTES section for MSIXIMAGEURI properties and create a hash table.</span></span>

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

### <span data-ttu-id="09ec0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09ec0-123">-ResourceGroupName</span></span>
<span data-ttu-id="09ec0-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="09ec0-124">The name of the resource group.</span></span>
<span data-ttu-id="09ec0-125">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="09ec0-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="09ec0-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="09ec0-126">-SubscriptionId</span></span>
<span data-ttu-id="09ec0-127">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="09ec0-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="09ec0-128">-Uri</span><span class="sxs-lookup"><span data-stu-id="09ec0-128">-Uri</span></span>
<span data-ttu-id="09ec0-129">URI in immagine</span><span class="sxs-lookup"><span data-stu-id="09ec0-129">URI to Image</span></span>

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

### <span data-ttu-id="09ec0-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09ec0-130">-Confirm</span></span>
<span data-ttu-id="09ec0-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09ec0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09ec0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09ec0-132">-WhatIf</span></span>
<span data-ttu-id="09ec0-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09ec0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09ec0-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09ec0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09ec0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09ec0-135">CommonParameters</span></span>
<span data-ttu-id="09ec0-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09ec0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09ec0-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="09ec0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09ec0-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="09ec0-138">INPUTS</span></span>

### <span data-ttu-id="09ec0-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri</span><span class="sxs-lookup"><span data-stu-id="09ec0-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri</span></span>

### <span data-ttu-id="09ec0-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="09ec0-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="09ec0-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09ec0-141">OUTPUTS</span></span>

### <span data-ttu-id="09ec0-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage</span><span class="sxs-lookup"><span data-stu-id="09ec0-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage</span></span>

## <span data-ttu-id="09ec0-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="09ec0-143">NOTES</span></span>

<span data-ttu-id="09ec0-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="09ec0-144">ALIASES</span></span>

<span data-ttu-id="09ec0-145">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="09ec0-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="09ec0-146">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="09ec0-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="09ec0-147">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="09ec0-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="09ec0-148">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="09ec0-148">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="09ec0-149">`[ApplicationGroupName <String>]`: nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="09ec0-149">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="09ec0-150">`[ApplicationName <String>]`: nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="09ec0-150">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="09ec0-151">`[DesktopName <String>]`: nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="09ec0-151">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="09ec0-152">`[HostPoolName <String>]`: nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="09ec0-152">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="09ec0-153">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="09ec0-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="09ec0-154">`[MsixPackageFullName <String>]`: nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="09ec0-154">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="09ec0-155">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="09ec0-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="09ec0-156">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="09ec0-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="09ec0-157">`[SessionHostName <String>]`: nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="09ec0-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="09ec0-158">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="09ec0-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="09ec0-159">`[UserSessionId <String>]`: nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="09ec0-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="09ec0-160">`[WorkspaceName <String>]`: nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="09ec0-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

<span data-ttu-id="09ec0-161">MSIXIMAGEURI: <IMsixImageUri> Rappresenta l'URI che fa riferimento all'immagine MSIX</span><span class="sxs-lookup"><span data-stu-id="09ec0-161">MSIXIMAGEURI <IMsixImageUri>: Represents URI referring to MSIX Image</span></span>
  - <span data-ttu-id="09ec0-162">`[Uri <String>]`: URI in immagine</span><span class="sxs-lookup"><span data-stu-id="09ec0-162">`[Uri <String>]`: URI to Image</span></span>

## <span data-ttu-id="09ec0-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09ec0-163">RELATED LINKS</span></span>

