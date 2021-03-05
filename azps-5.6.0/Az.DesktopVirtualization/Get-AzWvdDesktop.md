---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
ms.openlocfilehash: 2c276ab6b791d041000adf872bf2bfb807032ff2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980589"
---
# <span data-ttu-id="51e65-101">Get-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="51e65-101">Get-AzWvdDesktop</span></span>

## <span data-ttu-id="51e65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51e65-102">SYNOPSIS</span></span>
<span data-ttu-id="51e65-103">Ottenere un desktop.</span><span class="sxs-lookup"><span data-stu-id="51e65-103">Get a desktop.</span></span>

## <span data-ttu-id="51e65-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51e65-104">SYNTAX</span></span>

### <span data-ttu-id="51e65-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="51e65-105">List (Default)</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="51e65-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="51e65-106">Get</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="51e65-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="51e65-107">GetViaIdentity</span></span>
```
Get-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="51e65-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="51e65-108">DESCRIPTION</span></span>
<span data-ttu-id="51e65-109">Ottenere un desktop.</span><span class="sxs-lookup"><span data-stu-id="51e65-109">Get a desktop.</span></span>

## <span data-ttu-id="51e65-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51e65-110">EXAMPLES</span></span>

### <span data-ttu-id="51e65-111">Esempio 1: Ottenere un desktop virtuale di Windows in base al nome</span><span class="sxs-lookup"><span data-stu-id="51e65-111">Example 1: Get a Windows Virtual Desktop Desktop by name</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name DesktopName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="51e65-112">Questo comando recupera un desktop virtuale di Windows in un gruppo applicato.</span><span class="sxs-lookup"><span data-stu-id="51e65-112">This command gets a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

### <span data-ttu-id="51e65-113">Esempio 2: Elencare desktop virtuali Di Windows</span><span class="sxs-lookup"><span data-stu-id="51e65-113">Example 2: List Windows Virtual Desktop Desktops</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="51e65-114">Questo comando elenca i desktop virtuali di Windows in un gruppo applicato.</span><span class="sxs-lookup"><span data-stu-id="51e65-114">This command listsWindows Virtual Desktop Desktops in an applicaton Group.</span></span>

## <span data-ttu-id="51e65-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51e65-115">PARAMETERS</span></span>

### <span data-ttu-id="51e65-116">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="51e65-116">-ApplicationGroupName</span></span>
<span data-ttu-id="51e65-117">Nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="51e65-117">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e65-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51e65-118">-DefaultProfile</span></span>
<span data-ttu-id="51e65-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="51e65-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51e65-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51e65-120">-InputObject</span></span>
<span data-ttu-id="51e65-121">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="51e65-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51e65-122">-Name</span><span class="sxs-lookup"><span data-stu-id="51e65-122">-Name</span></span>
<span data-ttu-id="51e65-123">Nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="51e65-123">The name of the desktop within the specified desktop group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DesktopName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e65-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51e65-124">-ResourceGroupName</span></span>
<span data-ttu-id="51e65-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="51e65-125">The name of the resource group.</span></span>
<span data-ttu-id="51e65-126">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="51e65-126">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e65-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="51e65-127">-SubscriptionId</span></span>
<span data-ttu-id="51e65-128">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="51e65-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e65-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51e65-129">CommonParameters</span></span>
<span data-ttu-id="51e65-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51e65-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51e65-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="51e65-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51e65-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="51e65-132">INPUTS</span></span>

### <span data-ttu-id="51e65-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="51e65-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="51e65-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51e65-134">OUTPUTS</span></span>

### <span data-ttu-id="51e65-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span><span class="sxs-lookup"><span data-stu-id="51e65-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span></span>

### <span data-ttu-id="51e65-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktopList</span><span class="sxs-lookup"><span data-stu-id="51e65-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktopList</span></span>

## <span data-ttu-id="51e65-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="51e65-137">NOTES</span></span>

<span data-ttu-id="51e65-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="51e65-138">ALIASES</span></span>

<span data-ttu-id="51e65-139">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="51e65-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="51e65-140">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="51e65-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="51e65-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="51e65-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="51e65-142">INPUTOBJECT <IDesktopVirtualizationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="51e65-142">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="51e65-143">`[ApplicationGroupName <String>]`: nome del gruppo di applicazioni</span><span class="sxs-lookup"><span data-stu-id="51e65-143">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="51e65-144">`[ApplicationName <String>]`: nome dell'applicazione all'interno del gruppo di applicazioni specificato</span><span class="sxs-lookup"><span data-stu-id="51e65-144">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="51e65-145">`[DesktopName <String>]`: nome del desktop all'interno del gruppo di desktop specificato</span><span class="sxs-lookup"><span data-stu-id="51e65-145">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="51e65-146">`[HostPoolName <String>]`: nome del pool host all'interno del gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="51e65-146">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="51e65-147">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="51e65-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="51e65-148">`[MsixPackageFullName <String>]`: nome completo del pacchetto specifico della versione del pacchetto MSIX all'interno dello pool host specificato</span><span class="sxs-lookup"><span data-stu-id="51e65-148">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="51e65-149">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="51e65-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="51e65-150">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="51e65-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="51e65-151">`[SessionHostName <String>]`: nome dell'host di sessione all'interno del pool host specificato</span><span class="sxs-lookup"><span data-stu-id="51e65-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="51e65-152">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="51e65-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="51e65-153">`[UserSessionId <String>]`: nome della sessione utente all'interno dell'host di sessione specificato</span><span class="sxs-lookup"><span data-stu-id="51e65-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="51e65-154">`[WorkspaceName <String>]`: nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="51e65-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="51e65-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51e65-155">RELATED LINKS</span></span>

